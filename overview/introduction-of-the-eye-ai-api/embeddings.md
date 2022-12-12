---
cover: ../../.gitbook/assets/GITHUB.png
coverY: 0
---

# 🧿 Embeddings

_Get a vector representation of a given input that can be easily consumed by machine learning models and algorithms._

#### _Create embeddings_

_Creates an embedding vector representing the input text._

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/embeddings \
  -X POST \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"input": "The food was delicious and the waiter...",
       "model": "text-similarity-babbage-001"}'

```
{% endcode %}

{% code title="Parameters" lineNumbers="true" %}
```
{
  "model": "text-similarity-babbage-001",
  "input": "The food was delicious and the waiter..."
}

```
{% endcode %}

{% code title="Response" lineNumbers="true" %}
```
{
  "object": "list",
  "data": [
    {
      "object": "embedding",
      "embedding": [
        0.018990106880664825,
        -0.0073809814639389515,
        .... (1024 floats total for ada)
        0.021276434883475304,
      ],
      "index": 0
    }
  ],
  "usage": {
    "prompt_tokens": 8,
    "total_tokens": 8
  }
}

```
{% endcode %}

\
\
