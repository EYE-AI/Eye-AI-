---
cover: ../../../.gitbook/assets/GITHUB.png
coverY: 0
---

# 🧿 File

#### List files

_Returns a list of files that belong to the user's organization._

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/files \
  -H 'Authorization: Bearer YOUR_API_KEY'
```
{% endcode %}

{% code title="Response" lineNumbers="true" %}
```
{
  "data": [
    {
      "id": "file-ccdDZrC3iZVNiQVeEA6Z66wf",
      "object": "file",
      "bytes": 175,
      "created_at": 1613677385,
      "filename": "train.jsonl",
      "purpose": "search"
    },
    {
      "id": "file-XjGxS3KTG0uNmNOK362iJua3",
      "object": "file",
      "bytes": 140,
      "created_at": 1613779121,
      "filename": "puppy.jsonl",
      "purpose": "search"
    }
  ],
  "object": "list"
}
```
{% endcode %}

\
