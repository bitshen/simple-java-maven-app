pipeline {
    agent {
        docker {
            image 'maven'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
    options {
        enforceMavenVersion('3.5.0+')
        enforceJavaVersion('1.8.0-131+')
    }
}
