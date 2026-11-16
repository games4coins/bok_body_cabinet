# BOK Body TEST — Google Apps Script

This folder is a deployment scaffold, **not** the current backend. Before running the workflow, copy the complete verified TEST Apps Script source files (Code.gs, Players.gs, Deposits.gs, VKLinks.gs, VKCabinet.gs, etc.) into this folder. Do not copy production credentials or secrets.

Script ID is configured in root `.clasp.json`. Set GitHub Actions environment `test-gas`:
- Secret `CLASPRC_JSON`: full contents of the local clasp OAuth credentials file `~/.clasprc.json` (never commit it).
- Variable `GAS_DEPLOYMENT_ID`: TEST deployment ID (the string between `/s/` and `/exec` in the current TEST URL).

Enable Google Apps Script API in the Google account settings and grant clasp OAuth access locally. Configure a GitHub environment with required reviewers before using live funds.

Run manually from GitHub Actions → Deploy TEST Google Apps Script → Run workflow. It is intentionally NOT automatic on push until the backend is fully imported and tested. This workflow changes only the TEST Apps Script deployment, not production.

IMPORTANT: Script Properties (e.g. VK_TOKEN), project settings and spreadsheet access are managed in Google Apps Script and are not committed to GitHub. Verify the manifest matches your existing project before first push. The manifest here is only a placeholder; replace with the actual TEST project's manifest.
