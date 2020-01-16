pipeline {
    agent any

    stages {
        stage('All in one') {
            steps {
                node('maven') {
                    def maven = docker.image('maven:latest')
                    maven.pull()
                    maven.inside {
                        sh 'mvn clean compile'
                        sh 'mvn test'
                        sh 'mvn deploy'
                    }
                }
            }
        }
    }
}
