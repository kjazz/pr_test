node {
    stage('SCM') {
    checkout scm
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'SQ_SCAN1';
    withSonarQubeEnv('local_on_9930') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
