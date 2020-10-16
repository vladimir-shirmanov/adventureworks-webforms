pipeline {
    agent any
    
    environment {
        MS_BUILD = 'C:\\Program Files (x86)\\MSBuild\\14.0\\Bin\\MSBuild.exe'
    }

    stages {
        stage('Build') {
            environment {
                PLATFORM='any cpu'
            }
            steps {
                bat "\"${env.MS_BUILD}\" AdventureWorks.sln -p:Platform=${env.PLATFORM} -p:Configurations=Debug"
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}