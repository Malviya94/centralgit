pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                script {
                    if (env.GIT_BRANCH=='master') {
                        echo 'hello'
                        bat"""
                        powershell.exe -file abc.ps1 -P ${env:BUID_NUMBER}
                        """
                    }
                }
              } 
            }
        }
    }
