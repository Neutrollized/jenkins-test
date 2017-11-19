// docker vars
env.DOCKER_ANGULARCLI = 'neutrollized/chromium-headless-nodejs'
env.NG_VER = '6.11.3'
env.KARMA_PORT = '-p 9876:9876'
env.PROTRACTOR_PORT = '-p 49152:49152'

// node/nmp/ng vars
env.NPM_OPTS = '--silent'
env.BUILD_OPTS = '--progress=false'
env.TEST_OPTS = '--progress=false'
env.E2E_OPTS = '--progress=false'

// requires Pipeline Remote Loader Plugin
fileLoader.fromGit(
  'jenkins_pipeline',
  'https://github.com/Neutrollized/jenkins_pipeline-test.git',
  'master'
)
