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
                dir("test-go-app"){
                    sh("ls -l")
                    sh("go build helloWorld.go")
                }
            }
        }
    }
}
