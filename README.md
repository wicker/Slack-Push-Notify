# Slack-Push-Notify
Slack app that notifies about git pushes.

## Design Notes

Using the [Slack Apps docs](https://api.slack.com/slack-apps).

Created the app called `Push-Notify` on my workspace. For now, this will just be private to my workspace. 

Features: 

- Uses as incoming webhook

Future: 

- Richly format the message
- Supports slash commands
- Add OAuth support

### Incoming Webhooks

The app will look for a post-commit git webhook in the related repo, which is this one, for now. Webhooks are regular HTTP requests with a JSON payload. 

Flipped the right switches in the Slack API. These are great docs so far...

Added a webhook to my workspace and tried the example: 

```
curl -X POST -H 'Content-type: application/json' --data '{"text":"Hello, World!"}' <hook url here>
```

![Hello World webhook screenshot](hello-world-webhook.png)




