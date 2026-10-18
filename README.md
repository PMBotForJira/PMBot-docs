# Terms of Service and Privacy Policy

**Last Updated:** October 16, 2026

By installing and using the **"Telegram PMBot"** application (hereinafter, "the Application") in your Atlassian Jira instance, you agree to these terms. This is an independently developed tool provided "as is" to facilitate project management.

## 1. Description of Service
The Application acts as a bridge between the Atlassian Jira API and the Telegram API, enabling users to receive assignment notifications, report progress, view executive summaries, and transition task statuses directly from a Telegram chat. The platform operates under a multi-tenant architecture, allowing a single user to receive notifications from multiple Jira projects or instances within a single Telegram account.

## 2. Privacy and Data Handling
To ensure fast and secure routing, PMBot divides data processing between your organization's local infrastructure and a centralized router.

### 2.1 Data Stored in Your Jira Instance (Atlassian Forge)
Within the secure infrastructure of your own Atlassian administration, the following data is stored:
- Jira user identifiers (Account IDs).
- Project configurations (Reporting schedules, linear workflows, and assigned roles).
- Local mapping of users to the bot.

### 2.2 Data Processed by the Central Router (Google Cloud Platform)
To allow a single Telegram account to connect to multiple Jira boards, we use Google Cloud Platform (GCP) as a sub-processing service (Proxy). In this cloud database, **only** the following technical information is stored for routing purposes:
- Your public numerical Telegram identifier (Chat ID).
- An array containing the webhook URLs of the Jira instances you have authorized for linking.
- Single-use temporary tokens for account registration (which self-destruct after 24 hours or upon use).

### 2.3 Content and Message Transit
The content of your tasks (titles, descriptions, progress comments, and assignee names) travels in encrypted form between Jira, our GCP proxy, and Telegram. **GCP does not store, log, or retain the content of your messages or the information from your tickets.** The proxy acts exclusively as a real-time conduit. The developer and creator of the Application **has no access** to your Jira tickets, comment history, user credentials, or Telegram conversations.

## 3. Limitation of Liability
Use of the Application is at the sole risk and responsibility of the user or installing entity. While standard customer support is provided via our designated support channel, no explicit guarantees of uninterrupted 24/7 availability (SLA) or corrective maintenance are offered.

- **Third-Party Dependencies:** The continuous operation of PMBot depends on the stability and availability of the Atlassian, Telegram, and Google Cloud Platform APIs. PMBot is not responsible for delays or lost notifications resulting from outages in these external services.
- **Handling of Sensitive Information:** Because the Application transmits summaries via Telegram (a third-party messaging application), it is the sole responsibility of the user and the administering Jira organization to avoid transmitting passwords, credentials, financial data, or highly confidential personal information through the bot's reports.

## 4. Uninstallation and Right to Erasure
The administrator may revoke access and uninstall the Application at any time from the "Manage Apps" settings in their Jira instance, which will immediately stop notifications from being sent from that project.

For a user to completely remove their digital footprint from the central router (GCP), they may request the deletion of their Chat ID or simply block and delete the conversation with the bot in the Telegram application, which will invalidate any future routing attempts.
