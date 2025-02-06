pipeline {
    agent any
  
    stages {
        stage('Workspace cleanup') {
            steps {
                cleanWs()
            }
	}
        stage('clone') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], browser: github('https://github.com/Brunda9/eShopOnWeb.git'), extensions: [], userRemoteConfigs: [[credentialsId: 'test_git', url: 'https://github.com/Brunda9/eShopOnWeb']])
            }
        }
    
    
    stage('Build') {
            steps {
                // Build the project (replace with your .csproj or .sln file path)
                script {
                    sh 'dotnet build eShopOnWeb.sln.sln --configuration Release'  // Build the solution or specific project
                }
            }
        }
   }
}
