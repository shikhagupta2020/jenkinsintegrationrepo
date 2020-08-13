pipeline {
    agent any

    stages {
        stage('S1: Verify repository branch') {
            steps {
                echo "$GIT_BRANCH"
                sh label: '', script: 'echo \'Hello from SH\''
            }
        }        
        stage('S2: Build') {
            steps {
                echo 'Build process started'
                withCredentials([azureServicePrincipal('666ae483-f746-479c-b519-6e79fa87c6af')]){
                    sh '''
                    'az login'
                }
                echo 'Build process completed'
            }
        }
        stage('S3: Validate build / test') {
            steps {
                echo 'Build validation process started'
                echo 'Run/test process completed'
            }
        }
        stage('S4: Upload to registry') {
            steps {
                echo 'Uploading build to registry started'
                echo 'Uploading build to registry finished'
            }
        }   
        stage('S5: Scanning build') {
            steps {
                echo 'Scanning build started'
                azureCLI commands: [[exportVariablesString: '', script: '/usr/local/bin/az --help']], principalCredentialId: '666ae483-f746-479c-b519-6e79fa87c6af'  
                echo 'Scanning build finished'
            }
        }              
        stage('S6: Deploy') {
            steps {
                echo 'Deploy process started'           
                echo 'Deploy process finished'
            }
        }
    }
}
