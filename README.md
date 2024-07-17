# simple-teams-message

Microsoft Teams phased out the incoming webhook connector. This action allows you to send a message to a Teams channel using the new workflows process.

## How to use in your GitHub workflow

Add the following to your workflow file:

```yaml
- uses: tlolkema/simple-teams-message@main
  with:
    message_title: "Test Message"
    message_description: "Test"
    webhook: ${{ secrets.TEAMS_WEBHOOK }}
```

## How to configure the workflow in MS Teams

1. Create a new workflow in your Teams channel
2. Use: `"Post to a channel when a webhook request is received"`
3. Next
4. Add workflow
5. Go to workflow menu

![workflow](https://github.com/tlolkema/simple-teams-message/blob/main/assets/workflows.png?raw=true)

6. Edit the workflow

![edit](https://github.com/tlolkema/simple-teams-message/blob/main/assets/edit.png?raw=true)

7. Change the user `Post as` to User, `Post in` to Channel, and select a valid Team and Channel

![edit-workflow](https://github.com/tlolkema/simple-teams-message/blob/main/assets/edit-workflow.png?raw=true)

8. Success! Your workflow is now ready to receive messages from GitHub
