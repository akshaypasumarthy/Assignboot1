pipeline{
    agent any

        tools {
             jdk 'java.home'
        maven 'maven3.6'
    }
//spring mvc
    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'akshay', url: 'https://github.com/akshaypasumarthy/Assignboot1.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn clean package'
            }
        }
    }
}
