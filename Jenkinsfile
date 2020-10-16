pipeline {
    agent any
    
    environment {
        MS_BUILD = 'C:\\Program Files (x86)\\MSBuild\\14.0\\Bin\\MSBuild.exe'
        NUGET = 'C:\\Program Files (x86)\\NuGet\\nuget.exe'
    }

    stages {
        stage('Build') {
            environment {
                PLATFORM='any cpu'
            }
            steps {
                echo 'Restoring nuget packages'
                bat "\"${env.NUGET}\" restore AdventureWorks.sln"
                echo 'building solution'
                bat "\"${env.MS_BUILD}\" AdventureWorks.sln -p:Platform=\"${env.PLATFORM}\" -p:Configurations=Debug"
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