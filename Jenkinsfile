pipeline {

    agent any

    environment {
        NEW_VERSION = '1.3.0'
    }

    tools {
        maven "Maven"
    }

    stages {

        stage("build"){

            steps {
                echo 'Building the application'
                echo "Building version ${NEW_VERSION}"
                sh 'mvn clean'
                sh 'mvn install'
            }

        }

        stage("test"){

            steps {
                echo 'Testing the application'
            }

        }

        stage("deploy"){

            steps {
                echo 'Deploying the application'
            }

        }
    }

    post {
        always {
            echo "post always"
        }
        success {
            echo "post success"
        }
        failure {
            echo "post failure"
        }
    }

}