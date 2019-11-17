## SCM is tagged against a release for auditing purpose
## mvn release:prepare
## update all versions in multimodule project
### mvn release:update-versions -DautoVersionSubmodules=true
## mvn clean release:prepare will not work if there are local modifications
