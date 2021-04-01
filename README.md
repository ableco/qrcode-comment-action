# QRCode Comment

A GitHub Action to create a comment with a QR code in the PR.

## Usage

### Create Workflow

Create a workflow (eg: `.github/workflows/comment.yml` see [Creating a Workflow file](https://help.github.com/en/articles/configuring-a-workflow#creating-a-workflow-file)) to utilize the qrcode action with content:

```yaml
name: "Review App QR Code"
on:
  - pull_request

jobs:
  triage:
    runs-on: ubuntu-latest
    steps:
      # …
      - uses: ableco/qrcode-comment-action@main
        with:
          content: ${{ steps.deploy.outputs.review_url }}
          comment: |
            {qrcode}
```


## Contributing

Contributions are welcome. Please check out the [Contributing guide](CONTRIBUTING.md) for the guidelines you need to follow.

Please read our [Code of Conduct](CODE_OF_CONDUCT.md) so that you can understand the kind of respectful behavior we expect of all participants.

## License

Open Source Project is released under the MIT license. See [LICENSE](LICENSE) for the full license text.
