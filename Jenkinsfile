pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''echo "Hello, World!"
mvn -f ssgsems/pom.xml -B -DskipTests clean package'''
      }
    }

  }
}