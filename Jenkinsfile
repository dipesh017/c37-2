pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        sh 'echo git pull'
      }
    }

    stage('Docker Build') {
      steps {
        sh '''echo docker build .
echo docker push'''
      }
    }

    stage('Linux Testing') {
      parallel {
        stage('Linux Testing') {
          steps {
            sh 'echo Linux Testing'
          }
        }

        stage('Windows Testing') {
          steps {
            sh '''echo Windows Testing
'''
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        sh 'echo Deploy'
      }
    }

  }
}