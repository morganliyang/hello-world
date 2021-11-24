pipeline {
    agent any
    /*
    tools{
    gradle 'Gradle 7.3'
    }
    */
    stages {
         stage('run frontend') {
            steps {
                echo 'executing yarn...'
                nodejs('NodeJS17.1.0'){
                    sh 'yarn install'   
                }
            }
        }
         stage('run backend') {
            steps {
                echo 'executing gradle...'
                                 
                //sh './gradlew -v'
                     
                
            }
        }
        stage('Build') {
            steps {
                echo 'building the application...'
            }
        }
         stage('test') {
            steps {
                echo 'testing the application...'
            }
         }
         stage('deploy') {
            steps {
                echo 'deploying the application...'
            }
        }
    }
        post{
            always{echo 'always...'}
            success{echo 'success...'}
            failure{echo 'failure...'}
        }
        
        
    
}
