pipeline{
    agent any
    stages{
        stage("clone the repo"){
            steps{
                    checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'http://github.com/rajkiet2007/tarpeedo']]) 
                }
        }
        stage("mvn validate"){
            steps{
                sh "mvn validate"
            }
        }
        stage("test"){
            steps{
                sh "mvn test"
            }
        }
        stage("clean install"){
            steps{
                sh "mvn clean install"
                echo "installed the packages"
            }
            
        }
    }
}