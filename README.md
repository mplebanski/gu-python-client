# gu-python-client
API description in Markdown.

This Python package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: org.openapitools.codegen.languages.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/prekucki/gu-python-client.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/prekucki/gu-python-client.git`)

Then import the package:
```python
import gu_rest_api 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import gu_rest_api
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import gu_rest_api
from gu_rest_api.rest import ApiException
from pprint import pprint

configuration = gu_rest_api.Configuration()
# Configure API key authorization: serviceToken
configuration.api_key['X-GU-APIKEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-GU-APIKEY'] = 'Bearer'
configuration = gu_rest_api.Configuration()
# Configure API key authorization: systemName
configuration.api_key['X-GU-APPNAME'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-GU-APPNAME'] = 'Bearer'

# create an instance of the API class
api_instance = gu_rest_api.PeerApi(gu_rest_api.ApiClient(configuration))
node_id = 'node_id_example' # str | GU Network node identifier
spec = gu_rest_api.DeploymentSpec() # DeploymentSpec | 

try:
    api_response = api_instance.create_deployment(node_id, spec)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PeerApi->create_deployment: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *http://127.0.0.1:61622*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*PeerApi* | [**create_deployment**](docs/PeerApi.md#create_deployment) | **POST** /peers/{nodeId}/deployments | 
*PeerApi* | [**drop_deployment**](docs/PeerApi.md#drop_deployment) | **DELETE** /peers/{nodeId}/deployments/{deploymentId} | Removes deployment
*PeerApi* | [**get_peer_details**](docs/PeerApi.md#get_peer_details) | **GET** /peers/{nodeId} | Returns detailed peer info
*PeerApi* | [**list_deployments**](docs/PeerApi.md#list_deployments) | **GET** /peers/{nodeId}/deployments | 
*PeerApi* | [**list_peers**](docs/PeerApi.md#list_peers) | **GET** /peers | Returns a list hub peers.
*PeerApi* | [**update_deployment**](docs/PeerApi.md#update_deployment) | **PATCH** /peers/{nodeId}/deployments/{deploymentId} | 
*SessionApi* | [**add_session_peers**](docs/SessionApi.md#add_session_peers) | **POST** /sessions/{sessionId}/peers | Manually adds peers to hub session
*SessionApi* | [**create_blob**](docs/SessionApi.md#create_blob) | **POST** /sessions/{sessionId}/blobs | Creates new lob
*SessionApi* | [**create_deployment**](docs/SessionApi.md#create_deployment) | **POST** /sessions/{sessionId}/peers/{nodeId}/deployments | Creates new deployment
*SessionApi* | [**create_session**](docs/SessionApi.md#create_session) | **POST** /sessions | Creates new hub session.
*SessionApi* | [**delete_blob**](docs/SessionApi.md#delete_blob) | **DELETE** /sessions/{sessionId}/blobs/{blobId} | 
*SessionApi* | [**delete_deployment**](docs/SessionApi.md#delete_deployment) | **DELETE** /sessions/{sessionId}/peers/{nodeId}/deployments/{deploymentId} | 
*SessionApi* | [**delete_session**](docs/SessionApi.md#delete_session) | **DELETE** /sessions/{sessionId} | 
*SessionApi* | [**download_blob**](docs/SessionApi.md#download_blob) | **GET** /sessions/{sessionId}/blobs/{blobId} | Downloads binary content from the hub
*SessionApi* | [**get_config**](docs/SessionApi.md#get_config) | **GET** /sessions/{sessionId}/config | Gets configuration from stash
*SessionApi* | [**get_session**](docs/SessionApi.md#get_session) | **GET** /sessions/{sessionId} | Gets hub session info
*SessionApi* | [**list_blobs**](docs/SessionApi.md#list_blobs) | **GET** /sessions/{sessionId}/blobs | Lists currently allocated lobs
*SessionApi* | [**list_session_peers**](docs/SessionApi.md#list_session_peers) | **GET** /sessions/{sessionId}/peers | List session peers
*SessionApi* | [**list_sessions**](docs/SessionApi.md#list_sessions) | **GET** /sessions | Lists current hub sessions.
*SessionApi* | [**set_config**](docs/SessionApi.md#set_config) | **PUT** /sessions/{sessionId}/config | Sets configuration stash
*SessionApi* | [**update_deployment**](docs/SessionApi.md#update_deployment) | **PATCH** /sessions/{sessionId}/peers/{nodeId}/deployments/{deploymentId} | Sends multiple commands for peer
*SessionApi* | [**update_session**](docs/SessionApi.md#update_session) | **PATCH** /sessions/{sessionId} | Hub session update
*SessionApi* | [**upload_blob**](docs/SessionApi.md#upload_blob) | **PUT** /sessions/{sessionId}/blobs/{blobId} | Uploads a binary content to the hub.


## Documentation For Models

 - [BlobInfo](docs/BlobInfo.md)
 - [Command](docs/Command.md)
 - [DeploymentInfo](docs/DeploymentInfo.md)
 - [DeploymentSpec](docs/DeploymentSpec.md)
 - [DeploymentSpecImage](docs/DeploymentSpecImage.md)
 - [DeploymentStatus](docs/DeploymentStatus.md)
 - [DockerCreateOptions](docs/DockerCreateOptions.md)
 - [DownloadFileCommand](docs/DownloadFileCommand.md)
 - [EnvType](docs/EnvType.md)
 - [ExecCommand](docs/ExecCommand.md)
 - [FileFormat](docs/FileFormat.md)
 - [HubSession](docs/HubSession.md)
 - [HubSessionCommand](docs/HubSessionCommand.md)
 - [HubSessionTouchCommand](docs/HubSessionTouchCommand.md)
 - [PeerDetails](docs/PeerDetails.md)
 - [PeerInfo](docs/PeerInfo.md)
 - [ProcessInfo](docs/ProcessInfo.md)
 - [StartCommand](docs/StartCommand.md)
 - [StopCommand](docs/StopCommand.md)
 - [UploadFileCommand](docs/UploadFileCommand.md)
 - [VolumeDef](docs/VolumeDef.md)
 - [VolumeDefBindRw](docs/VolumeDefBindRw.md)


## Documentation For Authorization


## serviceToken

- **Type**: API key
- **API key parameter name**: X-GU-APIKEY
- **Location**: HTTP header


## systemName

- **Type**: API key
- **API key parameter name**: X-GU-APPNAME
- **Location**: HTTP header


## Author




