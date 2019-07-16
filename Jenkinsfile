/* https://jenkins.io/doc/book/pipeline/jenkinsfile/ */
pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                /* Start Php Unit Tests */
                sh 'echo "Build Adimi"'
            }
        }

        stage('Test') {
            steps {
                /* `make check` returns non-zero on test failures,
                * using `true` to allow the Pipeline to continue nonetheless
                */
                sh 'cd www; ls; phpunit --log-junit results/phpunit/phpunit.xml -c tests/phpunit.xml'
            }
        }


    }
    post {
        always {
            junit 'www/results/phpunit/phpunit.xml'
        }
    }
}
