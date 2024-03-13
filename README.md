# helm-charts

Followed instructions from here to create this helm chart repo:

https://tech.paulcz.net/blog/creating-a-helm-chart-monorepo-part-1/


To add repo in helm use this though: 

helm repo add --username <git-username> --password <token> helm-charts https://raw.githubusercontent.com/Adlucent/helm-charts/gh-pages/


If you want to use helm in a clouldbuild.yaml, beware that helm doesn't come with GCP Cloud Build by default.  

You need to build it:

git clone https://github.com/GoogleCloudPlatform/cloud-builders-community.git

cd cloud-builders-community

cd helm

gcloud builds submit . --config=cloudbuild.yaml


