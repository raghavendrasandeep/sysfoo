pipeline {
    agent any
  
    tools {
      maven 'Maven 3.9.6'
    }
    stages {
        stage("Build") {
            steps {
              echo 'compiling sysfoo app...'
              sh 'mvn compile'
            }
        }
        stage("test") {
            steps {
              echo 'running unit tests'
              sh 'mvn clean test'
            }
        }
        stage("package") {
            steps {
              echo 'packing the app...'
              sh 'mvn package -DskipTests'
            }
        }
    }
  post{
    always{
      echo 'This pipeline is completed..'
  }

}
}
