# Reflection on Hello Minikube

1. Compare the application logs before and after you exposed it as a Service. Try to open the app several times while the proxy into the Service is running. What do you see in the logs? Does the number of logs increase each time you open the app?

Yes the number of logs increase everytime the the service is running. The number of logs increases by two everytime the app is opened. The extra logs contains the incoming HTTP request.

2. Notice that there are two versions of `kubectl get` invocation during this tutorial section. The first does not have any option, while the latter has `-n` option with value set to `kube-system`. What is the purpose of the `-n` option and why did the output not list the pods/services that you
explicitly created?

The purpose of the `-n` option is to specify the namespace. The output did not list the pods/services that I explicitly created because the namespace was not specified. 

# Reflection on Rolling Update & Kubernetes Manifest File

1. What is the difference between Rolling Update and Recreate deployment strategy?

The difference between Rolling Update and Recreate deployment strategy is that Rolling Update updates the deployments, keeping it avaliable during the update process. Recreate deployment strategy deletes the old deployment and creates a new one.

2. Try deploying the Spring Petclinic REST using Recreate deployment strategy and document
your attempt.

I just Copied the `deployment.yaml` file and change the strategy type to `Recreate` and rename it as `deployment-recreate.yaml` and aplly it to new cluster

3. Prepare different manifest files for executing Recreate deployment strategy.

Check in the git repository for `deployment-recreate.yaml`

4. What do you think are the benefits of using Kubernetes manifest files? Recall your experience
in deploying the app manually and compare it to your experience when deploying the same app
by applying the manifest files (i.e., invoking `kubectl apply -f` command) to the cluster.

The benefits of using Kubernetes manifest files is that it is easier to deploy the app. It is easier to deploy the app using the manifest files because it is easier to keep track of the changes made to the app.



