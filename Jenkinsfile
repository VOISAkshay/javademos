pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**target/*.war', fingerprint: true)
        sh '''mkdir /home/javademos/buildoutput/${BUILD_NUMBER}
CP **/target/*.war /home/javademos/buildoutput/${BUILD_NUMBER}'''
      }
    }

  }
}