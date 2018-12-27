    pipeline {
            agent any
                options {
                    disableConcurrentBuilds()
                }

            stages {
                    stage('test') {
                            steps {
                                    sh 'echo hello'
                                    sh 'ping 8.8.8.8 -c 5'
                            }
                    }
                    stage('test1') {
                            steps {
                                    sh 'echo $TEST'
                            }
                    }
                    stage('test3') {
                            steps {
                                    script {
                                            if (env.BRANCH_NAME == 'master') {
                                                    echo 'I only execute on the master branch'
                                            } else {
                                                    echo 'I execute elsewhere'
                                            }
                                    }
                            }
                    }
            }
    }
