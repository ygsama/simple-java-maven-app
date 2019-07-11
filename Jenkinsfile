pipeline {
    agent {
        docker {
            // image 'maven:3-alpine' 
            image '10.2.21.95:10001/zj-gradle:4.10.3'
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
}
