pipeline {
    agent any

    stages { 
        stage ('compile') {

            steps {
                WithMaven(maven : 'mymaven') {
                    sh 'mvn clean compile'
            
                 }
            }

        }
        stage ('test') {

            steps {
                WithMaven(maven : 'mymaven') {
                    sh 'mvn test'
                }

            }

        }
        stage ('package') {

            steps {
                WithMaven(maven : 'mymaven') {
                    sh 'mvn package'
                }
            }
        }
        
    }
}
