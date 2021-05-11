pipeline {
    agent any
    stages { 
        stage('Build') {
           steps {
                echo 'Starting build'
                
                sh "pip3 install -r requirements.txt"

            }
        }
        stage('Test') {
            steps {
                echo 'Starting Testing '
                sh "python test.py"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Starting deployment '
                sh "python main.py"
            }
        }
        stage('Release') {
            steps {
                echo 'Starting Release'
            }
        }
    }
}
