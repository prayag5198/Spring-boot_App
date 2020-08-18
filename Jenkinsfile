pipeline {
    agent any
    stages {
        
        stage('build') {
            tools {
                jdk 'jdk8'
                maven 'Maven'
            }
            steps {
                powershell label: '', script: 'mvn clean package -f spring-boot-samples/spring-boot-sample-atmosphere/pom.xml'
                // echo "built"
               // checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/prayag5198/Spring-boot_App.git']]])
            }
        }
        
        stage('archive') {
            steps {
                archive 'spring-boot-samples/spring-boot-sample-atmosphere/target/*.jar'
                //echo "archived"
            }
        }
        
        stage('publist JUnit') {
            steps {
                junit 'spring-boot-samples/spring-boot-sample-atmosphere/target/surefire-reports/*.xml'
                //echo "published"
            }
        }
        
        stage('publish HTML') {
            steps {
                publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'spring-boot-samples/spring-boot-sample-atmosphere/target/site/jacoco', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: ''])
                //echo "published"
            }
        }
      
    }
}
