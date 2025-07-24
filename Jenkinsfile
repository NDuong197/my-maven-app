pipeline {
    agent any
    tools {
        maven 'Maven 3.8.6'
        jdk 'JDK21'   // Hoặc JDK11 nếu bạn đã cấu hình sẵn tên đó
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
    post {
        always {
            junit 'target/surefire-reports/*.xml'
        }
    }
}
