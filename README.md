<div align="center">
	<p>
	<img alt="Thoughtworks Logo" src="https://raw.githubusercontent.com/ThoughtWorks-DPS/static/master/thoughtworks_flamingo_wave.png?sanitize=true" width=200 /><br />
	<img alt="DPS Title" src="https://raw.githubusercontent.com/ThoughtWorks-DPS/static/master/EMPCPlatformStarterKitsImage.png?sanitize=true" width=350/><br />
	<h2>common-actions</h2>
	<img alt="GitHub Actions Workflow Status" src="https://img.shields.io/github/actions/workflow/status/ThoughtWorks-DPS/common-actions/.github%2Fworkflows%2Fdevelopment-build.yaml"> <img alt="GitHub Release" src="https://img.shields.io/github/v/release/ThoughtWorks-DPS/common-actions"> <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-blue.svg"></a>
	</p>
</div>

Example of collection of common pipeline actions. These are actions useful within any sort of pipeline and can be bundled in a collection to incorporate team or org specific configurations.  

### /slack-bot

Post messages using the https://slack.com/api/chat.postMessage API resource.  

```yaml
- name: Post success message to slack channel
  uses: ThoughtWorks-DPS/common-actions/slack-bot@v0.1.0
  with:
    channel: lab-events
    message: Successful use of common-actions/slack-bot
    custom-message: ""        # use this field to completely override json body
    include-link: "false"     # include link to action the sent message
    include-tag: "false"      # include git tag with standard message
```

###  /gren

Create github release on current tag using github-release-notes.    

```yaml
- name: Generate release notes
  uses: ThoughtWorks-DPS/common-actions/gren@v0.2.0
  with:
    gren-additional-args: ""  # include addiitonal gren command line arguments
```
