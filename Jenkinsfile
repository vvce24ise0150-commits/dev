
steps {
    checkout scm
}

    stages {

        stage('Build') {
            steps {
                echo 'Checking Python application'
                bat 'python -m py_compile app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Checking application'
                bat 'python --version'
            }
        }

        stage('Run Application') {
            steps {
                echo 'Running Python application'
                bat 'python app.py'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline completed successfully'
        }

        failure {
            echo 'CI Pipeline failed'
        }
    }
}
