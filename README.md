# circleci-monorepo
An example monorepo for a golang with CircleCI

Building in CircleCI:
1. Add your project
2. Under your user settings, create a "Personal API Token"
3. Under the project settings, add an environment var "CIRCLE_TOKEN" with the personal API token

To add a service:
1. Create a new directory with the code
2. Add it to .circleci/config.yml
3. Add it to project-dirs

How does it work?  
Everytime you commit a change, it finds the modified files, identifies which directories they reside in, adds dependant directories and calls CircleCI APIs to run builds for these directories.
