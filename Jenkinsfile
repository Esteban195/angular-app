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

        stage('Dependencies Installation') {
            steps {
                bat "npm install"
            }
        }    

        stage('Lint Test Execution') {
            steps {
                bat "ng lint"
            }
        }

        stage('Unit Test Execution') {
            steps {
                bat "ng Test"
            }
        } 

        stage('Build Execution') {
            steps {
                bat "ng Build"
            }
        }
        stage('Deploy Aplication'){
            when {
                branch 'prod'
            }
            steps {
                bat "xcopy dist\\clase6 C:\\inetpub\\wwwroot\\romell\\dev /s /y"
            }
        }
    }
}
