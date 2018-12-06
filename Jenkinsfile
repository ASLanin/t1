G_giturl = "git@github.com:ASLanin/t1.git"
G_artifactsource = "tests/m-t2/master"

properties([
// Builds rotation
    buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '10')),
    disableConcurrentBuilds(),
// Git project
    [$class: 'GithubProjectProperty', displayName: '', projectUrlStr: G_giturl],
// Trigger build from:
    pipelineTriggers([upstream(G_artifactsource), githubPush()])
])


pipeline {
    agent any
        stages {
            stage ('main') {
                steps {
                   script {
                   sh 'date'
                }
            }
        }
    }
}
