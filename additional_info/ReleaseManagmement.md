## SCM is tagged against a release for auditing purpose
## mvn release:prepare
## update all versions in multimodule project
### mvn release:update-versions -DautoVersionSubmodules=true
## mvn clean release:prepare will not work if there are local modifications --> this step is going to create a tag in scm for corresponding release this step has not performed the release
## mvn release:perform --> this step will actually perform the release which will include deploying into package cloug
## mvn release:clean is going to clean the prepare step
