pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // integrating git and jenkins
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/riya5498/PythonP.git']]])
            }
        }
        stage('Build'){
            steps{
                //fetch code from git first
                git 'https://github.com/riya5498/PythonP.git'
                sh 'python3 app.py'
            }
        }
    }
}
