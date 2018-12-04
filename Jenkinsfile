node{
    stage('SCM Checkout'){
      git 'https://github.com/vijayakumar1/multical.git'
    }
    stage('Compile-Package'){
      def mvnHome = tool name: 'Maven', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy-to-Tomcat'){
       ws('/home/manju/.jenkins/workspace/job2/target'){
       sh ‘cp -r *.war /etc/tomcat7/webapps’
    }
    }
}
