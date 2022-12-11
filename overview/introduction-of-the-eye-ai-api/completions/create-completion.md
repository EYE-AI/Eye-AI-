---
cover: ../../../.gitbook/assets/GITHUB.png
coverY: 0
---

# ▪ Create completion

_Creates a completion for the provided prompt and parameters_

{% code title="Example request" lineNumbers="true" %}
```ada
curl https://api.eye-ai.com/v1/completions \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer YOUR_API_KEY' \
  -d '{
  "model": "text-ada-001",
  "prompt": "Say this is a test",
  "max_tokens": 7,
  "temperature": 0
}
```
{% endcode %}

\
