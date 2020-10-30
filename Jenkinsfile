pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/target/*.war', fingerprint: true)
        sh '''mkdir /home/javademos/buildoutput/${BUILD_NUMBER}
CP /var/lib/jenkins/workspace/javademos_master/javademos-master/ssgsems/target/*.war /home/javademos/buildoutput/${BUILD_NUMBER}'''
      }
    }

  }
}