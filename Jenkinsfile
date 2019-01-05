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
       sh 'cp -r *.war /home/manju/Downloads/apache-tomcat-7.0.92/webapps'
    }
   }
 }
