pipeline {
    agent any

    stages { 
        stage ('compile stage') {

            steps {
                WithMaven(maven : 'mymaven') {
                    sh 'mvn clean compile'
            
                 }
            }

        }
        stage ('testing stage') {

            steps {
                WithMaven(maven : 'mymaven') {
                    sh 'mvn test'
                }

            }

        }
        stage ('packaging stage') {

            steps {
                WithMaven(maven : 'mymaven') {
                    sh 'mvn package'
                }
            }
        }
        
    }
}
