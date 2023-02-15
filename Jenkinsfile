pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
         
            }
        }
        stage('sdkman') {
            steps {
                script {
                    sh 'echo $SHELL'
                    sh 'export SDKMAN_DIR="/usr/local/sdkman" && curl -s "https://get.sdkman.io" | bash'
                    sh 'sdk version'
                    sh 'sdk install java 8.0.352-amzn'
                    sh 'sdk use java 8.0.352-amzn'
                    sh 'sdk current'
                }
            }
        }
        stage('gradle') {
            steps {
                echo 'gradle....'
                sh './gradlew -v'
            }
        }
    }
}
