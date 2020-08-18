pipeline {
    agent any
    stages {
        
        stage('build') {
            steps {
                echo "built"
               // checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/prayag5198/Spring-boot_App.git']]])
            }
        }
        
        stage('archive') {
            steps {
                echo "archived"
            }
        }
        
        stage('publist JUnit') {
            steps {
                echo "published"
            }
        }
        
        stage('publish HTML') {
            steps {
                echo "published"
            }
        }
      
    }
}
