pipeline {
    agent {
        label 'linux_node3'
    }
    triggers{
	cron('H/2 * * * *')    
    }	
    stages {
        stage('Build') {
            steps {
                dir('D:/Jenkin2024/test.bat') {
                    /* execute commands in the scripts directory */
                }
            bat 'D:/Jenkin2024/test.bat'
            }
        }
        stage('Test') {
			agent {
                label 'linux_node2'
            }
            steps {
                dir('D:/Jenkin2024/test.bat') {
                    /* execute commands in the scripts directory */
                }
                bat 'D:/Jenkin2024/test.bat'
            }
        }
      stage('Package') {
            steps {
                dir('D:/Jenkin2024/test.bat') {
                    /* execute commands in the scripts directory */
                }
                bat 'D:/Jenkin2024/test.bat'
            }
        }
        stage('Deploy') {
            steps {
                dir('D:/Jenkin2024/test.bat') {
                    /* execute commands in the scripts directory */
                }
                bat 'D:/Jenkin2024/test.bat'
            }
        }
	stage('Production') {
            steps {
                dir('D:/Jenkin2024/test.bat') {
                    /* execute commands in the scripts directory */
                }
                bat 'D:/Jenkin2024/test.bat'
            }
        }
    }
}


