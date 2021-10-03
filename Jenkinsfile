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
                echo 'Testing on bugs'
		sh 'mvn sonar:sonar -Dsonar.host.url=http://100.24.97.161:9000 -Dsonar.login=9223f69a89c2804ef061460b11f0df4e7486652f'
            }
        }
    }
}
