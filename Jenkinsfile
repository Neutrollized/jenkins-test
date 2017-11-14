node {
    try {
        // requires AnsiColor plugin
        wrap([$class: 'AnsiColorBuildWrapper', 'colorMapName': 'xterm']) {
            echo "\u27A1 inside the try"
            sh('echo alive on $(hostname)')

            stage ('Stage 1') {
                echo 'Hello World 1'
            }

            stage ('Stage 2') {
                echo 'Hello World 2'
            }
        }
    }
    catch (err) {
        echo "\u27A1 Caught: ${err}"
    }

}
