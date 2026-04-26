# automate-omni

A collection of Power Automate flows built for enterprise IT operations. Each flow is organized into its own folder containing the exported package, a `definition.json` for configuration, and a dedicated README with setup instructions.

---

## Repository Structure

```
automate-omni/
├── it-support-vip-ticket-notifications/
│   ├── definition.json
│   ├── VIPTicketNotifications.zip
│   └── README.md
└── ...
```

Each folder represents a standalone flow. More flows will be added over time as the collection grows.

---

## Flows

| Folder | Description |
|---|---|
| `it-support-vip-ticket-notifications` | Monitors a shared mailbox for Jira VIP incident alerts and posts the ticket link to a Teams channel for immediate L1 response |

---

## General Import Instructions

All flows follow the same import process in Power Automate:

1. Go to **My Flows → Import → Import Package (Legacy)**
2. Upload the `.zip` file from the flow's folder
3. Map your existing connections when prompted
4. Open `definition.json` and update the placeholder values documented in that flow's README
5. Save and enable the flow

---

## Skills Demonstrated

- Power Automate cloud flow development
- Microsoft 365 connector integration (Outlook, Teams, SharePoint, and more)
- Email parsing and string manipulation using Power Automate expressions
- IT service desk automation and notification workflows
- Enterprise-scale flow design with reusable, configurable patterns

---

## About

Built and maintained by Brian Wilson. All flows are designed around real enterprise IT workflows with a focus on reducing manual effort, improving response times, and integrating across the Microsoft 365 ecosystem.
