pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                script {
                    echo env.GIT_BRANCH
                    if (env.GIT_BRANCH=='origin/master') {
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
