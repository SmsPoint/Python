# com.nvt.celman.DefaultApi

All URIs are relative to *http://localhost:9003/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**sms_send**](DefaultApi.md#sms_send) | **POST** /sms/send | Send a text message request.


# **sms_send**
> SmsSendResponse sms_send(sms_send_request)

Send a text message request.

### Example

* Api Key Authentication (ApiKeyAuth):
```python
import time
import com.nvt.celman
from com.nvt.celman.api import default_api
from com.nvt.celman.model.sms_send_response import SmsSendResponse
from com.nvt.celman.model.sms_send_request import SmsSendRequest
from pprint import pprint
# Defining the host is optional and defaults to http://localhost:9003/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = com.nvt.celman.Configuration(
    host = "http://localhost:9003/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = 'YOUR_API_KEY'

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Enter a context with an instance of the API client
with com.nvt.celman.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    sms_send_request = SmsSendRequest(
        sender_name="sender_name_example",
        body="body_example",
        phone="phone_example",
        source="source_example",
    ) # SmsSendRequest | 

    # example passing only required values which don't have defaults set
    try:
        # Send a text message request.
        api_response = api_instance.sms_send(sms_send_request)
        pprint(api_response)
    except com.nvt.celman.ApiException as e:
        print("Exception when calling DefaultApi->sms_send: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_send_request** | [**SmsSendRequest**](SmsSendRequest.md)|  |

### Return type

[**SmsSendResponse**](SmsSendResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**0** | A response to a text message send request. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

