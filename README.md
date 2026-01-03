n8n Google OAuth Stability & Health Check

This project contains a diagnostic workflow and configuration guide to ensure Google OAuth (Gmail/Drive) tokens refresh correctly within n8n, especially for multi-user environments.

Core Fixes Included:

Scope Verification: Ensures https://www.googleapis.com/auth/drive.file and https://www.googleapis.com/auth/gmail.send are correctly requested.

Offline Access: Logic to force the access_type=offline and prompt=consent parameters to ensure a Refresh Token is provided during the first handshake.

Health Check Workflow: A recurring n8n workflow that pings the Google 'Token Info' endpoint to verify credential health before the main automation runs.