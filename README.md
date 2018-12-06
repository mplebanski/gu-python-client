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

# Configure API key authorization: serviceToken
configuration = gu_rest_api.Configuration()
configuration.api_key['X-GU-APIKEY'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-GU-APIKEY'] = 'Bearer'
# Configure API key authorization: systemName
configuration = gu_rest_api.Configuration()
configuration.api_key['X-GU-APPNAME'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-GU-APPNAME'] = 'Bearer'

# create an instance of the API class
api_instance = gu_rest_api.PeerApi(gu_rest_api.ApiClient(configuration))
node_id = 'node_id_example' # str | GU Network node identifier
peer_session_spec = gu_rest_api.PeerSessionSpec() # PeerSessionSpec | 

try:
    api_response = api_instance.create_deployment_on_peer(node_id, peer_session_spec)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PeerApi->create_deployment_on_peer: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *http://127.0.0.1:61622*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*PeerApi* | [**create_deployment_on_peer**](docs/PeerApi.md#create_deployment_on_peer) | **POST** /peers/{nodeId}/deployments | 
*PeerApi* | [**get_peer_details**](docs/PeerApi.md#get_peer_details) | **GET** /peers/{nodeId} | Returns detailed peer info
*PeerApi* | [**list_peer_deployments**](docs/PeerApi.md#list_peer_deployments) | **GET** /peers/{nodeId}/deployments | 
*PeerApi* | [**list_peers**](docs/PeerApi.md#list_peers) | **GET** /peers | Returns a list hub peers.
*SessionApi* | [**add_hub_session_peers**](docs/SessionApi.md#add_hub_session_peers) | **POST** /sessions/{sessionId}/peers | Manually adds peers to hub session
*SessionApi* | [**create_blob**](docs/SessionApi.md#create_blob) | **POST** /sessions/{sessionId}/blobs | Creates new lob
*SessionApi* | [**create_hub_session**](docs/SessionApi.md#create_hub_session) | **POST** /sessions | Creates new hub session.
*SessionApi* | [**create_peer_session**](docs/SessionApi.md#create_peer_session) | **POST** /sessions/{sessionId}/peers/{nodeId}/deployments | Creates new deploymnet
*SessionApi* | [**delete_hub_session**](docs/SessionApi.md#delete_hub_session) | **DELETE** /sessions/{sessionId} | 
*SessionApi* | [**delete_peer_session**](docs/SessionApi.md#delete_peer_session) | **DELETE** /sessions/{sessionId}/peers/{nodeId}/deployments/{deploymentId} | 
*SessionApi* | [**download_blob**](docs/SessionApi.md#download_blob) | **GET** /sessions/{sessionId}/blobs/{blobId} | Downloads binary content from the hub
*SessionApi* | [**get_hub_session**](docs/SessionApi.md#get_hub_session) | **GET** /sessions/{sessionId} | Gets hub session info
*SessionApi* | [**get_hub_session_config**](docs/SessionApi.md#get_hub_session_config) | **GET** /sessions/{sessionId}/config | Gets configuration from stash
*SessionApi* | [**list_hub_session_blobs**](docs/SessionApi.md#list_hub_session_blobs) | **GET** /sessions/{sessionId}/blobs | Lists currently allocated lobs
*SessionApi* | [**list_hub_sessions**](docs/SessionApi.md#list_hub_sessions) | **GET** /sessions | Lists current hub sessions.
*SessionApi* | [**sessions_session_id_patch**](docs/SessionApi.md#sessions_session_id_patch) | **PATCH** /sessions/{sessionId} | Hub session update
*SessionApi* | [**set_hub_session_config**](docs/SessionApi.md#set_hub_session_config) | **PUT** /sessions/{sessionId}/config | Sets configuration stash
*SessionApi* | [**update_peer_session**](docs/SessionApi.md#update_peer_session) | **PATCH** /sessions/{sessionId}/peers/{nodeId}/deployments/{deploymentId} | Sends multiple commands for peer
*SessionApi* | [**upload_blob**](docs/SessionApi.md#upload_blob) | **PUT** /sessions/{sessionId}/blobs/{blobId} | Uploads a binary content to the hub.


## Documentation For Models

 - [BlobInfo](docs/BlobInfo.md)
 - [Command](docs/Command.md)
 - [ConfigStash](docs/ConfigStash.md)
 - [DeploymentInfo](docs/DeploymentInfo.md)
 - [DeploymentStatus](docs/DeploymentStatus.md)
 - [DownloadFileCommand](docs/DownloadFileCommand.md)
 - [EnvType](docs/EnvType.md)
 - [ExecCommand](docs/ExecCommand.md)
 - [HubSession](docs/HubSession.md)
 - [HubSessionCommand](docs/HubSessionCommand.md)
 - [HubSessionTouchCommand](docs/HubSessionTouchCommand.md)
 - [PeerDetails](docs/PeerDetails.md)
 - [PeerInfo](docs/PeerInfo.md)
 - [PeerSessionSpec](docs/PeerSessionSpec.md)
 - [PeerSessionSpecImage](docs/PeerSessionSpecImage.md)
 - [ProcessCollection](docs/ProcessCollection.md)
 - [ProcessInfo](docs/ProcessInfo.md)
 - [StartCommand](docs/StartCommand.md)
 - [StopCommand](docs/StopCommand.md)
 - [UploadFileCommand](docs/UploadFileCommand.md)


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




