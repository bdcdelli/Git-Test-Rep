pipeline {
    agent any

    stages {
        stage('Clone the repo') {
            steps {
                echo 'Clonning the repo'
                bat 'if exist Git-Test-Rep rmdir Git-Test-Rep /q /s'
                bat 'git clone https://github.com/bdcdelli/Git-Test-Rep.git'
            }
        }
        // stage('Execute python file') {
        //     steps {
        //         bat 'python Git-Test-Rep/Test_files/hello.py'
        //     }
        // }
        stage('Build') {
            steps {
                zip zipFile: 'Git-Test-Rep.zip', archive: False, dir: 'Git-Test-Rep', overwrite: 'true'
            }
        }
        
    }
}
