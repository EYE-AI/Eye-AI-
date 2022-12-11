---
cover: ../../.gitbook/assets/GITHUB.png
coverY: 0
---

# 👁 Introduction of the Eye- AI API

#### _Authentication_

_The Eye AI API uses API keys for authentication. Visit the_ [_API Keys_](making-requests.md) _page to retrieve the API key you will use in your requests._

_Remember that your API key is a secret! Do not share it with others or expose it in any client-side code (browsers, applications). Production requests should be routed through your own back-end server, where your API key can be loaded securely from an environment variable or key management service._

#### _All API requests must include your API key in an Authorization HTTP header as follows:_

```
Authorization: Bearer YOUR_API_KEY
```

_Requesting Organization For users who belong to multiple organizations, you can pass a header to specify which organization is used for an API request. The usage of these API requests will be counted in the subscription quota of the specified organization._

#### _**Example curl command:**_

{% code lineNumbers="true" %}
```
Curl https://api.eye-ai.com/v1/models \
-H 'Authorization: Bearer YOUR_API_KEY' \
-H 'eye-ai-Organization: YOUR_ORG_ID'
```
{% endcode %}

#### _Example with the Eye-AI Python package:_

{% code lineNumbers="true" %}
```python
import os
import Eye-AI
Eye-AI.organization = "YOUR_ORG_ID"
Eye-AI.api_key = os.getenv("Eye-AI_API_KEY")
Eye-AI.Model.list()
```
{% endcode %}

#### _Example with the Eye-AI Node.js package:_

{% code lineNumbers="true" %}
```javascript
import { Configuration, eYE-ai-API} from "eye-ai";
const configuration = new Configuration({
    organization: "YOUR_ORG_ID",
    apiKey: process.env.EYE-AI_API_KEY,
});
const eye-ai  = new Eye-AI-Api(configuration);
const response = await Eye-AI.listEngines();
```
{% endcode %}

