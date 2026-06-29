# DevOps Project Assignment - Docker + Jenkins + Kubernetes

## Project :-  End-to-End CI/CD Pipeline Automation Using Docker, Jenkins and Kubernetes**

**Prepared By:**
**Srushti Tembhurne**

**Role:**
**DevOps Engineer**

**Date: 28/06/2026**



 
 
 
 
 
 #                                                             Architecture

                                                            
<img width="940" height="624" alt="image" src="https://github.com/user-attachments/assets/674306af-48cc-49bd-9479-7340c62ef068" />




## EC2 instance:-
<img width="940" height="331" alt="image" src="https://github.com/user-attachments/assets/ba0171d6-5477-4fe3-b5d9-80e767056c67" />



## Security Group:-
<img width="940" height="425" alt="image" src="https://github.com/user-attachments/assets/4acbfd90-83bd-4d41-a066-be9e2a82b4cb" />


## Dockerfile :-

<img width="940" height="261" alt="image" src="https://github.com/user-attachments/assets/471f101f-3d0b-4a91-b7d7-73e2a05426c5" />


## Docker Images:-
<img width="940" height="177" alt="image" src="https://github.com/user-attachments/assets/d51c02c5-0be3-4503-ac39-e903f2ba5f36" />


## Docker Container :-
<img width="940" height="100" alt="image" src="https://github.com/user-attachments/assets/0569c9bd-69a3-4ddf-a828-d85cd1502b2c" />


## On Browser:-
<img width="890" height="246" alt="image" src="https://github.com/user-attachments/assets/4402aae7-dab1-4371-ac5a-7c932dc66051" />


## Docker Container:-
<img width="940" height="94" alt="image" src="https://github.com/user-attachments/assets/b3ab094d-1589-4633-b88f-8675a685e3a9" />


## Dockerhub:-
<img width="940" height="218" alt="image" src="https://github.com/user-attachments/assets/d67fc592-764d-471c-a1ef-46bc146194c9" />


## Pod:-
<img width="940" height="187" alt="image" src="https://github.com/user-attachments/assets/32d25fc7-3b14-4ced-b889-c99216997d85" />



## Jenkins pipeline:-
<img width="940" height="206" alt="image" src="https://github.com/user-attachments/assets/23a93057-fadb-4ff5-9af9-0d78b847c998" />
<img width="940" height="318" alt="image" src="https://github.com/user-attachments/assets/5597bebc-6e9a-43e0-a024-1948810102b8" />



## Deployment:-
<img width="940" height="133" alt="image" src="https://github.com/user-attachments/assets/14ec2d86-c8ef-4ad4-b447-f6a4f1fdc1f3" />



## Service:-
<img width="940" height="125" alt="image" src="https://github.com/user-attachments/assets/81d7c97b-407a-462b-8784-ef0c6a3e9432" />


## deployment.yml file :-
<img width="940" height="832" alt="image" src="https://github.com/user-attachments/assets/da27af01-9f85-4dc9-b1fd-6e613d870eb9" />
<img width="759" height="171" alt="image" src="https://github.com/user-attachments/assets/ca348921-ffb9-431f-acf6-5c9e20736214" />



## Service.yml file :-
<img width="926" height="615" alt="image" src="https://github.com/user-attachments/assets/4cc8e54b-65a5-4687-b495-d88db71a3f9d" />


## Jenkisnfile:-  
<img width="940" height="528" alt="image" src="https://github.com/user-attachments/assets/5a63a56c-fd45-48bc-8aaf-5f7205f7d4c8" />
<img width="940" height="755" alt="image" src="https://github.com/user-attachments/assets/0497dce8-f7eb-4f3b-9e8c-48605ffd2e77" />
<img width="801" height="615" alt="image" src="https://github.com/user-attachments/assets/e6a07296-273c-4667-a4cc-1105f79dccf3" />



#                                                     Answer of all Question
## 1.	What problem does Docker solve? 
Docker solves the problem of application portability, dependency management, and environment inconsistency.
Benefits:
•	Same application runs everywhere. 
•	Faster deployment. 
•	Easy scaling. 
•	Better resource utilization. 
•	Consistent environments.




## 2.	Difference between VM and Container?
**Virtual Machine**	                                                
Runs complete operating system	                             
Uses more CPU and RAM	                                       
 Takes minutes to start	                                    
 Uses hypervisor	                                            
 Large size (GBs)	                                           
 Hardware virtualization	                                    
Example: VMware, VirtualBox	                                 

**Container**
Shares host OS kernel
Lightweight
Starts in seconds
Uses Docker Engine
Small size (MBs)
OS-level virtualization
Example: Docker


## 3.	What is an Image?
A Docker Image is a read-only template used to create containers.
It contains:
•	Application code 
•	Runtime 
•	Libraries 
•	Dependencies 
•	Configuration

## 4.	What is a Container?
A Container is a running instance of a Docker Image.

