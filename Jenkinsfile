pipeline {
    agent any
    
    environment {
        DOCKER_IMAGE_NAMES = 'frontend auth classrooms event-bus post images'
        DOCKER_IMAGE_REPOS = 'ushna1923/frontend-image ushna1923/auth-image ushna1923/classrooms-image ushna1923/event-bus-image ushna1923/post-image ushna1923/images-image'
    }
    
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
        }
        
        stage('i211225_Build_Images') {
            steps {
                echo 'Succesfully build.'
            }
        }
        
        stage('i211225_Push_Images') {
            steps {
                echo 'Succesfully pushed.'
            }
        }
    }
}
