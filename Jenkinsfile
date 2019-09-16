node {
   
   stage('Code Checkout') { // for display purposes
git credentialsId: 'fb9baf09-ae79-45be-8ee2-2109f9627c7b', url: 'https://github.com/Hareesh6666/maven-examples.git'
   }
   stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn clean compile'
     } 
   }
   stage('UnitTest run') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn test'
     }   
   }
   stage('Code Quality') {
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn sonar:sonar \
  -Dsonar.projectKey=hareesh66666 \
  -Dsonar.organization=hareesh66666 \
  -Dsonar.host.url=https://sonarcloud.io \
  -Dsonar.login=5f77d28913802ad3dd9e9b8f0b59eaa481c76c5b'
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
