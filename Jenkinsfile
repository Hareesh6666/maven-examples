node {
   
   stage('Code Checkout') { // for display purposes
git 'https://github.com/Hareesh6666/maven-examples.git'
   }
   stage('Build') {
    withMaven(jdk: 'JDK', maven: 'Apache Maven 3.6.3') {
     sh 'mvn clean compile'
     } 
   }
   stage('UnitTest run') {
    withMaven(jdk: 'JDK', maven: 'Apache Maven 3.6.3') {
     sh 'mvn test'
     }   
   }
   stage('Code Quality') {
     withMaven(jdk: 'JDK', maven: 'Apache Maven 3.6.3') {
     sh 'mvn sonar:sonar \
  -Dsonar.projectKey=hareesh66666 \
  -Dsonar.organization=hareesh66666 \
  -Dsonar.host.url=https://sonarcloud.io \
  -Dsonar.login=5f77d28913802ad3dd9e9b8f0b59eaa481c76c5b'
     }    
      
   }
   stage('Archival repo') {
    withMaven(jdk: 'JDK', maven: 'Apache Maven 3.6.3') {
     sh 'mvn package'
     }   
   }
   stage('Docker Build') {
      
   }
   stage('Deploy to Prod') {
      
   }
   
}
