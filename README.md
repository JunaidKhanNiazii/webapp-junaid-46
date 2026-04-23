# webapp-junaid-46

## CI/CD Setup

This project uses GitHub Actions for continuous integration and deployment to Azure App Service.

### Prerequisites

1. Azure App Service named `app-junaid-46` must be created in your Azure subscription.
2. The repository must be hosted on GitHub.

### Setup Instructions

1. **Get the Publish Profile**:
   - Go to your Azure App Service `app-junaid-46` in the Azure Portal.
   - Navigate to **Deployment Center** > **Settings**.
   - Download the publish profile.

2. **Add Secret to GitHub**:
   - Go to your GitHub repository.
   - Navigate to **Settings** > **Secrets and variables** > **Actions**.
   - Add a new repository secret named `AZURE_WEBAPP_PUBLISH_PROFILE`.
   - Paste the content of the downloaded publish profile as the secret value.

3. **Deploy**:
   - Push changes to the `main` branch.
   - The workflow will automatically deploy to Azure App Service.

### Manual Deployment

You can also trigger the deployment manually from the Actions tab in GitHub.
