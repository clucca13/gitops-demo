# gitops-pipeline-demo
Repo that contains the manifests for gitops pipeline demos

**Please fork or clone this into your own repo!
**

This demo requires 3 clusters and one harness gitops agent.

1 cluster has the gitops agent, you will deploy the appset to this cluster in the argocd namespace
1 cluster is the dev version of the application
1 cluster is the prod version
You will need service accounts and tokens configured for the dev and prod clusters

In Harness





Edit https://github.com/clucca13/gitops-demo/blob/main/helm/app/appset.yaml and change

      repoURL: https://github.com/clucca13/gitops-demo.git <--change to your repo name
      project: 06af6bc2 <-- change to your harness project ID, this can be found in gitops:Settings>GitOpsAgent>Mapped Harness Project

![image](https://github.com/clucca13/gitops-demo/assets/63068621/95297bac-5331-4c72-84dd-d0e210908f7b)


Edit helm/app/prod/testcluster1/lucca-gitops-prod/config.json and helm/app/qa/testcluster1/lucca-gitops-prod/config.json






Create a new gitops application in Harness called "gitops-demo" 
Create a new service called gitops-demo
Create a new environment called gitops-demo



