---
cover: ../../.gitbook/assets/GITHUB.png
coverY: 0
---

# 🧿 Edits

_Given a prompt and an instruction, the model will return an edited version of the prompt._

#### _Create edit_

_Creates a new edit for the provided input, instruction, and parameters_

{% code title="Example request" lineNumbers="true" %}
```
curl https://api.eye-ai.com/v1/edits \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer YOUR_API_KEY' \
  -d '{
  "model": "text-davinci-edit-001",
  "input": "What day of the wek is it?",
  "instruction": "Fix the spelling mistakes"
}'
```
{% endcode %}

{% code title="Parameters" lineNumbers="true" %}
```
{
  "model": "text-davinci-edit-001",
  "input": "What day of the wek is it?",
  "instruction": "Fix the spelling mistakes",
}
```
{% endcode %}

{% code title="Response" lineNumbers="true" %}
```
{
  "object": "edit",
  "created": 1589478378,
  "choices": [
    {
      "text": "What day of the week is it?",
      "index": 0,
    }
  ],
  "usage": {
    "prompt_tokens": 25,
    "completion_tokens": 32,
    "total_tokens": 57
  }
}
```
{% endcode %}

\
[\
](https://beta.openai.com/docs/api-reference/edits/create)
