# lsf_client
LSF Web Service

This Python package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0
- Package version: 1.0.0
- Generator version: 7.6.0-SNAPSHOT
- Build package: org.openapitools.codegen.languages.PythonClientCodegen

## Requirements.

Python 3.7+

## Installation & Usage
### pip install

If the python package is hosted on a repository, you can install directly using:

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import lsf_client
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import lsf_client
```

### Tests

Execute `pytest` to run the tests.

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python

import lsf_client
from lsf_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:8088/lsf
# See configuration.py for a list of all supported configuration parameters.
configuration = lsf_client.Configuration(
    host = "http://localhost:8088/lsf"
)



# Enter a context with an instance of the API client
with lsf_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = lsf_client.AuthenticationApi(api_client)
    user = lsf_client.User() # User |  (optional)

    try:
        # User log on
        api_response = api_instance.logon(user=user)
        print("The response of AuthenticationApi->logon:\n")
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling AuthenticationApi->logon: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost:8088/lsf*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthenticationApi* | [**logon**](docs/AuthenticationApi.md#logon) | **POST** /v1/auth/logon | User log on
*AuthenticationApi* | [**logout**](docs/AuthenticationApi.md#logout) | **POST** /v1/auth/logout | User log off
*FileOperationsApi* | [**delete**](docs/FileOperationsApi.md#delete) | **DELETE** /v1/files/{filePath} | Delete file by a specific path
*FileOperationsApi* | [**download**](docs/FileOperationsApi.md#download) | **GET** /v1/files/{filePath} | Download a single file
*FileOperationsApi* | [**file_tree**](docs/FileOperationsApi.md#file_tree) | **GET** /v1/files | List file under a specific path
*FileOperationsApi* | [**list_repos**](docs/FileOperationsApi.md#list_repos) | **GET** /v1/repos | List repositories
*FileOperationsApi* | [**upload**](docs/FileOperationsApi.md#upload) | **POST** /v1/files | Upload a single file
*LSFClusterApi* | [**execute_lsf_cli**](docs/LSFClusterApi.md#execute_lsf_cli) | **POST** /v1/cluster/usercmd | Execute LSF command
*LSFClusterApi* | [**get_cluster_info**](docs/LSFClusterApi.md#get_cluster_info) | **GET** /v1/cluster | Get LSF cluster information
*PingApi* | [**ping**](docs/PingApi.md#ping) | **GET** /v1/ping | Ping service


## Documentation For Models

 - [Error](docs/Error.md)
 - [ErrorMessage](docs/ErrorMessage.md)
 - [LSFCLIResult](docs/LSFCLIResult.md)
 - [LSFCluster](docs/LSFCluster.md)
 - [Repositories](docs/Repositories.md)
 - [RepositoryBean](docs/RepositoryBean.md)
 - [ReturnMessage](docs/ReturnMessage.md)
 - [Session](docs/Session.md)
 - [TreeNode](docs/TreeNode.md)
 - [User](docs/User.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization


Authentication schemes defined for the API:
<a id="LSF-Web-Service-authentication"></a>
### LSF-Web-Service-authentication

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Author




