pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                
                sh 'g++ -o PES1UG20CS643 PES1UG20CS643.cpp'
                build job: 'PES1UG20CS643-1'
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                
                sh './PES1UG20CS643'
                echo 'Test Stage Successful'
            }
        }

        stage('Deploy') {
            steps {
                
                
                echo 'Deployment Successful'
            }
        }
    }

    post {
      failure{
        echo 'Pipeline failed'
      }
        
    }
}