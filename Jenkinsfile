pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                /* `make check` returns non-zero on test failures,
                * using `true` to allow the Pipeline to continue nonetheless
                */
                sh 'make check || true' (1)
                junit '**/target/*.xml' (2)
            }
        }
    }
}
