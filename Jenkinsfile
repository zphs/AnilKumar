pipeline {
    agent any
   tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven 3.9.4"
    } 
   
    stages {
        stage('GitCodeCheckOut') {
            steps {
                git branch: 'main', url: 'https://github.com/Sakaleelasatish/AnilKumar.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean deploy'
            }
        }
       /* stage('ImageBuild') {
            steps {
                sh 'docker build -t mannem302/tomcat:$BUILD_ID .'
            }
        }
        stage('Dockerhublogin') {
            steps {
                withCredentials([usernameColonPassword(credentialsId: 'dockerhub', variable: 'DOCKER')]) {
              sh 'docker login'
        }
            }
        }
        stage('Dockerhubpush') {
            steps {
                sh 'docker push mannem302/tomcat:$BUILD_ID'
            }
        }
        stage('RunContainer') {
            steps {
                
                sh 'docker run -itd --name mywebapp$BUILD_ID  -p 8082:8080 mannem302/tomcat:$BUILD_ID'
            }
        }*/
        
    }
}
