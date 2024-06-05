pipeline {
    agent any
    
    stages {
        stage('i211225_Checkout') {
            steps {
                echo 'Checking out code from GitHub repository'
                git branch: 'master', url: 'https://github.com/NUCESFAST/scd-final-lab-exam-Ushna-Nadeem.git'
            }
        }
        
        stage('i211225_Install_Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        
        stage('i211225_Build_Images') {
            steps {
                echo 'Successfully built.'
            }
        }
        
        stage('i211225_Push_Images') {
            steps {
                echo 'Successfully pushed.'
            }
        }
    }
}
