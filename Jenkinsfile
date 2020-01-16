pipeline {
    agent any

    stages {
        node('maven') {
            stage ('Get Image') {
                steps {
                    def maven = docker.image('maven:latest')
                    maven.pull()
                }
            }
            stage ('Compile Stage') {
                steps {
                    maven.inside {
                        sh 'mvn clean compile'
                    }
                }
            }

            stage ('Testing Stage') {
                steps {
                    maven.inside {
                        sh 'mvn test'
                    }
                }
            }


            stage ('Deployment Stage') {
                steps {
                    maven.inside {
                        sh 'mvn deploy'
                    }
                }
            }
        }
    }
}
