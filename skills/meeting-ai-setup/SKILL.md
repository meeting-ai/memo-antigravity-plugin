---
name: meeting-ai-setup
description: Use when Meeting.ai tools are not available in this session, the user wants to connect Meeting.ai, is asked to sign in or authorize, sees an authentication error from a meeting-ai tool, or asks how to switch the workspace the connection uses. Walks through turning on the plugin, signing in, and checking that it works.
compatibility: Requires the Meeting.ai MCP server (https://mcp.meeting.ai/mcp)
---

# Connect Meeting.ai

The other Meeting.ai skills call tools from a hosted MCP server. This plugin adds that server
for you. You do not need to change a configuration file.

| Server detail | Value |
|---|---|
| URL | `https://mcp.meeting.ai/mcp` |
| Transport | Streamable HTTP |
| Sign-in | Browser sign-in with a Meeting.ai account. No API key. |

Antigravity shows the tools with the prefix `meeting-ai_meeting-ai`.

## Check the connection first

If `workspace_list` is available, call it. A reply with at least one workspace means the
connection works. Tell the user which workspace is active and stop here.

If the tool is available but returns an authentication error, go to **Sign in**.

If the tool is not available, the plugin is not enabled or the user has not signed in. Go to
**Turn on the plugin**. Do not guess or invent meeting data while the server is not connected.

## Turn on the plugin

- **Antigravity App:** the user opens **Customizations › Installed** and checks that
  Meeting.ai is on. A plugin that shows "Sign in required" needs the sign-in below.
- **Antigravity CLI:** the user runs `/plugin`, opens the **Installed** tab, and checks that
  `meeting-ai` is enabled. `agy plugin enable meeting-ai` does the same from the shell.

Most sessions load a plugin's server only when the session starts. Tell the user to start a new
session if the tools do not appear.

## Sign in

1. A browser window opens on `auth.meeting.ai` when the Meeting.ai server connects. The
   approval page names Google Antigravity as the app that asks for access.
2. The user signs in with the same account they use for the Meeting.ai web or mobile app, then
   approves the connection. Never ask for a password, API key, or token in chat.
3. Call `workspace_list` and identify the active workspace. Installed does not mean
   authenticated. Do not say the account is connected until this call succeeds.

If the user has no Meeting.ai account yet, they can create one at https://meeting.ai. A new
account has no meetings, so suggest recording one with `meetings_create` or uploading a
recording in the web app before exploring.

## Workspace and access

Use `workspace_list` to show available workspaces. Use `workspace_set_active` only when the
user wants to change this connection's default. This changes only this connection and never
moves any data. Use `workspace_id` for a one-off call. `media_image_gen`, `media_audio_gen`, and
`recipe_visual_note` do not accept it: they always save to the active workspace.

## Common problems

- **Authentication error on a tool call.** The session was revoked or expired. Ask the user to
  sign in again through the agent's reconnect control. Do not retry the tool until they have.
- **The sign-in never starts.** Report the connection error. Changing a password or buying a
  plan does not fix this.
- **The browser did not open.** Many agents print the authorization URL. The user can open it
  by hand on the same machine.
- **A tool returns an error about coins, balance, subscription, or storage.** Nothing is wrong
  with the connection. Explain the tool's message and stop. Do not keep retrying paid
  operations. The user manages their plan in the Meeting.ai web app.
- **Tools work but return no meetings.** Check the active workspace with `workspace_list`. The
  user may have meetings in a different workspace, or no meetings yet.
- **Disconnecting.** The user revokes the grant in the Meeting.ai web app under Settings › MCP & CLI.
  Revocation takes effect immediately. Removing the server or plugin locally does not prove
  that the grant was revoked.

## Support

Website: https://meeting.ai
Privacy: https://meeting.ai/privacy
Terms: https://meeting.ai/terms
Support: support@meeting.ai