## 5.	What happens if a container is deleted?
If a container is deleted, the container data is removed but the image and external volumes remain.


## 6)Difference between Image and Container?
**Image**                                                      
Blueprint/template	                                            
Read-only	                                                   
Does not run	                                               
Created using Dockerfile	                                   
Stored in registry	                                          
---------- 
**Container**
Running instance
Writable layer
Runs application
Created from Image 
Runs on Docker Engine

 
## 7)Difference between docker stop and docker rm?
**docker stop**	                                                                  
Stops container	                                                        
Container remains	                                                      
Data inside container remains temporarily	                              
Can restart	                                                             
Used for maintenance	                                                  
 **docker rm**
Deletes container
Container removed
Container metadata removed
Cannot restart
Used for cleanup


## 8)Where are container logs stored?
Docker stores container logs by default under /var/lib/docker/containers, and logs can be viewed using docker logs.

## 9)Why are volumes needed?
Docker volumes are used for persistent data storage.
By default, data created inside a container exists only inside the container filesystem. If the container is deleted, that data is lost.
Volumes solve this problem by storing data outside the container lifecycle.


## 10)What happens without volumes?
Without volumes:
•	Data is stored inside container writable layer. 
•	Container deletion removes data. 
•	Data is not shared between containers. 
•	Database data can be lost. 

## 11)Difference between Volume and Bind Mount?
**Docker Volume**	                                                        
Managed by Docker	                                             
Stored in Docker storage area	                                 
More secure	                                                      
Recommended for production	                                      
Docker manages lifecycle	                                       
**Bind Mount**
  Managed by user
 Stored anywhere on host
 Less isolated
 Mostly development use
 User manages files

 
## 12)Why use custom networks?
Custom Docker networks are used to allow containers to communicate with each other securely and easily using container names.
By default, Docker creates a default bridge network, but custom networks provide better isolation and service communication.





## 13)Difference between bridge and host network?
**Bridge Network**	                                                                     
Default mode        	                                                               
Container has own IP	                                                              
More isolation	                                                                      
Requires port mapping	                                                             
More secure	                                                                         
Good for most applications	   

 **Host Network**
 Uses host network
 Container shares host IP
 Less isolation
 No port mapping
  Less secure
  Used for high-performance workloads

   
## 14)How do containers communicate?
Containers communicate using:
1.	Docker Networks 
2.	Container IP addresses 
3.	Container DNS names

   
## 15)What is Jenkins?
Jenkins is an open-source automation server used to automate the software development lifecycle, especially Continuous Integration (CI) and Continuous Delivery/Deployment (CD).

## 16)What problem does Jenkins solve?
Jenkins solves the problem of manual, slow, and error-prone software delivery processes by automating build, testing, and deployment.


## 17)Difference between CI and CD?
CI :- focuses on automatically building and testing code changes.
CD:- focuses on automatically delivering or deploying the tested application to environments like staging or production.

## 18)What is a Jenkins Pipeline?
A Jenkins Pipeline is a set of automated steps written as code that defines the complete software delivery process.
It describes how Jenkins should:
•	Get source code 
•	Build application 
•	Run tests 
•	Create Docker images 
•	Push images to registry 
•	Deploy application 
•	Verify deployment 
A Jenkins Pipeline is usually written in a file called Jenkinsfile.
stored inside the Git repository.

## 19)Why use pipelines instead of manual deployments?
Pipelines are used because manual deployments are:
•	Slow 
•	Error-prone 
•	Difficult to repeat 
•	Hard to track

## 20)Difference between Freestyle and Pipeline jobs?
**Freestyle Job**                                           	
Configured using Jenkins UI	                              
Hard to maintain for large projects	                      
Limited version control	                                  
Manual configuration	                                
Less suitable for DevOps	                             
Difficult to replicate	                                  

**Pipeline Job**
Written as code
Easy to maintain	
Jenkinsfile stored in Git
Automated workflow
Recommended for CI/CD
Easily reusable


  
## 21)Why use a registry?
A Docker Registry is used to store, manage, and distribute Docker images.

## 22)Difference between local image and registry image?
**Local Image**                                                
Stored on one machine	                                
Not shared	                                          
Built locally	                                        
Limited availability	                                
Used for development/testing	                       
**Registry Image**
Stored in central repository
Shared
Pulled by servers
Available anywhere
 Used for deployment

 
## 23)Why not build images directly on production servers?
Building images directly on production servers is not recommended because it creates security, stability, and deployment problems.


## 24)What is Kubernetes?
Kubernetes (K8s) is an open-source container orchestration platform used to automate the deployment, scaling, networking, and management of containerized applications.

## 25)Why not run containers directly?
We do not run containers directly in production because manual management becomes difficult for scaling, recovery, networking, and updates.

## 26)What problems does Kubernetes solve?
Kubernetes solves problems like self-healing, automatic scaling, load balancing, rolling updates, rollback, and maintaining the desired state of applications.

