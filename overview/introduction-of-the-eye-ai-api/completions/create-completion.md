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

{% code title="Parameters" lineNumbers="true" %}
```ada
{
  "model": "text-ada-001",
  "prompt": "Say this is a test",
  "max_tokens": 7,
  "temperature": 0,
  "top_p": 1,
  "n": 1,
  "stream": false,
  "logprobs": null,
  "stop": "\n"
}
```
{% endcode %}

{% code title="Response" lineNumbers="true" %}
```ada
{
  "id": "cmpl-uqkvlQyYK7bGYrRHQ0eXlWi7",
  "object": "text_completion",
  "created": 1589478378,
  "model": "text-ada-001",
  "choices": [
    {
      "text": "\n\nThis is indeed a test",
      "index": 0,
      "logprobs": null,
      "finish_reason": "length"
    }
  ],
  "usage": {
    "prompt_tokens": 5,
    "completion_tokens": 7,
    "total_tokens": 12
  }
}
```
{% endcode %}

\
