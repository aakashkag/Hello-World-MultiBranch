pipeline {
  agent any
  stages {
        stage('Setup') {
            steps {
                echo 'Setup Stage'
                sh '''
                 python3 hello.py
                '''
            }
        }
        stage('Build') {
            steps {
                echo 'Build Stage'
                echo "current build number: ${currentBuild.number}"
            }
        }
        stage('QA') {
            steps {
                echo 'QA Stage' 
            }
        }
         stage('Deploy') {
            steps {
                echo 'Deploy Stage' 
            }
        }
         stage('Monitor') {
            steps {
                echo 'Monitor Stage' 
            }
        }
    }
}
