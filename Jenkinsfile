pipeline {
  options {
    buildDiscarder(logRotator(numToKeepStr: '10')) // Retain history on the last 10 builds
    ansiColor('xterm') // Enable colors in terminal
    timestamps() // Append timestamps to each line
    timeout(time: 20, unit: 'MINUTES') // Set a timeout on the total execution time of the job
  }
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
                echo "Build for ${env.JOB_NAME} ${env.BUILD_NUMBER} (${env.BUILD_URL})"
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
