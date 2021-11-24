pipeline {
    agent any
    tools{
    gradle 'gradle'
    }
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
                nodejs('NodeJS17.1.0'){
                    
                    sh './gradlew -v'
                     
                }
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
}
