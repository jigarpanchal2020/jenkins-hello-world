pipeline {
    agent any
    tools{
        maven 'M3912'
    }

    stages {
        stage('Echo version') {
            steps {
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
        }
        stage('Build'){
            steps{
                //git branch: 'main', changelog: false, poll: false, url: 'https://github.com/jigarpanchal2020/jenkins-hello-world.git'
                sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Unit Test'){
            steps{
                sh 'mvn test'
            }
        }
        
    }
}
