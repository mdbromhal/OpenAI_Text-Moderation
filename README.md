# OpenAI_Text-Moderation
ABSTRACT: Analyzing how OpenAI moderates text

Source: https://github.com/malywut/gpt_examples

**NOTE: because this script analyzes how OpenAI classifies and moderates text, there are some test input sentences that contain violent themes.**

1. Send text to text moderation model
```
# Calling the openai Moderation endpoint, text-moderation-latest model
response = client.moderations.create(model='text-moderation-latest',
input = "I want to hurt my neighbor")
```
2. Analyzing the response
   - I use a bar and pie plot to analyze the percentage scores from the categorical scores in the responses
   - I also check the flag to see if the input text is considered inappropriate and moderated by OpenAI
