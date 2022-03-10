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
                bat "ng test"
            }
        } 

        stage('Build Execution') {
            steps {
                bat "ng build"
            }
        }
        stage('Deploy Aplication'){
            when {
<<<<<<< HEAD
                branch 'dev'
            }
            steps {
                bat "xcopy dist\\clase6 C:\inetpub\wwwroot\edgar\dev  /s /y"
=======
                branch 'prod'
            }
            steps {
                bat "xcopy dist\\clase6 C:\inetpub\wwwroot\edgar\prod /s /y"
>>>>>>> e651f1458adbe222105a363316b5d99e674af98a
            }
        }
    }
}
