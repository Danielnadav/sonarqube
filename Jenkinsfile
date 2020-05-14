node {
  stage('SCM') {
    git 'git@github.com:scmgalaxy/java-sonar-runner-simple.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'sonar';
    withSonarQubeEnv('SonarQubeserver') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}