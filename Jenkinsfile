pipeline {
    agent any
    environment {
        a='abc'    
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                script {
                    echo env.GIT_BRANCH
                    if (env.GIT_BRANCH=='origin/master') {
                        echo 'hello'
                        bat"powershell.exe -file abc.ps1 -P ${env:BUILD_NUMBER} -Q $a -f ab"
                    }
                }
              } 
            }
        }
    }
