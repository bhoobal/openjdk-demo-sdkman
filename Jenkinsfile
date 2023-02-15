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
