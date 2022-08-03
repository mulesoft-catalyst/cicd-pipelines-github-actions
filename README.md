# github-action-mule
There are mainly two branches. Aug/1/2021 :

- main

- develop


two entry points for github actions for each branches and build_deploy_reusable.yml is re-usable workflow file:

.github/workflows/ci_cd_pipeline_development.yml@develop
  This is PR triggered for develop branch

.github/workflows/ci_cd_pipeline_release_stage_prod.yml@main
  This is manually triggered. asks user input in which environment you want to push the release.
  
There are few environment created [ this is optional for private repo as environment is not supported in private repo ]:
  - dev
  - qa
  - staging
  - prod

environment specific variables:  
  - CLOUDHUB_USERNAME
  - CLOUDHUB_PASSWORD

To run/try this example, 
- Fork this repo 
- configure your fork and setup your environment and secrets mentioned above
