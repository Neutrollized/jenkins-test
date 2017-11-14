node {
    try {
        // requires AnsiColor plugin
        wrap([$class: 'AnsiColorBuildWrapper', 'colorMapName': 'xterm']) {
            echo "\u27A1 inside the try"
            sh 'echo alive on $(hostname)'

            stage ('Clean workspace') {
                deleteDir()
                sh 'pwd'
                sh 'ls -lah'
            }

            stage ('Checkout source') {
                // Pull the latest commit of the specified branch(es)
                // of the specified submodule(s)
                checkout scm
                sh 'git submodule update --remote --init'
            }  
        }

        stage ('Build') {
            echo 'Compiling software'
        }

/*
        stage ('Parallel stage') {
            parallel {
                stage ('Run integration test 1') {
                    steps {
                        echo 'Running test 1'
                    }
                }
                stage ('Run integration test 2') {
                    steps {
                        echo 'Running test 2'
                    }
                }
                stage ('Run UI functional tests') {
                    steps {
                        echo 'Running test 3'
                    }
                }
            }
        }
*/
        stage ('Parallel stage') {
            steps {
                parallel {
                    "stage1": {
                        echo 'Running test 1'
                    }
                }
                    "stage2": {
                        echo 'Running test 2'
                    }
                }
                    "stage3": {
                        echo 'Running test 3'
                    }
                }
            }
        }
    }
    catch (err) {
        echo "\u27A1 Caught: ${err}"
    }

}
