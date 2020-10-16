pipeline {
    agent any
    
    environment {
        MSBuild = 'C:\Program Files (x86)\MSBuild\14.0\Bin\MSBuild.exe'
    }

    stages {
        stage('Build') {
            environment {
                PLATFORM='any cpu'
            }
            steps {
                bat '${env.MSBuild} AdventureWorks.sln -p:Platform=${env.PLATFORM} -p:Configurations=Debug'
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