## 27)What is a Pod?
A Pod is the smallest deployable unit in Kubernetes that runs one or more containers.


## 28)Why doesn't Kubernetes deploy containers directly?
Kubernetes does not deploy containers directly because a Pod provides an additional management layer around containers.
Containers need:
•	Networking 
•	Storage 
•	Lifecycle management 
•	Resource control 
•	Communication 
Kubernetes uses Pods to provide these features.


## 29) Can a Pod contain multiple containers?
Yes, a Pod can contain multiple containers.

## 30)Why did the Pod return automatically?
The Pod returned automatically because it was managed by a Kubernetes Deployment.
Kubernetes continuously monitors the actual state of the application and compares it with the desired state.


## 31)Difference between Pod and Deployment?
 **Pod**                                                  
Smallest Kubernetes unit	                       
Runs containers	                                  
Cannot self-heal alone	                          
No replica management	                           
No rolling updates	                              
Temporary object	                              

**Deployment**
Kubernetes controller
 Manages Pods
 Provides self-healing
 Maintains replicas
 Supports rolling updates
 Long-term management
 
## 32)What is desired state?
Desired state is the configuration we define, such as the number of replicas, that Kubernetes continuously maintains automatically.

## 32)Why do Pods need Services?
Pods need Services because Pod IP addresses are temporary and can change whenever Pods restart or are recreated.
A Kubernetes Service provides:
•	Stable network access 
•	Load balancing 
•	Service discovery 
•	Communication between applications

## 33)Difference between ClusterIP and NodePort?
**ClusterIP**                                    
Default service type	                      
Internal communication only	                  
No external IP	                              
More secure	                                   
Used in production internally	              
**NodePort**
 External access service
 Accessible outside cluster
 Uses node IP + port
 Less secure
 Used for testing/demo

 
## 34)What happens when Pod IP changes?
When a Pod IP changes, Kubernetes automatically updates the Service endpoints and redirects traffic to the new Pod.



## 35)What is a rolling update?
A rolling update is a Kubernetes deployment strategy where the old version of an application is gradually replaced with a new version without stopping the entire application.

## 36)Why is rolling update safer?
Rolling updates are safer because Kubernetes keeps the old version running while deploying the new version.


## 37)What is zero downtime deployment?
Zero downtime deployment means releasing a new application version without making the application unavailable to users.
Users can continue using the application during deployment.

## 38)Why are rollbacks important?
A rollback is the process of returning an application to a previous stable version after a failed deployment.
Rollbacks are important because new application releases can introduce:
•	Bugs 
•	Configuration issues 
•	Performance problems 
•	Deployment failures 
•	Compatibility issues 
Instead of manually fixing production immediately, Kubernetes can quickly restore the previous working version.


## 39)How does Kubernetes maintain availability?
Kubernetes maintains availability using replicas, self-healing, Services for load balancing, rolling updates, automatic Pod replacement, and rescheduling workloads when failures occur.	
	
## 40)How does Jenkins communicate with Kubernetes?
Jenkins communicates with Kubernetes using the Kubernetes API Server.

## 41)Why automate deployments?
Deployment automation reduces manual work and provides faster, safer, and repeatable releases.

## 42)What risks exist in manual deployments?
Manual deployments have risks such as configuration mistakes, downtime, inconsistent environments, security issues, and slower recovery.


	
	

#                                                      complete CI/CD flow

	             
"In this project, I have implemented a complete CI/CD pipeline using Docker, Jenkins, Docker Registry, and Kubernetes."
The flow starts with the Developer. Developer writes application code and pushes the changes to the Git repository like GitHub. Git is used for version control and maintaining application source code.
After code is pushed, Jenkins automatically triggers the pipeline. Jenkins is used for automation of build and deployment processes. In my Jenkins pipeline, first it clones the latest code from Git, then builds the Docker image.
Next, Docker packages the application and its dependencies into a container image. The Docker image provides a consistent environment so the application runs the same way everywhere.
After creating the image, Jenkins pushes it to a Docker Registry like Docker Hub. The registry works as a centralized storage location where Docker images are stored and Kubernetes can pull them.
Then Jenkins communicates with the Kubernetes cluster using kubectl commands. Kubernetes Deployment pulls the image from the registry and creates Pods to run the application.
A Pod is the smallest unit in Kubernetes that runs containers. The Deployment maintains the required number of replicas and provides self-healing, scaling, and rolling updates.
Finally, the Kubernetes Service exposes the application to users. Since Pod IPs can change, the Service provides a stable endpoint and load balances traffic between Pods.
The complete flow is:
**Developer → Git → Jenkins → Docker Build → Docker Registry → Kubernetes Deployment → Service → Users**
This automation provides faster deployments, reduces manual errors, supports rolling updates, rollback, and helps achieve high availability with zero downtime deployment.







