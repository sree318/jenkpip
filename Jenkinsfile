pipeline {
    agent any
    stages {
        stage('Build Step') {
            steps { 
                bat 'javac pip.java'
            }   
            }
        stage('Run Step') {
            steps { 
                bat 'java pip'
            }   
        }
    }
}
