  node{
   stage('SCM Checkot'){
     git 'https://github.com/sohaib629/my-app'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'Maven3.6', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"

   }

}


