pipeline {
    agent any

    environment {
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/teyiamah/aws-cicd.git'
        IMAGE_TAG = 'teyiamah/awscicd'
        IMAGE_VERSION = ${BUILD_NUMBER}
    }
     
     stages {
        stage('git checkout'){
            steps{
                git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
            }
        } 
        stage('docker build'){
            steps{
                sh 'docker build -t "${IMAGE_TAG}:${IMAGE_VERSION}" .'
                sh 'docker images'
            }
        }

      }

}