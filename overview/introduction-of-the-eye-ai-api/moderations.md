---
cover: ../../.gitbook/assets/GITHUBCAPA.png
coverY: 0
---

# 🧿 Moderations

#### _Given a input text, outputs if the model classifies it as violating Eye-ai content policy._

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/moderations \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer YOUR_API_KEY' \
  -d '{
  "input": "I want to kill them."
}'
```
{% endcode %}

{% code title="Parameters" lineNumbers="true" %}
```
{
  "input": "I want to kill them."
}
```
{% endcode %}

{% code title="Response" lineNumbers="true" %}
```
{
  "id": "modr-5MWoLO",
  "model": "text-moderation-001",
  "results": [
    {
      "categories": {
        "hate": false,
        "hate/threatening": true,
        "self-harm": false,
        "sexual": false,
        "sexual/minors": false,
        "violence": true,
        "violence/graphic": false
      },
      "category_scores": {
        "hate": 0.22714105248451233,
        "hate/threatening": 0.4132447838783264,
        "self-harm": 0.005232391878962517,
        "sexual": 0.01407341007143259,
        "sexual/minors": 0.0038522258400917053,
        "violence": 0.9223177433013916,
        "violence/graphic": 0.036865197122097015
      },
      "flagged": true
    }
  ]
}
```
{% endcode %}

\
