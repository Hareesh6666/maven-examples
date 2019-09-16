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
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn sonar:sonar \
        -Dsonar.projectKey=article370-maven \
        -Dsonar.organization=Hareesh6666 \
        -Dsonar.host.url=https://sonarcloud.io \
        -Dsonar.login=a4b161d57444f3b5f51f365322e49d613da40f76'
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
