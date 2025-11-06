# Using the Postman collection and environment

This repo includes a Postman collection and an environment JSON you can import into Postman (or run with Newman).
### Import into Postman (GUI)
- Open Postman → Click "Import".
- Drag-and-drop [CIRCL-Threat-Hunting-Tools.postman_collection.json](CIRCL-Threat-Hunting-Tools.postman_collection.json) and [CIRCL-Threat-Hunting-Tools.postman_environment.json](CIRCL-Threat-Hunting-Tools.postman_environment.json) (or click "Upload Files").
- After import, open the Environments dropdown (top-right) and select the imported environment to make it active.
- Inspect environment variables (gear icon → Manage Environments) such as `misp_authkey`, `misp_baseurl`.

![Screenshot of CIRCL-Threat-Hunting-Tools Postman collection](postman.png)