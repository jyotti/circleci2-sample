# circleci2-sample

circleci 2.0 workflow-demo (spring-boot).

## jobs

**build**

- image openjdk:8
- gradle build ...
- save jar-file to `persist_to_workspace`

**deploy**

- image python:3.6.1
- take jar-file from `attach_workspace`
- use awscli (aws deploy...)

## workflow

- `build` => `deploy`
