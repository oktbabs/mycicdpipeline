pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checking out code'
            }
        }
        stage('Build') {
            steps {
                echo 'Building Artefacts'
            }
        }
        stage('Execute Unit Tests') {
            steps {
                echo 'Executing Unit tests'
            }
        }
        stage('Code Quality') {
            steps {
                echo 'Validate Code Quality'
            }
        }
        stage('Upload Binary to nexus') {
            steps {
                echo 'Uploading binaries to Nexus Repo'
            }
        }
        stage('Deploy to DEV') {
            steps {
                echo 'Deploying to DEV'
            }
        }
        stage('Slack Notifications') {
            steps {
                echo 'Slack Notifications'
            }
        }
        stage('Approval for QA Deployment') {
            steps {
                echo 'Approval for QA Deployment'
            }
        }
        stage('Deploy to QA Environment') {
            steps {
                echo 'Deploying to QA Environment'
            }
        }    	
        stage('Approval for PROD Deployment') {
            steps {
                echo 'Approval for PROD Deployment'
            }
        }
        stage('Deploy to PROD Environment') {
            steps {
                echo 'Deploying to PROD Environment'
            }
        }    
    }
}
