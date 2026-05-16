# Using Joule In-App

> Quick notes on how Joule is accessed and used directly inside SAP applications.

---

# Official Documentation

## Using Joule

https://help.sap.com/docs/joule/serviceguide/using-joule

---

# Opening Joule

Joule can be opened using:

- Built-in launcher  
  - Floating button at the bottom-right of the screen

- Custom launch option  
  - Implemented by integrating web platform

### Example

SAP S/4HANA Fiori Launchpad provides a built-in button in its toolbar.

---

# After Opening Joule

You can:

- trigger a conversation
- enter a request in the input field
- press Enter
- click Send

---

# Conversation Expiration

- Conversations expire after:
  ```text
  8 hours of inactivity
  ```

- After expiration:
  - user is notified
  - option provided to trigger new conversation

---

# Managing Multiple Conversations

Users can:

- start new conversation
- rename conversations
- delete conversations

### Limits

| Type | Limit |
|---|---|
| Active Conversations | 10 |
| Expired Conversations | 7 days |

---

# Important Notes

Once open:

- Joule offers useful actions in side menu panel
- Joule can be closed anytime
- Expanded mode provides larger interaction space
- Settings icon appears inside side menu panel

---

# Main Actions Available

- Disable streaming
- Add new conversation
- View active threads
- View expired conversations
- Rename conversations

---

# UI Reference Screens

## Joule Toolbar Button

![images](using joule.png)

---

# My Notes

## Important Observations

- Joule is embedded directly into SAP applications.
- User experience is conversational and contextual.
- Conversation lifecycle management is built-in.
- Multi-conversation support behaves similarly to modern AI chat tools.
- In-app integration is important for enterprise adoption.

---

# Things to Explore Next

- Joule launch architecture
- In-app contextual grounding
- SAP Launchpad integration
- Embedded Joule workflows
- Joule capability triggering
