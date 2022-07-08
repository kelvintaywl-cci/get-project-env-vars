# get-project-env-vars
Extracting project environment variables (env vars) in CircleCI

This project showcases, through a _.circleci/config.yml_ how you can extract the project env vars from your CircleCI project.

The env vars will be saved into a _extracted.csv_, and uploaded as a build artifact when this job runs.

## Important

Before starting, please make sure that:

- your repository and project is private; This should not be used for public projects.

## How to use

1. Copy the _.circleci/config.yml_ on this project to your own.
2. Modify the `pipeline.parameters.envs` default value to match the list of env vars you need.
3. Commit the updated _.circleci/config.yml_ to your project on GitHub / BitBucket / GitLab.
4. Head over to app.circleci.com and find the triggered "build" job.
5. Go over to the **Artifacts** tab, and download the _/home/circleci/project/extracted.csv_ file.
