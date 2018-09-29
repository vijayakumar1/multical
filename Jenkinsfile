node{
    stage('SCM Checkout'){
      git 'https://github.com/vijayakumar1/multical.git'
    }
    stage('Compile-Package'){
      def mvnHome = tool name: 'maven', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy-to-Tomcat'){
      sh 'cp -rf *Calculator-0.0.1-SNAPSHOT.war /home/manju/Downloads/tomcat7/webapps'
    }
}
