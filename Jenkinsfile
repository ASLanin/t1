pipeline {
    agent any
        stages {
            stage ('main') {
                steps {
                   script {
                   sh 'date'
                   
                   sh 'if [ -f master.txt ] ; then cat fake.txt ;fi'
                }
            }
        }
    }
}
