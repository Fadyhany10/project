## Udagram Pipeline

![Pipeline](pipline digram.png)

### Continuous Integration
#### GitHub
When the developers commit any chagnes to github repo this will trigger an action to circleci to build and deploy our changes.

#### CircleCI
CircleCI reads the `.circleci/config.yml` file which tells the service what has to be done. there are 2 jobs to be run by CircleCI.
- **build**: Runs the `build` and `install any dependencies` script given in the `package.json` file.
- **deploy**: Runs the `deploy` script, then runs the `archive` script. Then uses AWS CLI to upload archive to S3.
