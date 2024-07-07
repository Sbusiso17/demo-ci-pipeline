pipeline {
    agent any
    
    tools {
        maven 'Maven 3.8.4' // Use the Maven version configured in Jenkins
    }
    
    stages {         
        stage('Validate') {
            steps {
                // Run Maven build
                echo 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                // Run Maven tests
                echo 'mvn test'
            }

       stage('build') {
            steps {
                // Run Maven build
                echo 'mvn clean install'
            }
        }
            post {
                always {
                    // Archive test results
                    junit '**/target/surefire-reports/TEST-*.xml'
                }
            }
        }
        
        stage('Archive') {
            steps {
                // Archive the built artifacts
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
    }
}
