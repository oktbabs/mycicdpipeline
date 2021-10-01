pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
              withCredentials([gitUsernamePassword(credentialsId: '73b3562f-8684-4049-a7c1-ff8983c89640', gitToolName: 'git')]) {
               sh 'git clone https://github.com/oktbabs/spring-boot-mongo-docker.git'
              }
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
                nexusArtifactUploader artifacts: [
                    [artifactId: 'spring-boot-mongo', 
                     classifier: '', 
                     file: 'target/spring-boot-mongo-1.0', 
                     type: 'war']
                ], 
                    credentialsId: 'NEXUS3_CREDS', 
                    groupId: 'com.mt', 
                    nexusUrl: 'jenkinserver.mycompany.com:8081', 
                    nexusVersion: 'nexus3', 
                    protocol: 'http', 
                    repository: 'timmyfirstnexus', 
                    version: '1.0'
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
