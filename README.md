## Deployment manager script for the below shell script
### https://github.com/spinnaker/spinnaker/blob/master/codelabs/gke-source-to-prod/install/setup.sh

`service-account` - code to create service account and assign roles
`pubsub` - code to create pubsub topic and subscription
`basic-gke`- code to create GKE cluster
`gsutil-cp` - code to upload files to GCS buckets and images to GCR.

##NOTE
params are in .yaml file of the respective folders and description is in .schema file of the respective folder.

## Steps to setup

go to the respective directories
### cd <dir_name>

## Create Deployment
syntax: gcloud deployment-manager deployments create <deployment_name> --config <config_file>
example: gcloud deployment-manager deployments create basic-gke --config basic-gke.yaml

## List Deployment
syntax: gcloud deployment-manager deployments list


## Delete Deployment
syntax: gcloud deployment-manager deployments delete <deployment_name>
example: gcloud deployment-manager deployments delete basic-gke
