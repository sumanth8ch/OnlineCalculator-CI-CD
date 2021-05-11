pipeline {
    agent any
    stages { 
        stage('Build') {
           steps {
                echo 'Starting build'
                sh "/usr/local/bin/virtualenv -p /usr/bin/python3 work"
                sh "source work/bin/activate"
                sh "pip3 install --user -r requirements.txt"
            }
        }
        stage('Test') {
            steps {
                echo 'Starting Testing '
                sh "export PYTHONPATH=/usr/local/bin/flask"
                sh "python3 test.py"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Starting deployment '
                sh "FLASK_APP=main.py /usr/local/bin/flask run &"
            }
        }
        stage('Release') {
            steps {
                echo 'Starting Release'
            }
        }
    }
}
