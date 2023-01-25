<!-- CICD Pipelines for mule application deployment to cloudhub using GitHub Actions  -->
# Branch Details
There are two branches. Aug/1/2021 :
1. main
2. develop

two entry points for github actions for each branches and build_deploy_reusable.yml is re-usable workflow file:

.github/workflows/ci_cd_pipeline_development.yml@develop
  This is PR triggered for develop branch

.github/workflows/ci_cd_pipeline_release_stage_prod.yml@main
  This is manually triggered. asks user input in which environment you want to push the release.

# Environment and Secrets Setup
## Environment
There are few environment created [ this is optional for private repo as environment is not supported in private repo ]:
1. dev
2. qa
3. staging
4. prod
## Environment Secrets
Environment specific variables:  
1. CLOUDHUB_USERNAME
2. CLOUDHUB_PASSWORD

# How to Trigger pipeline
1. Fork this repo 
2. configure your fork and setup your environment and secrets mentioned above
3. Trigger pipeline either manually, by PR or cronjob schdeduled

# Features
## Mule Application
1. Mule Application compile, build, test, package [Aug/2021]
2. Mule Application release prepare and perform [Aug/2021]
3. CloudHub Deployment using username/password [Aug/2021]
## GitHub Actions
Most of the advanced features are used in this pipeline workflows
