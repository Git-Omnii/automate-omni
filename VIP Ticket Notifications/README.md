# IT Support Level – VIP Ticket Notifications

A Power Automate flow that monitors a shared mailbox for VIP incident alerts from Jira and automatically posts the ticket link to a Microsoft Teams channel for prompt L1 response.

---

## What It Does

1. **Trigger** – Watches a designated mailbox for emails from Jira's automation engine with "VIP Incident" in the subject line
2. **Parse Email Body** – Extracts the text following the phrase "Open Incident Record in main application:"
3. **Extract Ticket URL** – Isolates the direct Jira ticket link from the parsed text
4. **Post to Teams** – Sends a Flow bot message to a specified Teams channel with the ticket URL embedded

---

## Flow Diagram

```
[Email Trigger: VIP Incident]
        |
        v
[Compose: Parse Email Body]
        |
        v
[Compose: Extract Jira URL]
        |
        v
[Teams: Post to Channel]
```

---

## Connections Required

| Connection | Type |
|---|---|
| Office 365 Outlook | Shared mailbox monitoring |
| Microsoft Teams | Post message to channel |

---

## Configuration

Before importing, update the following placeholders in `definition.json`:

| Placeholder | Description |
|---|---|
| `<RECIPIENT_EMAIL>` | The mailbox address being monitored |
| `<JIRA_AUTOMATION_EMAIL>` | The sender address from your Jira automation |
| `<YOUR_JIRA_DOMAIN>` | Your Jira subdomain (e.g. `yourcompany`) |
| `<TEAMS_GROUP_ID>` | The Microsoft Teams group (team) ID |
| `<TEAMS_CHANNEL_ID>` | The specific channel ID to post alerts to |

---

## How to Import

1. In Power Automate, go to **My Flows → Import → Import Package (Legacy)**
2. Upload the `.zip` export file
3. Map your existing connections for Office 365 and Teams
4. Update any hardcoded values to match your environment
5. Save and enable the flow

---

## Use Case Context

Built for an IT Service Desk environment using Jira Service Management. VIP incidents require faster SLA response times, and this flow ensures the L1 team gets an immediate Teams notification with a direct link to the ticket — no manual mailbox monitoring needed.

---

## Skills Demonstrated

- Power Automate cloud flow development
- Email parsing using `substring` and `indexOf` expressions
- Microsoft 365 connector integration (Outlook + Teams)
- Automation of IT service desk notification workflows
