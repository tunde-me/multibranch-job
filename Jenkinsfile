pipeline {
    agent any
    stages{
        stage('system statistics and Jenkins status check'){
            parallel{
                stage('systems statistics'){
                    steps{
                        sh "lscpu"
                    }
                }
                stage('Jenkins status check'){
                    steps{
                        sh "grep -i jenkins /etc/passwd"
                    }
                }
            }
        }
        stage('End of parallel build'){
            steps{
                echo "End of pipeline"
            }
        }
    }
}

