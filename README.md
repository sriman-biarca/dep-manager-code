## Deployment manager script for the below shell script
### https://github.com/spinnaker/spinnaker/blob/master/codelabs/gke-source-to-prod/install/setup.sh

# Modularized <br />
`service-account` - code to create service account and assign roles <br />
`pubsub` - code to create pubsub topic and subscription <br />
`basic-gke`- code to create GKE cluster <br />
`gsutil-cp` - code to upload files to GCS buckets and images to GCR <br />

# Single file
`template` -  combined all the modules into a single folder <br />

##NOTE
params are in .yaml file of the respective folders and description is in .schema file of the respective folder <br />

## Steps to setup only one respective resource

go to the respective directories <br />
### cd <dir_name>

## Create Deployment
syntax: gcloud deployment-manager deployments create <deployment_name> --config <config_file> <br />
example: gcloud deployment-manager deployments create basic-gke --config basic-gke.yaml <br />

## List Deployment
syntax: gcloud deployment-manager deployments list <br />


## Delete Deployment
syntax: gcloud deployment-manager deployments delete <deployment_name> <br />
example: gcloud deployment-manager deployments delete basic-gke <br />

# Steps to setup all resources at a go
## Create Deployment
syntax: gcloud deployment-manager deployments create <deployment_name> --config <config_file> <br />
example: gcloud deployment-manager deployments create basic-gke --config main.yaml <br />
