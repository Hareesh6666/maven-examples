node {
   
   stage('Code Checkout') { // for display purposes
      git url: 'https://github.com/Hareesh6666/maven-examples.git'
    }
   stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn clean compile'
       mvn sonar:sonar \
  -Dsonar.projectKey=Hareesh6666 \
  -Dsonar.organization=hareesh6666 \
  -Dsonar.host.url=https://sonarcloud.io \
  -Dsonar.login=bc03a466b583f876ad6a4505c6988f357ebf10ed
     } 
   }
   stage('UnitTest run') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn test'
     }   
   }
   stage('Code Quality') {
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
   
     }    
      
   }
   stage('Archival repo') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn package'
     }   
   }
   stage('Docker Build') {
      
   }
   stage('Deploy to Prod') {
      
   }
   
}
