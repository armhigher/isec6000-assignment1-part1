# isec6000-assignment1-part1
# There is two part of assignment1,this is part1 Part1 is the environmental construction and preparation of part2 in Windows system.

Outline: Build, configure, deploy, and maintain a comprehensive Saleor application suite on a Linux server using the knowledge acquired in Docker containerization, Kubernetes orchestration, integrated security concepts, and the Google Kubernetes Engine (GKE) environment.

Task1:Set Up Initial Infrastructure 
1. Create a Kubernetes Cluster on GKE
   [image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/4e143a76-8813-4caa-955b-c1456b0aeeda)
   
3. Configure your cluster settings, such as the cluster name, location, and node pool configuration.
   ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/b9e8e2db-7841-4cf0-8db5-fdd11ac993f3)
   
   after create,can check the status
   ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/d1ca386e-639e-41bc-ab45-8d36dad80eab)
   
4. Install and configure kubectl to manage your Kubernetes cluster.
   for windows: install link is: 
   https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/
 after install, test:
   ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/95d37a56-a2f1-4d52-8da3-f23f8f4e07b2)
   
    set environment variable to syetem path:
   ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/c1bcd297-1a45-4ebe-905c-eb4bf0589999)
   
4.Install gcloud command-line tool
   link: https://cloud.google.com/sdk/docs/install#windows
   after install and Log in to your Google Cloud account,then is time to connect cluster 
   ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/638d9cb2-0471-46d4-a4b5-79524fa40d39)

5.Obtain cluster credentials  
   Run the command "gcloud container clusters get-credentials <cluster-name> --zone <cluster-zone> --project <project-id>," 
           <cluster-name> is the name of your Kubernetes cluster, 
           <cluster-zone> is the region where the cluster is located
           <project-id> is your Google Cloud project's ID.
   the place to find the command:
   [1] click the cluster detail:
       ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/7257b710-8dfb-4c85-9ab2-cb0a2c6d730b)

       then
       ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/674c0596-b8cb-4902-8087-c6a19201e1b4)
       ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/907e98fb-0208-430b-bdf5-efd6975fc070)
   enter the command in the   Google cloud SDK shell
   result:
      ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/d17845c9-80ce-4ee5-a4c4-a51a010e99b8)

6.verify the connection
   use this command to check "kubectl cluster-info"   
   success:
   ![image](https://github.com/armhigher/isec6000-assignment1-part1/assets/130580265/fa1b5436-4d33-4707-95e5-0c80fc4c3091)


recap:
Simplified Steps to Connect to a Kubernetes Cluster
 [1] Install kubectl:Steps:  Install the kubectl command-line tool on your local computer.Reason: kubectl is the primary tool for interacting with Kubernetes clusters.
 [2]Install gcloud command-line tool (if not already installed):Steps: Install Google Cloud's gcloud command-line tool on your local computer. Reason: gcloud is used for managing Google Cloud resources and obtaining credentials for Kubernetes clusters. 
 [3]Log in to your Google Cloud account: Steps: Use the gcloud command-line tool to log in to your Google Cloud account.Reason: Logging in to your account is necessary to gain access to your Google Cloud project.
 [4]Obtain cluster credentials:Steps: Run the command "gcloud container clusters get-credentials <cluster-name> --zone <cluster-zone> --project <project-id>," where <cluster-name> is the name of your Kubernetes cluster, <cluster-zone> is the region where the cluster is located, and <project-id> is your Google Cloud project's ID.Reason: This step automatically generates a kubeconfig configuration file and adds cluster information and credentials to the configuration for use by kubectl.
 [5]Verify the connection:Steps: Run the "kubectl cluster-info" command to ensure a successful connection to the Kubernetes cluster.Reason: This command displays information about your cluster to verify that the connection is working correctly.
