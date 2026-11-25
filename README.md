# Meeting.ai for Antigravity

Meeting.ai takes the notes in every meeting, in person or on Zoom, Google Meet, and Microsoft
Teams. Antigravity builds from what was said.

## From a meeting to your work

> "Read my last planning meeting and draft the implementation plan for this project."

> "We agreed to change the retry limit to 5. Find where we decided that, and make the change."

> "Make a task list from the action items of today's standup, with the owners."

## Before and during a meeting

> "Before the sync, find what we decided about this feature in my past meetings."

> "Send the Meeting.ai notetaker to my Google Meet and take notes."

> "Turn the design review into a one-page Visual Note that I can share."

## What it can reach

- Only your Meeting.ai account: the meetings, notes, transcripts, contacts and Drive files in
  the workspaces that you belong to.
- Antigravity acts as you. It cannot do more than your own Meeting.ai account can do in those
  workspaces.
- It writes only when you ask it to. You can end the connection at any time in Meeting.ai,
  under **Settings › MCP & CLI**.

## How to start

1. Add the plugin. In the Antigravity App, open **Customizations › Marketplace**, find
   **Meeting.ai**, and click **Add**. In the Antigravity CLI, run
   `agy plugin install meeting-ai@antigravity-plugins-partners`.
2. Sign in. The first time Antigravity uses a Meeting.ai tool, your browser opens the
   Meeting.ai sign-in page. Sign in and click **Allow access**. There is no API key to paste.
3. Ask in plain words.

You need a Meeting.ai account. You can start free at [meeting.ai](https://meeting.ai).

## What is in this plugin

| Part | What it does |
|---|---|
| MCP server `meeting-ai` | Connects Antigravity to the hosted Meeting.ai server, `https://mcp.meeting.ai/mcp`. |
| Skill `meeting-ai-overview` | How to read meetings, notes, transcripts and action items, recap several meetings, and use exports, sharing, tags, contacts, Drive and workspaces. |
| Skill `meeting-ai-setup` | How to turn on the plugin, sign in, check that the connection works, and fix sign-in problems. |
| Skill `meeting-ai-record-meeting` | How to send the notetaker to a Zoom, Google Meet or Microsoft Teams call, transcribe a recording, follow the progress, and stop a recording. |
| Skill `meeting-ai-edit-notes` | How to rewrite or restructure the notes of a meeting and rename it. Only the meeting owner can edit. |
| Skill `meeting-ai-visual-notes` | How to make a Visual Note, a one-page summary image, from one meeting, several meetings, or any text. |

The plugin is configuration and instructions only. It has no code, no binary, and no hooks.

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
