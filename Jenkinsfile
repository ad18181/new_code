pipeline {

    agent {

        docker {image 'horuszup/horusec-cli:latest'}
    }

 

    stages {

        stage('Checkout') {

            steps {

                // Checkout code from the branch

                checkout scm

            }

        }

 

        stage('Code Analysis with Horusec') {

            steps {

                script {

                    sh 'horusec start -p="./" --disable-docker="true" --config-file-path=horusec-config.json -a f09c888c-525e-491b-9e90-1f5876478734'

                }

            }

        }

    }

}
