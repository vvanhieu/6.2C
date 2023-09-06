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
        stage("Deploy"){
            steps{
                echo "Deploying..."
            }
        }
        stage("Complete"){
            steps{
                echo "Completed..."
            }
        }
    }
}
