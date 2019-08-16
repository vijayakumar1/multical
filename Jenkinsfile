node{
    stage('SCM Checkout'){
      git 'https://github.com/vijayakumar1/multical.git'
    }
    stage('Compile-Package'){
      def mvnHome = tool name: 'Maven', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy-to-Tomcat'){
       ws('/home/vijay/.jenkins/workspace/mypip/target'){
       sh 'cp -r *.war /home/vijay/softwares/apache-tomcat-8.5.35/webapps:'
    }
   }
 }
