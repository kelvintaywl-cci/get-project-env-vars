
# get-project-env-vars
Extracting project environment variables (env vars) in CircleCI

This project showcases, through a _.circleci/config.yml_ how you can extract the project env vars from your CircleCI project.

The env vars will be saved into a _extracted.csv_, and uploaded as a build artifact when this job runs.

## Important

:warning: 

### Disclaimer

This is not an official tool, nor endorsed by CircleCI.
In general, I would recommend users SSH into a build to extract the values, if possible.

You can use [the Python script in here](https://github.com/kelvintaywl-cci/get-project-env-vars/blob/2c8874bcb78cde6c4f8b3da1d334a22a08e0b4b6/.circleci/config.yml#L21-L42) when inside the SSH session.

### Prerequisites

Before starting, please make sure that:

- your repository and project is **private**; This should not be used for public projects.

- you understand the risk that **anyone with read access** to your project can see the extracted CSV file.

## How to use

1. Copy the _.circleci/config.yml_ on this project to your own.
2. Modify the `pipeline.parameters.envs` default value to match the list of env vars you need.
3. Commit the updated _.circleci/config.yml_ to your project on GitHub / BitBucket / GitLab.
4. Head over to app.circleci.com and find the triggered "build" job.
5. Go over to the **Artifacts** tab, and download the _/home/circleci/project/extracted.csv_ file.
