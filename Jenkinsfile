pipleline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                git 'https://github.com/mindtree-sumit/spring-petclinic.git'
            }
        }
        stage ('Build') {
            stepa {
                bat 'mvn clean package'
                junit '**/target/surefire-reports/Test-*.xml'
            }
        }
    }
}
