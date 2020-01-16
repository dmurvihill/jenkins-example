pipeline {
    agent any

    stages {
        node('maven') {
            stage('All in one') {
                steps {
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
