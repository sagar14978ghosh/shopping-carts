pipeline {
  agent any
  stages {
    stage('compile-app') {
      steps {
        echo 'this is the compile job'
        sh 'mvn compile'
      }
    }

    stage('test-app') {
      steps {
        echo 'this is the test job'
        sh 'mvn test'
      }
    }

    stage('package-app') {
      steps {
        echo 'this is the package job'
        sh 'mvn package'
      }
    }

    stage('archive-app') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'this is my first pipeline and it has been completed...'
    }

  }
}