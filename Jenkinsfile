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

       stage('build') {
            steps {
                // Run Maven build
                echo 'mvn clean install'
            }
        }
            post {
                success {
                    // Actions to perform if buld is a success
                    echo 'build Successful!!'
                }
            }
        }
    }
}
        

