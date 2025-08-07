# Shared Drive Deletion Monitor

**Shared Drive Deletion Monitor** is a project of Hack for LA. Hack for LA is a project of Civic Tech Structure, Inc. This tool helps Google Workspace administrators detect and respond to large-scale file deletions across Shared Drives. It uses daily file ID snapshots to compare yesterday’s and today’s contents, flagging deletions above a configurable threshold. Alerts are sent by email or Slack, and a dashboard tracks activity trends

### Project context
This project was developed after repeated incidents of accidental high-volume file deletions by users with Manager access. Many third-party tools priced monitoring on a per-user basis, making them cost-prohibitive. By leveraging Google Apps Script and Sheets, this system is free to run within Google Workspace quotas.  
[Full background and context document] 
[Code of Conduct](https://www.hackforla.org/code-of-conduct/)

### Technology used
- [Google Apps Script](https://developers.google.com/apps-script) — automation logic and API calls  
- [Google Sheets](https://support.google.com/docs) — data storage, logging, and dashboard  
- [Google Drive API](https://developers.google.com/drive) — file listing and metadata access  
- [Slack API](https://api.slack.com/messaging) *(optional)* — deletion alerts  

---

# How to contribute
You can help in several ways:  
- Join the conversation on Hack for LA Slack in the [#shared-drive-monitor] channel.  
- Help with testing by setting up the script in your own Google Workspace and reporting issues.  
- Improve the dashboard design or report formatting.  
- Contribute to the code by following the steps below.  

---

## Installation instructions
1. Make a copy of the [Shared Drive Monitor Google Sheet Template].  
2. Open **Extensions → Apps Script** in the copied Sheet.  
3. Paste the project’s code from `/src` into the Script Editor.  
4. In the **Config** tab of the Sheet, add the Shared Drive IDs to be monitored and adjust thresholds or notification settings.  
5. Authorize the script to access your Google Drive and Sheets.  
6. Set a daily time-based trigger to run the main monitoring function.  
7. (Optional) Configure Slack webhook URL in the config if using Slack alerts.  

---

### Working with issues
- To report a bug: [Open a new GitHub issue] with the label `bug`.  
- To request a feature: [Open a new GitHub issue] with the label `enhancement`.  
- To contribute to an existing issue, comment in the thread and coordinate with the assignee.

---

### Working with forks and branches
- Fork this repo before making changes.  
- Create a new branch for each feature or fix (`feature/your-feature-name` or `fix/your-fix-name`).  

---

### Working with pull requests and reviews
- Submit PRs to the `main` branch.  
- Assign at least one reviewer.  
- Ensure your PR description clearly states the problem and solution.  

---

### Testing
- Manually test by deleting test files in a monitored Shared Drive.  
- Confirm that deletions are logged in the Sheet and that alerts are sent.  
- Use small drives for initial testing to stay under quota limits.

### Licencing
[Add details]
