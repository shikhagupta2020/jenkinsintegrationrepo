pipeline {
    agent any

 

    stages {      
        stage('S1: Build') {
            steps {
                echo 'Build process started'
             azureCLI commands: [[exportVariablesString: '', script: 'az login']], principalCredentialId: '4a76623b-7c19-4a62-8d78-b68e2bc0177c'
                echo 'Build process completed'
            }
        }
        
    }
}
