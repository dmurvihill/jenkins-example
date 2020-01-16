pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                sh 'echo "hello compiler!"'
            }
        }

        stage ('Testing Stage') {

            steps {
                sh 'echo "hello test suite!"'
            }
        }


        stage ('Deployment Stage') {
            steps {
                    sh 'echo "hello deployment environment!"'
            }
        }
    }
}
