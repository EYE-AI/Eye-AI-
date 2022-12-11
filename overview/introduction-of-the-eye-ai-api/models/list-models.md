---
cover: ../../../.gitbook/assets/GITHUB.png
coverY: 0
---

# ▪ List models

_Lists the currently available models, and provides basic information about each one such as the owner and availability._

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/models \
  -H 'Authorization: Bearer YOUR_API_KEY'
```
{% endcode %}

{% code title="Response" lineNumbers="true" %}
```
{
  "data": [
    {
      "id": "model-id-0",
      "object": "model",
      "owned_by": "organization-owner",
      "permission": [...]
    },
    {
      "id": "model-id-1",
      "object": "model",
      "owned_by": "organization-owner",
      "permission": [...]
    },
    {
      "id": "model-id-2",
      "object": "model",
      "owned_by": "eye-ai",
      "permission": [...]
    },
  ],
  "object": "list"
}
```
{% endcode %}

#### _Retrieve model_

_Retrieves a model instance, providing basic information about the model such as the owner and permissioning._

{% code title="Example request" lineNumbers="true" %}
```ada
curl https://api.eye-ai.com/v1/models/text-ada-001 \
  -H 'Authorization: Bearer YOUR_API_KEY'
```
{% endcode %}

#### Path parameters

_The ID of the model to use for this request_

{% code title="Response" lineNumbers="true" %}
```ada
{
  "id": "text-ada-001",
  "object": "model",
  "owned_by": "eye-ai",
  "permission": [...]
}
```
{% endcode %}

\
\
