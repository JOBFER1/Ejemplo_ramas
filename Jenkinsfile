pipeline{
    agent any
    tools{
        maven 'MAVEN_3_8_6'
        jdk 'JDK_11'
    }
    stages{
//        stage('Checkout') {
//            steps {
//                git branch: 'temp', url: 'https://github.com/JOBFER1/Ejemplo_ramas.git'
//            }
//        }
        stage ('Etapa master') {
            when {
                branch 'master'
            }
            steps {
                bat 'mvn -v'
                bat 'mvn clean package'
            }
        }
        stage ('Etapa temp') {
            when {
                branch 'temp'
            }
            steps {
                bat 'mvn -v'
                bat 'mvn clean package'
            }
        }        
    }
}