
pipeline {
     agent { label 'master' }
     tools {
          maven 'Maven 3.6.1'
     }
     stages {
          stage('Source') {
               steps {
                    git branch: 'master',
                         url: 'https://github.com/panda09/evoting-1.git'
               }
          }
          stage('Build') {
               steps {
                    sh 'mvn compile'
               }
          }
          stage('Test') {
               steps {
                    sh 'mvn test'
               }
          }
          stage('Deploy') {
               steps {
                    sh 'mvn spring-boot:run'
               }
          }
     }
}
