
node {
  stage('SCM') {
    git 'https://sonarsource-bitbucket-test.valiantys.net/scm/kris/pr_test.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'sonar_scanner';
    withSonarQubeEnv('SQ@9000') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
