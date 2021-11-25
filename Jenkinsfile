node {

    stage ('git'){
        git branch: 'J2EE', credentialsId: 'githubrepo', url: 'https://github.com/venkatareddychinnapareddy/onlinebookstore.git'
    }
     
    stage ('compile'){
        sh 'mvn clean compile'
    }
    
     stage ('Test'){
        sh 'mvn test'
    }
   
    stage ('package'){
        sh 'mvn package'
    }
    
    stage('Deploy'){
          
        sh 'cp /root/.jenkins/workspace/Bookstore_scripted_pipeline/target/*.war /opt/apache-tomcat-8.0.52/webapps'
    } 
    
}
