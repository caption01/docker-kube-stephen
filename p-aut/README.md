# Docker and Kubernetes: The Complete Guide

https://www.udemy.com/course/docker-and-kubernetes-the-complete-guide

## Section1
12. But Really...What's a Container?

## Section2
17. Container Lifecycle
24. The Purpose of the IT Flag

## Section3
32. The Build Process in Detail
36. Manual Image Generation with Docker Commit

## Section5
53. Docker Compose Files
54. Networking with Docker Compose
55. Docker Compose Commands
58. Automatic Container Restarts
59. Container Status with Docker Compose

## Section6
68. Creating the Dev Dockerfile
```bash
docker build -f Dockerfile.dev .
```
72. Docker Volumes
74. Bookmarking Volumes
```bash
docker run -it -p 3000:3000 -v /app/node_modules  -v $(pwd):/app CONTAINER_ID
```
76. Shorthand with Docker Compose
77. Overriding Dockerfile Selection
80. Executing Tests
```bash
docker run -it CONTAINER_ID npm run test    
```
82. Docker Compose for Running Tests
85. Need for Nginx
87. Implementing Multi-Step Builds

## Section9
129. Environment Variables with Docker Compose
131. Nginx Path Routing
132. Routing with Nginx
133. Building a Custom Nginx Image

## Section11
151. Multi-Container Definition Files
152. Finding Docs on Container
153. Adding Container Definitions to DockerRun
154. More Container Definitions
155. Forming Container Links
157. Managed Data Service Providers

## Section12
174. The Why's and What's of Kubernetes
186. Running Containers in Pods

## Section13
191. Updating Existing Objects
193. Limitations in Config Updates
203. Triggering Deployment Updates
204. Imperatively Updating a Deployment's Image
```bash
#kubectl set image <object_type>/<object_name> <contain_name>=<new_image_to_use>
kubectl set image deployment/client-deployment client=stephengrider/multi-client:v5
```

## Section14
212. NodePort vs ClusterIP Services
223. The Need for Volumes with Databases
224. Kubernetes Volumes
225. Volumes vs Persistent Volumes
226. Persistent Volumes vs Persistent Volume Claims
228. Persistent Volume Access Modes
229. Where Does Kubernetes Allocate Persistent Volumes?
234. Creating an Encoded Secret
```bash
#kubectl create secret generic <secret_name> --from-literal key=value
kubectl create secret generic pgpassword --from-literal PGPASSWORD=password123
```
237. Environment Variables as Strings

## Section14
239. A Quick Note on Ingresses
```bash
# We're using ingress-nginx, a community led project.
# https://kubernetes.github.io/ingress-nginx/
```
