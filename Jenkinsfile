pipleline {
    agent { docker 'maven:3.5-alpine'}
    stages {
        stage ('Checkout') {
            steps {
                git 'https://github.com/spring-projects/spring-petclinic.git'
            }
        }
        stage ('Build') {
            step {
                bat 'mvn clean package'
                junit '**/target/surefire-reports/Test-*.xml'
            }
        }
    }
}