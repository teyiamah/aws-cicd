pipeline {
    agent any
     
     stages {
        stage('git checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/teyiamah/aws-cicd.git'
            }
        }
        stage('test'){
            steps{
                sh 'echo test'
            }
        }

      }

}