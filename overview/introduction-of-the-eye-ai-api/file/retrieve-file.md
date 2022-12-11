---
cover: ../../../.gitbook/assets/GITHUB.png
coverY: 0
---

# ▪ Retrieve file

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/files/file-XjGxS3KTG0uNmNOK362iJua3 \
  -H 'Authorization: Bearer YOUR_API_KEY'
}
```
{% endcode %}

{% code title="Response" lineNumbers="true" %}
```
{
  "id": "file-XjGxS3KTG0uNmNOK362iJua3",
  "object": "file",
  "bytes": 140,
  "created_at": 1613779657,
  "filename": "mydata.jsonl",
  "purpose": "fine-tune"
}
```
{% endcode %}
