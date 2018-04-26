pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh './gradlew clean classes'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'
		junit 'build/test-results/**/*.xml'
            }
        }
    }
}
