pipeline {
    agent any
    stages {
        stage('Build Step') {
            steps { 
                sh 'javac pip.java'
            }   
            }
        stage('Run Step') {
            steps { 
                sh 'java pip'
            }   
        }
    }
}
