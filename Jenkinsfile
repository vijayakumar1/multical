node{
    stage('SCM Checkout'){
      git 'https://github.com/vijayakumar1/multical.git'
    }
    stage('Compile-Package'){
      def mvnHome = tool name: 'maven', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
    }
    stage('deploy-to- tomcat'){
       def deploy(war, id) 
       sh "cp ${Calculator-0.0.1-SNAPSHOT.war} /tmp/webapps/${02d2386a-3175-49f3-b931-8106bf3802ee}.war"
    }
}
