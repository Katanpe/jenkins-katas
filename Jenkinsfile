pipeline {
  agent {
    docker {
      image 'gradle:6-jdk17'
    }

  }
  stages {
    stage('Say Hello') {
      steps {
        sh 'echo "hello world"'
      }
    }

    stage('build app') {
      agent {
        docker {
          image 'gradle:6-jdk11'
        }

      }
      steps {
        sh 'ci/build-app.sh'
      }
    }

  }
}