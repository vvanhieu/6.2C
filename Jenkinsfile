pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                sh 'mvn clean package'
            }
        }

        stage("Unit and Integration Tests") {
            steps {
                sh 'mvn test'
                sh 'your_integration_test_command'
            }
        }

        stage("Code Analysis") {
            steps {
                sh 'mvn sonar:sonar'
            }
        }

        stage("Security Scan") {
            steps {
                sh 'your_security_scan_command'
            }
        }

        stage("Deploy to Staging") {
            steps {
                sh 'aws s3 cp your-app.jar s3://staging-bucket/'
            }
        }

        stage("Integration Tests on Staging") {
            steps {
                sh 'your_integration_test_command_on_staging'
            }
        }

        stage("Deploy to Production") {
            steps {
                sh 'aws s3 cp your-app.jar s3://production-bucket/'
            }
        }
    }

    post {
        success {
            echo 'Deployment to production successful!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
