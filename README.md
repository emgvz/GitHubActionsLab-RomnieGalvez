#GitHub Actions Lab - Workflows Summary

## Workflow 1: Dependent Jobs Workflow
The purpose of Workflow 1 is to demonstrate sequential job executing using the keyword "needs".
This workflow runs three jobs in order: 1. build 2. test 3. deploy
Workflow triggers on push to the main branch.

## Key Concepts
- runs the workflow when code is pushed to the main branch.
- keyword "needs" creates dependencies.
- keyword "run" executes shell commands inside each job.

## Workflow 2: Multi-Platform Workflow
The purpose of Workflow 2 is to demonstrate multiple jobs that are running in parallel on different operating systems.
Workflow triggers on pull request to the main branch and runs three separate jobs:
1. ubuntu-job
2. windows-job
3. macos-job

Each job checks out the code, runs a command, creates a string message and appends that message to a textfile then prints the contents of the textfile.

## Key Concepts
- needs to trigger a pull_request for the workflow to run.
- since workflow doesn't have the keyword needs, the jobs will run in parallel.
- runs-on: shows how to run jobs on Ubuntu, Windows, and macOS.

## Challenges Faced and How They Were Resolved
- No upstream branch error when pushing it to the repositroy: Fixed by pushing with 'git push --set-upstream origin <your-branch-name-here>'.
- YAML formatting issues: Corrected indentation and spacing to avoid syntax errors.
- Workflow not triggering and showed an error: At first the workflow didn't run because the YAML file was empty, after adding a workflow code and pushing it to the repository, the workflow successfuly triggered.
