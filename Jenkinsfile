pipeline {
    agent any
    
   tools {
      maven 'Maven 3.8.1'
    }
    stages {
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }  
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }  
        }    
      stage('deploy') {
            steps {
                sh 'java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App'
            }  
        }    
    }
}
