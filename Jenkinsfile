pipeline {
    agent any
    stages { 
        stage('Build') {
           steps {
                echo 'Starting build'
                sh "mkvirtualenv myenv --python=python3.6"
                sh "workon myenv"
                sh "python3.6 -m venv ~/Workspace/venvs/my_venv"
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
