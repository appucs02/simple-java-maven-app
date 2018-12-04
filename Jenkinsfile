pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'mvn Test'
		}
	post {
		always {
			junit 'target/surefire-reports/.xml'	

        }
    }
}
