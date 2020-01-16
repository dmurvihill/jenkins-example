docker.image('maven:latest').inside {
    sh 'mvn clean compile'
    sh 'mvn test'
    sh 'mvn deploy'
}
