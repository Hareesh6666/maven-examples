node {
   
   stage('Code Checkout') { // for display purposes
      git url: 'https://github.com/itrainarticle370/maven-examples.git'
   }
   stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn clean compile'
     } 
   }
   stage('UnitTest run') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn test'
     }   
   }
   stage('Code Quality') {
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn sonar:sonar \
  -Dsonar.projectKey=Hareesh_article370 \
  -Dsonar.organization=article \
  -Dsonar.host.url=https://sonarcloud.io \
  -Dsonar.login=67f9dd3b20178dbbed56938e2afb000ab3e7216e
     }    
      
   }
   stage('Archival repo') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
     sh 'mvn package'
     }   
   }
   stage('Docker Build') {
      
   }
   stage('Deploy to Prod') {
      
   }
   
}
