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
        stage("build"){
            steps{
                sh("pwd")
                sh("ls -l")
                dir("test-go-app"){
                    sh("pwd")
                    sh("ls -l")
                    sh("go build helloWorld.go")
                }
            }
        }
    }
}
