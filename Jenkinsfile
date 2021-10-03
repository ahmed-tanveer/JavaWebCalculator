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
		sh 'mvn sonar:sonar -Dsonar.host.url=http://100.24.97.161:9000 -Dsonar.login=9b843063909bfa0e23b5741e4525b9db2bf06839'
		}
        }
    }
}
