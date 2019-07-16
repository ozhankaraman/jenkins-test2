pipeline {
    agent any

    stages {

        stage('Clone repository') {
            /* Let's make sure we have the repository cloned to our workspace */
    
            checkout scm
        }
    
    
        stage('Build') {
            /* Start Php Unit Tests */
            sh 'cd www; ls; phpunit --log-junit results/phpunit/phpunit.xml -c tests/phpunit.xml'
    
        }

    }
}
