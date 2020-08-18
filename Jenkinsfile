pipeline {
    agent any
    stages {
        
        stage('build') {
            tools {
                jdk 'jdk-11.0.6'
                maven 'apache-maven-3.6.1'
            }
            steps {
                powershell label: '', script: 'mvn clean package -f spring-boot-samples/spring-boot-sample-atmosphere/pom.xml'
                // echo "built"
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
