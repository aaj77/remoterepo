pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               bat "rmdir  /s /q automation_scripts"
                bat "git clone https://stash.intranet.qualys.com/scm/~aljadhav/automation_scripts.git"
                bat "mvn clean -f automation_scripts"
            }
        }
        stage('install') {
            steps {
                bat "echo 01_install-%date%_%time% >> jb/file1.txt"
            }
        }
        stage('test') {
            steps {
                bat "echo 02_test-%date%_%time% >> jb/file1.txt"
            }
        }
        stage('package') {
            steps {
                bat "echo 03_package-%date%_%time% >> jb/file1.txt"
            }
        }
    }
}
