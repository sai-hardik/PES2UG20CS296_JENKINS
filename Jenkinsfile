pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS296-1 rand.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                shs './PES2UG20CS296-1'
            }
        }
        stage('Deploy') {
            steps {
               echo 'Deployed!'
           }
        }
     
    }
    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
