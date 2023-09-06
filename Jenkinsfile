pipeline{
    agent any
    stages{
        stage("Build"){
            steps {
                sh 'mvn clean package' 
            }
        }
        stage("Unit and Integration Tests"){
            steps{
                sh './JUnit Test'
                sh './Integration Test'
            }
        }
        stage("Code Analysis"){
            steps{
                echo "Deploying..."
            }
        }
        stage("Security Scan"){
            steps{
                echo "Completed..."
            }
        }
        stage("Deploy to Staging"){
            steps{
                echo "Completed..."
            }
        }
        stage("Integration Tests on Staging"){
            steps{
                echo "Completed..."
            }
        }
        stage("Deploy to Production'"){
            steps{
                echo "Completed..."
            }
        }
    }
}
