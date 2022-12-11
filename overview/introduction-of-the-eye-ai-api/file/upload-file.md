---
cover: ../../../.gitbook/assets/GITHUB.png
coverY: 0
---

# ▪ Upload File

_Upload a file that contains document(s) to be used across various endpoints/features. Currently, the size of all the files uploaded by one organization can be up to 1 GB. Please contact us if you need to increase the storage limit._

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/files \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -F purpose="fine-tune" \
  -F file='@mydata.jsonl'
}
```
{% endcode %}

{% code title="Response " lineNumbers="true" %}
```
{
  "id": "file-XjGxS3KTG0uNmNOK362iJua3",
  "object": "file",
  "bytes": 140,
  "created_at": 1613779121,
  "filename": "mydata.jsonl",
  "purpose": "fine-tune"
}

```
{% endcode %}
