# github-action-mule
There are mainly two branches. Aug/1/2021 :

main

develop


two entry points for github actions:

.github/workflows/ci_cd_pipeline_development.yml@develop
  This is PR triggered for develop branch

.github/workflows/ci_cd_pipeline_release_stage_prod.yml@main
  This is manually triggered. asks user input in which environment you want to push the release.
  
There are few environment created:
  - dev
  - qa
  - staging
  - prod
environment specific variables:  
      CLOUDHUB_USERNAME
      CLOUDHUB_PASSWORD
