pipeline {
    agent any

    stages { 
        stage ('compile') {

            steps {
                environment(maven : 'mymaven') {
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
