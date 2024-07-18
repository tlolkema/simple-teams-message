# Simple Teams Message

Microsoft Teams phased out the incoming Office365 webhook connector. This action allows you to send a message to a Teams channel using the new workflows process.

## Examples

> Simple message

<img src="https://github.com/tlolkema/simple-teams-message/blob/main/assets/simple.png?raw=true" width="400"/>

> With image and extra text blocks

<img src="https://github.com/tlolkema/simple-teams-message/blob/main/assets/complex.png?raw=true" width="400"/>

## How to use in your GitHub workflow

Add the following to your workflow file:

```yaml
- uses: tlolkema/simple-teams-message@main
  with:
    message_title: "Test Message"
    message_description: "Test"
    webhook: ${{ secrets.TEAMS_WEBHOOK }}
```

You can add the following optional parameters:

```yaml
image_url: "https://example.com/path/to/your/image.jpg"
extra_text_blocks: "This is an extra block|||This is another extra block"
```

## How to configure the workflow in MS Teams

1. Go to workflow menu

![workflow](https://github.com/tlolkema/simple-teams-message/blob/main/assets/workflows.png?raw=true)

2. Create a new workflow
3. Use: `"Post to a channel when a webhook request is received"`
4. Add workflow
5. Go to workflow menu
6. Edit the workflow

![edit](https://github.com/tlolkema/simple-teams-message/blob/main/assets/edit.png?raw=true)

7. Change the user `Post as` to User, `Post in` to Channel, and select a valid Team and Channel

![edit-workflow](https://github.com/tlolkema/simple-teams-message/blob/main/assets/edit-workflow.png?raw=true)

8. Success! Your workflow is now ready to receive messages from GitHub
