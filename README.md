<p align="center">
  <a href="https://meeting.ai" target="_blank" rel="noopener noreferrer">
    <img width="64" src="assets/logo.png" alt="Meeting.ai logo">
  </a>
</p>
<h1 align="center">
  Meeting.ai for Antigravity
</h1>
<h3 align="center">
  Bring your meetings into Antigravity
</h3>
<p align="center">
  Meeting.ai takes the notes in every meeting, in person or on Zoom, Google Meet, and Microsoft Teams.<br/>
  Antigravity builds from what was said.
</p>

## Overview

The Meeting.ai plugin connects Antigravity to your Meeting.ai account. Find what was decided,
read notes and transcripts, and turn a meeting into a plan, a task list, or code, without
leaving your project.

The plugin uses [Meeting.ai's hosted MCP server](https://meeting.ai/en/docs/developers/connect-meeting-ai).
Sign in with your Meeting.ai account to get started. No API key or local server is required.

## Quick start

### 1. Install from the marketplace

Open **Customizations → Marketplace** in Antigravity, find **Meeting.ai**, and click **Add**.

### 2. Connect your Meeting.ai account

**Installing the plugin is the first step. Connect your account before using Meeting.ai tools.**

1. Open **Customizations → Installed** and open **Meeting.ai**.
2. Open the **Accounts** tab and click **Sign in**.
3. Sign in to Meeting.ai in your browser and click **Allow access**.

Antigravity then shows the account as **Connected**. If you do not have a Meeting.ai account
yet, you can start free at [meeting.ai](https://meeting.ai).

### 3. Try it out

Ask Antigravity:

> Summarize the decisions and action items from my last meeting.

Once Antigravity retrieves your meeting from Meeting.ai, you're connected. You can also try:

- Read my last planning meeting and draft the implementation plan for this project.
- We agreed to change the retry limit to 5. Find where we decided that, and make the change.
- Before the sync, find what we decided about this feature in my past meetings.
- Send the Meeting.ai notetaker to my Google Meet and take notes.
- Turn the design review into a one-page Visual Note that I can share.

## What it can reach

- Only your Meeting.ai account: the meetings, notes, transcripts, contacts and Drive files in
  the workspaces that you belong to.
- Antigravity acts as you. It cannot do more than your own Meeting.ai account can do in those
  workspaces.
- It writes only when you ask it to. You can end the connection at any time in Meeting.ai,
  under **Settings › MCP & CLI**.

## Before you install

- **Your data goes to Meeting.ai.** Every tool call goes to Meeting.ai's hosted server and acts
  on your Meeting.ai account, with your own role in each workspace.
- **Some actions use Coins.** Recording, Visual Notes, and image and audio generation use your
  Meeting.ai Coins, the usage credits that come with a Meeting.ai plan or a Coin pack. If your
  account has no Coins, the tool stops with a clear message. An export costs no Coins and saves
  a file to your Meeting.ai Drive.
- **A long generation can continue after the agent's reply.** It can be charged, and Meeting.ai
  saves the file to your Drive when it is ready.
- **Generation uses third-party AI providers.** Visual Note, image and audio generation send
  the text you supply to them.
- **Meeting.ai records each tool call** (tool, outcome, and user, workspace and client
  identifiers) for product analytics. The plugin itself sends no telemetry.
- **The notetaker is visible.** It joins a live call as a participant named Meeting.ai.
- **A share link is public.** It shows the notes and, by default, the transcript. It has a PIN
  by default.

## Troubleshooting

### Installed, but Meeting.ai tools are unavailable

Check that the plugin is enabled, then open its **Accounts** tab and sign in. Installation does
not sign you in automatically. Start a new conversation after you sign in.

### A tool says that you are out of Coins

Nothing is wrong with the connection. Recording, Visual Notes, and image and audio generation
use Meeting.ai Coins. See [Coins and billing](https://meeting.ai/en/docs/billing/coins-and-billing).

### The connection stopped working

Open the plugin's **Accounts** tab, sign out, and sign in again. For more help, see
[Connect Meeting.ai through MCP](https://meeting.ai/en/docs/developers/connect-meeting-ai) or
write to support@meeting.ai.

## Links

- [Connect Meeting.ai through MCP](https://meeting.ai/en/docs/developers/connect-meeting-ai)
- [Meeting.ai docs](https://meeting.ai/en/docs)
- [Coins and billing](https://meeting.ai/en/docs/billing/coins-and-billing)
- [Privacy policy](https://meeting.ai/privacy)
- [Terms of service](https://meeting.ai/terms)
- Support: support@meeting.ai

## License

Apache-2.0. See [LICENSE](LICENSE) and [NOTICE](NOTICE). The Meeting.ai name, logo and artwork
are trademarks of Meeting.ai and are not licensed under the Apache License.
