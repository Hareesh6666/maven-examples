node {
   
   stage('Code Checkout') { // for display purposes
      git url: 'https://github.com/Hareesh6666/maven-examples.git'
    }
   stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn clean compile'
  mvn sonar:sonar \
  -Dsonar.projectKey=Hareesh6666 \
  -Dsonar.organization=Hareesh6666 \
  -Dsonar.host.url=https://sonarcloud.io \
  -Dsonar.login=2419a7774f0ee749c84ed158a4ec7ce1bd2e2b3c
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
