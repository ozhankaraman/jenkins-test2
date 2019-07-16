pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                /* Start Php Unit Tests */
                sh 'cd www; ls; phpunit --log-junit results/phpunit/phpunit.xml -c tests/phpunit.xml'
            }
        }
    }
}
