node{
    stage('SCM Checkout'){
      git 'https://github.com/vijayakumar1/multical.git'
    }
    stage('Compile-Package'){
      def mvnHome = tool name: 'Maven', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy-to-Tomcat'){
        ws('/var/lib/jenkins/workspace/jenkinsjob1/target'){
      sh 'cp -r *.war /home/manju/Downloads/tomcat7/webapps'
        }
    }
}
