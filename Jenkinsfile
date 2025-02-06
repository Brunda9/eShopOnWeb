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
    
    
    //     stage('Build') {
    //         steps {
    //     sh 'npm install'
    //   }
    // }

}
}
