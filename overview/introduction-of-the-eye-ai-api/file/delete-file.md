---
cover: ../../../.gitbook/assets/GITHUB.png
coverY: 0
---

# ▪ Delete File

#### Delete a file.

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/files/file-XjGxS3KTG0uNmNOK362iJua3 \
  -X DELETE \
  -H 'Authorization: Bearer YOUR_API_KEY'
}
```
{% endcode %}

{% code title="Response" lineNumbers="true" %}
```
{
  "id": "file-XjGxS3KTG0uNmNOK362iJua3",
  "object": "file",
  "deleted": true
}

```
{% endcode %}

\
