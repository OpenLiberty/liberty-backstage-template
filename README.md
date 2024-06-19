# Open Liberty Backstage Template
This is a sample template for Backstage/Red Hat Developer Hub that creates and deploys the Liberty Starter app on Kubernetes.

## What does it do?
This template after taking parameters from Backstage/RHDH does the following:
1. Creates a new repo on git containing starter code for application development.
2. Creates a new repo on git containing GitOps configuration for deployment.
3. Sets up a build pipeline using GitHub Actions.
4. Deploys the application code to kubernetes via GitOps.

## Prerequisites
In order to use this template in Backstage/RHDH the plugins must be properly configured and the underlying development platfrom must be set up.  Info on this can be found on the Backstage site as well as the steps we took to set up our platform can be found here.  The setup steps vary based on which platform you opt for.
- Some form of Backstage instance (ex: on-prem Backstage, RHDH)
  - [Backstage](https://backstage.io/docs/getting-started/)
  - [RedHat Developer Hub](https://developers.redhat.com/rhdh/getting-started)
- GitHub Application created and connected to Backstage. ([Backstage](https://backstage.io/docs/auth/github/provider#create-an-oauth-app-on-github)) ([RHDH](https://developers.redhat.com/learning/learn:openshift:install-and-configure-red-hat-developer-hub-and-explore-templating-basics/resource/resources:configure-github-access-red-hat-developer-hub))
- Kubernetes Frontend and Backend Plugins enabled and configured for the deployment location. ([Backstage](https://backstage.io/docs/features/kubernetes/installation)) ([RHDH](https://access.redhat.com/documentation/en-us/red_hat_developer_hub/1.1/html/administration_guide_for_red_hat_developer_hub/rhdh-installing-dynamic-plugins))
- ArgoCD installed and set up. [ArgoCD Docs](https://argo-cd.readthedocs.io/en/stable/getting_started/)
- ArgoCD Plugins added to Backstage 
  - Frontend: ([Backstage](https://github.com/RoadieHQ/roadie-backstage-plugins/tree/main/plugins/frontend/backstage-plugin-argo-cd)) (RHDH: )
  - Backend ([Backstage](https://www.npmjs.com/package/@roadiehq/backstage-plugin-argo-cd-backend)) (RHDH: )
  - Scaffolder: ([Backstage](https://www.npmjs.com/package/@roadiehq/scaffolder-backend-argocd))
  
- GitHub Actions plugin installed and set up. ([Backstage](https://github.com/backstage/community-plugins/tree/main/workspaces/github-actions/plugins/github-actions))

## Usage
Once all the prerequisites are set up you can use this template with the following steps
