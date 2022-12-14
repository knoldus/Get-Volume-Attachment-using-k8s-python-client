### Install Kubernetes Python Client:

`git clone --recursive https://github.com/kubernetes-client/python.git cd`

`cd python`

`python setup.py install`

### Installation from pip:

`pip install kubernetes`

### Listing Volume Attachments in your cluster using python

For Volume Attachments, we use StorageV1Api class from client module.

For listing Volume Attachments on local cluster e.g minikube we use the following command:

`config.load_kube_config()`

### Authentication to the Kubernetes Python Client in other cluster is done by: 

`configuration.api_key = {"authorization": "Bearer" + bearer_token}`

We will use here the Bearer Token which enable requests to authenticate using an access key.

In get_va.py file we have to provide our cluster details for listing Volume Attachments:


Give your cluster details:
```
cluster_details={
        "bearer_token":"<Your_cluster_bearer_token>",
        "api_server_endpoint":"<Your_cluster_IP>"
    }
```

### Running the File:
```
python3 get_va.py
```

You will get the list of Volume Attachments inside your cluster.