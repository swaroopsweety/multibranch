pipeline {
    agent any

    stages {
        stage('continuous download') {
            steps {
                git 'https://github.com/AneesRavidKhan/DemoATR.git'
            }
        }
        stage('continuous build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('continuous deploy') {
            steps {
                sh 'sshpass -p "jeevan" scp target/DemoATR.war jeevan@172.17.0.4:/opt/apache-tomcat-9.0.56/webapps' 
            }
        }
    }
}

