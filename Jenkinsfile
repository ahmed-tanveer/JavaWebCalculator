pipeline {
    agent any

    stages {
        stage('Validate') {
            steps {
                echo 'Building..'
		sh 'mvn validate'
            }
        }
        stage('UnitTesting') {
            steps {
                echo 'Testing..'
		sh 'mvn test'
            }
        }
        stage('Sonaranalysis') {
            steps {
                echo 'Testing on sonar'
		sh 'mvn sonar:sonar -Dsonar.host.url=http://100.24.97.161:9000 -Dsonar.login=f829dd80a979c34f8cc14204aa8955a20c62012a'
		}
        }
    }

