---
cover: ../../../.gitbook/assets/GITHUBCAPA.png
coverY: 0
---

# ▪ Create image edit

#### Creates an edited or extended image given an original image and a prompt.

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/images/edits \
  -H 'Authorization: Bearer YOUR_API_KEY' \
  -F image='@otter.png' \
  -F mask='@mask.png' \
  -F prompt="A cute baby sea otter wearing a beret" \
  -F n=2 \
  -F size="1024x1024"
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
