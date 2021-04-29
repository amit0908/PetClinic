pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git 'https://github.com/amit0908/PetClinic.git'
        sh './mvnw clean compile'
      }
    }
    stage('Test') {
      steps {
        sh './mvnw test'
      }
      post {
        always {
          junit '**/taget/surefire-reports/TEST-*.xml'
        }
      }
    }
  }
}
