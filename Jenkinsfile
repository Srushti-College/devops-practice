pipeline {

    agent any

    stages {

        stage('Git Clone') {

            steps {

                git branch: 'main',
                    url: 'https://github.com/Srushti-College/devops-practice.git'

            }

        }


        stage('Docker Build') {

            steps {

                sh 'docker build -t srushti22/myapp:v1 .'

            }

        }


        stage('Push Image') {

            steps {

                withCredentials([usernamePassword(
                    credentialsId: 'docker-creds',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {

                    sh '''
                    docker login -u $DOCKER_USER -p $DOCKER_PASS
                    docker push srushti22/myapp:v1
                    '''

                }

            }

        }


        stage('Deploy Kubernetes') {

            steps {

                sh '''
                kubectl apply -f deployment.yaml
                kubectl apply -f service.yaml
                '''

            }

        }


        stage('Verify') {

            steps {

                sh '''
                kubectl get pods
                kubectl get svc
                '''

            }

        }

    }

}
