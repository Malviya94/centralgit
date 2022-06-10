pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                script {
                    if (env.GIT_BRANCH=='master') {
                        bat"""
                        powershell.exe -file abc.ps1 -P ${env:BUID_NUMBER}
                        """
                    }
                }
              } 
            }
        }
    }
