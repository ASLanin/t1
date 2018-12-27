pipeline {
    agent any
     options {
        disableConcurrentBuilds()
     }

        stages {
            stage ('main') {
                steps {
                   script {
                   sh 'date'
                   sh 'ping 8.8.8.8 -c 100'
                   //sh 'if [ -f master.txt ] ; then cat fake.txt ;fi'
                }
            }
        }
    }
}
