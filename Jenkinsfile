node {
    try {
        // requires AnsiColor plugin
        wrap([$class: 'AnsiColorBuildWrapper', 'colorMapName': 'xterm']) {
            echo "\u27A1 inside the try"
            sh 'echo alive on $(hostname)'

            stage ('Checkout source') {
                // Pull the latest commit of the specified branch(es)
                // of the specified submodule(s)
                checkout scm
                sh 'git submodule update --remote --init'

                echo "\u27A1 GIT_PROJECT: ${env.GIT_PROJECT}"
                echo "\u27A1 GIT_PROJECT_KEY: ${env.GIT_PROJECT_KEY}"
                echo "\u27A1 GIT_REPO: ${env.GIT_REPO}"
                echo "\u27A1 GIT_BRANCH: ${env.GIT_BRANCH}"
                echo "\u27A1 GIT_COMMIT: ${env.GIT_COMMIT}"
                echo "\u27A1 GIT_COMMIT_SHORT: ${env.GIT_COMMIT_SHORT}"
            }  

            stage ('Stage 1') {
                echo 'Hello World 1'
            }

            parallel {
                stage ('Stage 2A') {
                    echo 'Hello World 2a'
                }

                stage ('Stage 2B') {
                    echo 'Hello World 2b'
                }
            }
        }
    }
    catch (err) {
        echo "\u27A1 Caught: ${err}"
    }

}
