pipeline {
    agent any
    
    environment {
        DOCKER_IMAGE_NAMES = 'frontend auth classrooms event-bus post images'
        DOCKER_IMAGE_REPOS = 'ushna1923/frontend-image ushna1923/auth-image ushna1923/classrooms-image ushna1923/event-bus-image ushna1923/post-image ushna1923/images-image'
    }
    
    stages {
        stage('i211225_Checkout') {
            steps {
                // Checkout code from GitHub repository
                git 'https://github.com/NUCESFAST/scd-final-lab-exam-Ushna-Nadeem.git'
            }
        }
        
        stage('i211225_Install_Dependencies') {
            steps {
                // Install dependencies for your application
                script {
                    docker.image('node:14-alpine').inside('-v $PWD:/app') {
                        sh 'npm install'
                    }
                }
            }
        }
        
        stage('i211225_Build_and_Push_Images') {
            steps {
                script {
                    def imageNames = DOCKER_IMAGE_NAMES.split(' ')
                    def imageRepos = DOCKER_IMAGE_REPOS.split(' ')
                    
                    for (int i = 0; i < imageNames.size(); i++) {
                        docker.build(imageRepos[i] + ':latest', '-f ' + imageNames[i] + '/Dockerfile .')
                        docker.withRegistry('https://registry.hub.docker.com', 'e16fa279-f0bf-4bed-bd20-eeefaed24468') {
                            docker.image(imageRepos[i] + ':latest').push()
                        }
                    }
                }
            }
        }
    }
}
