pipeline {
    agent any
        
    tools {
        jdk "JDK-18"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
         
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
