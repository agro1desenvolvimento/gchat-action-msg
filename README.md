# Google Chat Build Message Action

This GitHub Action sends build status notifications to Google Chat.

## Inputs

| Name         | Description               | Required |
|--------------|---------------------------|----------|
| `webhook-url`| Google Chat webhook URL  | Yes      |
| `name`       | Name of the build        | Yes      |

## Usage Example

Create a new webhook in Google Chat and add the URL to your repository secrets.

```yaml
      (...)
      - name: Notify Google Chat
        uses: ./.github/actions/gchat-action-msg
        with:
          webhook-url: ${{ GOOGLECHAT_WEBHOOK_BUILD_URL }}
          name: "Message Title"
      (...)
```

