# Title

This runs standard maven build installs with standard flags used by the IKMDev team.

### Team Ownership - Product Owner

Automation Team

## How to Use

Create a build in the `.github/workflows` folder, as described in the 
[GitHub Documentation](https://docs.github.com/en/actions/writing-workflows/quickstart).  Add the following code, 
or something like it:

```yaml
env:
  MAVEN_SETTING: '/home/ec2-user/maven/.m2/settings.xml'
  BRANCH_NAME: ${{github.ref_name}}

jobs:
  build-job:
    name: Build Job
    runs-on: ubuntu-24.04
    if: github.repository_owner == 'ikmdev'
    steps:
          - name: Build IKMDEV Code
            uses: ikmdev/maven-promote-action@main
            with:
              branch_name: ${{env.BRANCH_NAME}}
```

## Issues and Contributions
Technical and non-technical issues can be reported to the [Issue Tracker](https://github.com/ikmdev/maven-unique-release-action/issues).

Contributions can be submitted via pull requests. Please check the [contribution guide](doc/how-to-contribute.md) for more details.

Testing num 2
