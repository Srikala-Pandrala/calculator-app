pipeline {
    agent any
    tools {
        maven 'Maven3' 
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build & Test') {
            steps {
                // Using the verified proxy flags for the Jenkins environment
                sh "mvn clean test -DproxySet=true -DproxyHost=staffnet.rgukt.ac.in -DproxyPort=3128 -DproxyUser=mgntguest1 -DproxyPassword=rgurgu"
            }
        }
    }
}
