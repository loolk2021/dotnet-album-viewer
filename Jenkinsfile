pipeline {
    agent {
        label 'linux_node3'
    }
    /*triggers{
	cron('H/3 * * * *')    
    }
   environment {
        // Define environment variables here
        JDK = "value"
        ANOTHER_VARIABLE = "another value"
        // You can also use expressions or function calls
        PATH_TO_TOOL = tool 'ToolName'
    }*/	
    stages {
	stage('Parallel') {
            parallel {
                stage('Task One') {
                    steps {
                        echo 'Task One...'
                        // Compile your code here
                    }
                }
                stage('Task Two') {
                    steps {
                        echo 'Running task two...'
                        // Run unit tests here
                    }
                }
                stage('Task Three') {
                    steps {
                        echo 'Running Task Three...'
                        // Run integration tests here
                    }
                }
            }
        }   
        stage('Build') {
            steps {
                dir('D:/Jenkin2024/test.bat') {
                    /* execute commands in the scripts directory */
                }
		//echo '%BUILD_NUMBER%'
		echo "Build number is: ${env.BUILD_NUMBER}"
		
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


