pipeline{
  agent any
  stages {
    stage ('Build'){
      step {
        git 'https://github.com/amit0908/PetClinic.git'
        sh './mvnw clean compile'
      }
    }
    stage ('Test'){
      step {
        sh './mvnw test'
      }
      post {
        always {
          junit ' ** /taget/surefire-reports/TEST-*.xml'
        }
      }
    }
  }
}
