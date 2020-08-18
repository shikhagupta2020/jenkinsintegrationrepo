pipeline {
    agent any

 

    stages {      
        stage('S1: Build') {
            steps {
                echo 'Build process started'
             azureCLI commands: [[exportVariablesString: '', script: 'az login --username gushikhadm@MFCGD.com --password 15RahRamf']]
                echo 'Build process completed'
            }
        }
        
    }
}
