node{
    stage('SCM Checkout'){
      git 'https://github.com/vijayakumar1/multical.git'
    }
    stage('Compile-Package'){
      def mvnHome = tool name: 'maven', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy-to-Tomcat'){
      sh 'cp $/var/lib/jenkins/workspace/newpipeline/target https://localhost:8090:/Downloads/tomcat7/webapps'
    }
}
