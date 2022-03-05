pipeline {
  agent any

  stages {
      stage('Build Artifact') {
            steps {
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar' //comment
            }
        }   
      stage('Unit Tests') {
            steps {
              sh "mvn test"
            }
        }
    }
}
