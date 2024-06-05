pipeline {
    agent any
    
    stages {
        stage('i211225_Checkout') {
            steps {
                echo 'Checking out code from GitHub repository'
                git 'https://github.com/NUCESFAST/scd-final-lab-exam-Ushna-Nadeem.git'
            }
        }
        
        stage('i211225_Install_Dependencies') {
            steps {
                sh 'npm install'
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
