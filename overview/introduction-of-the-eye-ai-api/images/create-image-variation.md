---
cover: ../../../.gitbook/assets/GITHUBCAPA.png
coverY: 0
---

# ▪ Create image variation

#### Creates a variation of a given image.

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/images/variations \
  -H 'Authorization: Bearer YOUR_API_KEY' \
  -F image='@otter.png' \
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
