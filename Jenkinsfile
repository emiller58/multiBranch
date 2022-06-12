pipeline {
    agent any
    tools {
        maven 'mvn-353'
    }
    stages {
        stage ('Compile Stage') {

            steps {                
                    bat 'mvn clean compile'                
            }
        }

        stage ('Testing Stage') {

            steps {                
                    bat 'mvn test -fn'                
            }
        }  
        stage('Publish test results') {
             steps {
                junit '**/target/surefire-reports/TEST-*.xml'
              }
        } 
      
    } 

}
