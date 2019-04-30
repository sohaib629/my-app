properties([parameters([choice(choices: 'develop\nfeature-1\nfeature-2\nfeature-3\nmaster', description: 'Select the Branch to Build', name: 'branch')])])

node{
   stage('SCM Checkout'){
    echo "Pulling changes from the branch ${params.branch}"
    git url: 'https://github.com/sohaib629/my-app', branch: "${params.branch}"
     
   }
  
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'Maven3.6', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"

   }

}
