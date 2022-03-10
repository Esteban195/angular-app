pipeline {
    agent {
        label "windows-worker"
    }

    stages {
        stage('Angulara Verification') {
            steps {
                bat "ng version"
            }
        }

    stages {
        stage('Dependencies Installation') {
            steps {
                bat "npm install"
            }
        }    

    stages {
        stage('Lint Test Execution') {
            steps {
                bat "ng lint"
            }
        }

    stages {
        stage('Unit Test Execution') {
            steps {
                bat "ng Test"
            }
        } 

    stages {
        stage('Build Execution') {
            steps {
                bat "ng Build"
            }
        }
        stage('Deploy Aplication'){
            when {
                branch 'main'
            }
            steps {
                bat "xcopy dist\\clase6 C:\\inetpub\\wwwroot\\romell\\dev /s /y"
            }
        }
    }
}