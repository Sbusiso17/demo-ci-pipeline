pipeline {
    agent any
  
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
        }

        stage('Build') {
            steps {
                // Run Maven build
                echo 'mvn clean install'
            }
        }
    }
    
    post {
        success {
            // Actions to perform if build is a success
            echo 'Build Successful!!'
        }
    }
}
                   

