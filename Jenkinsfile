pipeline {
    agent any
    
    tools{
        jdk 'jdk11'
        maven 'maven3'
    }
    
    stages {
        stage('Git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/vijkes/Petclinic.git'
            }
        }
        stage('compile') {
            steps {
                sh "mvn clean compile"
            }
        }

        stage('build') {
            steps {
                sh "mvn clean package -DskipTests=true"
            }
        }
        // stage('deploy') {
        //     steps {
        //         sh "cp target/*.war /opt/apache-tomcat-9.0.89/webapps"
        //     }
        // }
        // stage('Git checkout') {
        //     steps {
        //         git branch: 'main', url: 'https://github.com/vijkes/Petclinic.git'
        //     }
        // }
        // stage('Git checkout') {
        //     steps {
        //         git branch: 'main', url: 'https://github.com/vijkes/Petclinic.git'
        //     }
        // }
    }
}
