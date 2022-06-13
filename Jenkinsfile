pipeline {
     agent {
                node { label 'Build'}
            }
    environment {
        a='abc'    
    }
    stages {
        stage('Hello') {
            agent {
                node { label 'Build'}
            }
            steps {
                echo 'Hello World'
                script {
                    echo env.GIT_BRANCH
                     if (env.GIT_BRANCH=='origin/master' || env.GIT_BRANCH=='origin/Dev') {
                        echo 'hello'
                        bat"powershell.exe -file abc.ps1 -P mkdir -Q $a"
                    }
                }
              }
        }
            stage('test') {
                 agent {
                node { label 'hjh'}
            }
                steps {
                input('Do you want to proceed?')
                    echo 'hello'
                    catcherror(buildResult: 'ABORT', stageResult: 'FAILURE') {
                        sh "exit 0"
                    }
                }
            }
            
        }
    }
