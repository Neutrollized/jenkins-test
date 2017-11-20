// docker vars
env.DOCKER_NODEJS = 'neutrollized/headless-chrome-nodejs'
env.NODEJS_VER = '6.11.2'
env.KARMA_PORT = '-p 9876:9876'
env.PROTRACTOR_PORT = '-p 49152:49152'

// node/nmp/ng vars
env.NPM_OPTS = '--silent'
env.BUILD_OPTS = '--progress=false'
env.TEST_OPTS = '--progress=false'
env.E2E_OPTS = '--progress=false'

// Manadatory Jenkinsfile vars
env.PROJECT_REPO = 'test-code'
//env.PROJECT_DIR = 'angular-realworld-example-app'
env.PROJECT_DIR = 'esri-angular-cli-example'

// requires Pipeline Remote Loader Plugin
fileLoader.fromGit(
  'jenkins_pipeline',
  'https://github.com/Neutrollized/jenkins_pipeline-test.git',
  'master'
)
