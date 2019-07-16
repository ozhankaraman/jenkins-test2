node {
    def app
    def test_cont_id

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }


    stage('Build') {
        /* Start Php Unit Tests */
        sh 'cd www; ls; phpunit --log-junit results/phpunit/phpunit.xml -c tests/phpunit.xml'

    }

    post {
        always {
            junit "www/results/phpunit/phpunit.xml"
        }
    }


}
