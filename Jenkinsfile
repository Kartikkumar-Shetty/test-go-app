pipeline{
    agent any
    tools { go 'go1.22.2' }

    stages{
        stage("Start"){
            steps{
                echo 'This is the start of the jenkins job'
                sh 'go version'
                deleteDir()
            }
        }
        stage("clone"){
            steps{
                echo 'This is the start of the jenkins job'
                echo 'cloning my repo'
                dir("mycode"){
                    sh "git clone https://github.com/Kartikkumar-Shetty/test-go-app"
                }
            }
        }
        stage("build"){
            steps{
                dir("mycode/test-go-app"){
                    sh("ls -l")
                    sh("go build helloWorld.go")
                }
            }
        }
    }
}
