pipeline {
    agent any

    tools {
        maven 'localMAVEN'
    }

    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
                sh "sudo /usr/local/bin/docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
    }
}