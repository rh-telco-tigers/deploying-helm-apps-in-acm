In this post, I am going to show how a Helm-based application is deployed in ACM (Advanced Cluster Management).  This application will be mysql.

First, Mysql will be deployed by specifying the Helm repo and chart. This method is based off a tar.gz (tgz) file which is contained on a webserver (see https://helm.sh/docs/topics/chart_repository/).  Within that tgz file are default deployment settings (values.yaml) that will get applied.

Secondly,  I will make a modification to the default deployment settings (values.yaml) to show how a Helm-chart that doesn't use default settings is deployed.  In contrast to the first method, this is deployed via Github.

The default deployment of Mysql will show the Application/Subscription (AppSub) model which is the default in ACM.  For the second example, an ApplicationSet will be used which is based off of Openshift Gitops/ArgoCD.  

In the end, you will see how the AppSub model and ApplicationSet models differ.  Also, you will be prepared to deploy Helm-based apps via ACM that can have deployment settings other than the default ones.

Here are the contents of this article:

A.  Installing Openshift Gitops on Hub Cluster

B.  Integrating Openshift Gitops with ACM

C.  Explanation of Mysql Helm Repo

D.  Deploying AppSub Version of Mysql (default deployment settings)

E.  Deploying Openshift Gitops/ArgoCD Version of Mysql (non-default settings)

https://github.com/kcalliga/helm-mysql
https://www.myopenshiftblog.com/deploying-helm-based-acm-applications/
