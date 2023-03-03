pipeline {
    agent any
    stages {
        
        //Checkout the code
        stage("Preparation") {
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/pocketaces2/pipeline_trigger']]])
            }
        }

        stage('Do some logic') {
            steps {
                sh "echo Running some random logic to mimic a job or service"
            }
            
        }
        
        stage('Automation tests') {
            steps {
               build 'Simple service pipeline'
            }

            
        }
    }
}
