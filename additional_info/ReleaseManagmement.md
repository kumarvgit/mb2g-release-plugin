## SCM is tagged against a release for auditing purpose
## mvn release:prepare
## delete git tag (both of below step is needed)
### remote --> git push --delete origin mb2g-release-plugin-1.0
### delete local repository tag --> git tag -d mb2g-release-plugin-1.0   
## update all versions in multimodule project
### mvn release:update-versions -DautoVersionSubmodules=true
## mvn clean release:prepare will not work if there are local modifications
## mvn release:rollback is going to rollback the tag but manually delete the tag from remote and local (there is a bug in release plugin)
## mvn clean release:prepare -DdryRun=true
## mvn dependency:go-offline -- download all deps and go offline to work with
## --batch-mode accepts default values
