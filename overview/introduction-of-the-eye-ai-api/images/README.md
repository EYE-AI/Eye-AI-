---
cover: ../../../.gitbook/assets/GITHUB.png
coverY: 0
---

# 🧿 Images

_Given a prompt and/or an input image, the model will generate a new image._

#### Create image

_Creates an image given a prompt._

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/images/generations \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer YOUR_API_KEY' \
  -d '{
  "prompt": "A cute baby sea otter",
  "n": 2,
  "size": "1024x1024"
}'
```
{% endcode %}

{% code title="Parameters" lineNumbers="true" %}
```
{
  "prompt": "A cute baby sea otter",
  "n": 2,
  "size": "1024x1024"
}
```
{% endcode %}

{% code title="Response" lineNumbers="true" %}
```
{
  "created": 1589478378,
  "data": [
    {
      "url": "https://..."
    },
    {
      "url": "https://..."
    }
  ]
}
```
{% endcode %}

\
\
