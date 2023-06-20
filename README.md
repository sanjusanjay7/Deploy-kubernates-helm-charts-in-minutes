#Sanjay kumar 
# Deploy-kubernates-helm-charts-in-minutes

#helm   #kubernetes #tutorial  #devops
<img width="527" alt="Screenshot 2023-06-20 113350" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/a6378be3-ecb8-4177-af28-e63366cd14f1">

With the ever-increasing popularity of Kubernetes the cloud-native landscape is gaining attention in developer communities. Helm, on the other hand, came as a saviour to help developers with Kubernetes-related deployments by making them super simple with the so-called 'Helm Charts'.

A Helm chart consists of all the necessary YAML manifests and templates that are needed to describe Kubernetes resources (Deployments, Secrets, CRDs, etc.) and other configurations needed for the Kubernetes application. Every application can now be packaged as a Helm chart and deployed wherever you want.

Today, in this tutorial, I'll show you how you can deploy any publicly available Helm chart in minutes using Harness CD.

##Prerequisites
Free Harness CD account with free builds to deploy our helm chart.
A Kubernetes cluster access from any cloud provider.
##Tutorial
Login to your Harness CD module and start your free plan where you get free builds.

<img width="534" alt="Screenshot 2023-06-20 113414" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/feab4cef-509a-4d89-bb96-9fad313783b4">

In this tutorial, we will take Grafana Helm chart as an example to deploy. The Grafana chart is available here - https://github.com/bitnami/charts/tree/main/bitnami/grafana

Create a project to start with and name it.

<img width="521" alt="Screenshot 2023-06-20 113448" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/fed45afb-0418-4084-807e-b561c97b4752">

Invite collaborators to your project if you want

<img width="549" alt="Screenshot 2023-06-20 113508" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/fc59647c-3cf5-4a4e-af91-8d26d346a20a">

Select 'Continuous Delivery' from the modules available.

<img width="535" alt="Screenshot 2023-06-20 113531" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/b0a87e0a-b9e7-4c0f-8ddc-e58eea5cb5d7">

For this deployment pipeline, we need Harness Delegate to be up and running. Let's create the Harness Delegate.

<img width="517" alt="Screenshot 2023-06-20 113552" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/ce0b1ce1-8ffb-4ef7-be81-c4a9c7dcf687">

##So, what is Harness Delegate?
Delegate is a service that runs on your infrastructure to execute tasks on behalf of the Harness platform.

Now, you need to install this Harness Delegate on your Kubernetes cluster.

Make sure you have a cluster access from any cloud provider.
You can also use Minikube or Kind.

<img width="533" alt="Screenshot 2023-06-20 113612" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/44becff0-db73-40b7-ad56-18d99d901687">

Follow the step-by-step guide as shown and install the Delegate.

<img width="175" alt="Screenshot 2023-06-20 113756" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/8217ecd1-7efa-4055-8dd5-b3ad16dfd835">

Once the Harness Delegate is installed, go back to the pipeline dashboard and create a pipeline.

<img width="186" alt="Screenshot 2023-06-20 113821" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/7886cd17-8513-4b47-a027-f9cf3412dc82">

Name the stage and deployment type as 'Native Helm'.

<img width="189" alt="Screenshot 2023-06-20 113848" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/5f444259-8a11-4576-881f-34c7a80079db">

Add the Helm store details

<img width="185" alt="Screenshot 2023-06-20 113906" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/fee9f20e-88f0-4577-a0a5-b68a16dad984">

Add all the required details

<img width="184" alt="Screenshot 2023-06-20 113925" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/089ac277-a4d8-4334-bbbd-6c0a0299d074">

Save everything and you can see the manifest details added for the service.

<img width="180" alt="Screenshot 2023-06-20 113948" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/5b1c7efb-8c12-4893-ae82-000b8ffcd9f2">

Select the execution strategy as 'Rolling'

<img width="186" alt="Screenshot 2023-06-20 114014" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/d4c60899-3d70-434b-b666-a94aa2f426cd">

Save everything and run the pipeline. You should see a successful Grafana Helm chart deployment.

<img width="181" alt="Screenshot 2023-06-20 114031" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/56b2bb69-a968-4dec-bda4-004aa965d934">

Open the http://localhost:8080/ on your machine and you should see the Grafana login page.

<img width="185" alt="Screenshot 2023-06-20 114056" src="https://github.com/sanjusanjay7/Deploy-kubernates-helm-charts-in-minutes/assets/131652504/9c07a461-94f9-4fc0-94b5-2bef270b7c84">

This way, we can easily deploy any publicly available Helm chart using Harness CD.

This way, you can easily deploy any Helm charts from this public repo - https://github.com/bitnami/charts/tree/main/bitnami in just minutes.

Try Harness CD, the most advanced and trusted continuous delivery platform.
