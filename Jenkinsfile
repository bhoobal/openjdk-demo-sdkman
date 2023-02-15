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
                    sh 'curl -s https://get.sdkman.io | bash'
                    sh 'source "/usr/local/sdkman/bin/sdkman-init.sh"'
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
