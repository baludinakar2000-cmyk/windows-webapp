pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'main',
                    credentialsId: 'git-creds',
                    url: 'https://github.com/baludinakar2000-cmyk/windows-webapp.git'
            }
        }
        stage('Deploy') {
            steps {
                bat '''
                    xcopy /E /I /Y . "C:\\inetpub\\wwwroot\\"
                '''
            }
        }
    }
}
