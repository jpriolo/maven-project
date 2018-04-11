pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh '/usr/local/Cellar/maven/3.5.3/libexec/bin/mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
