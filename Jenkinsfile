pipeline {
    agent any

    stages { 
        stage ('compile') {

            steps {
                WithMaven(maven : 'mymaven') {
                    sh 'compile'
            
                 }
            }

        }
        stage ('test') {

            steps {
                WithMaven(maven : 'mymaven') {
                    sh 'test'
                }

            }

        }
        stage ('package') {

            steps {
                WithMaven(maven : 'mymaven') {
                    sh 'package'
                }
            }
        }
        
    }
}
