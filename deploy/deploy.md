# Deployment Instructions

This document needs to contain all information on how to deploy the lab. 

## RHPDS link 
None

## Instructions to deploy on RHPDS
Currently would be similar to "non-RHPDS" instructions, below,
assuming a working RHPDS openshift cluster.

## Instructions to deploy outside of RHPDS
```sh
# Install Open Data Hub on your cluster and relevante namespace
$ oc apply -f /path/to/cluster-demo/deploy/clusterdemo.yaml

```

To run the lab:
1. Bring up JupyterHub Launcher (assuming something like Open Data Hub)
1. Set `JUPYTER_PRELOAD_REPOS = https://github.com/erikerlandson/cluster-demo.git`
1. Run notebook `33-clusterdemo-train.ipynb` if you want to show a data scientist exploration workflow
1. Run notebook `33-clusterdemo-train-s2i.ipynb` to demonstrate what a source-to-image notebook convention looks like
1. Kick off the clusterdemo-build build in OpenShift (this takes 5-10 minutes to run)
1. Run `33-clusterdemo-client.ipynb` to demonstrate the running micro service
