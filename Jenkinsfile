  node{
   stage('SCM Checkout'){
     git 'https://github.com/sohaib629/my-app'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'Maven3.6', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"

stage('Email Notification'){

	mail bcc: '', body: '''Hi, This is Sohaib\'s Jenkins Pipeline Job Notification.
	Thank you,
	Sohaib''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'sohaib.uft@gmail.com'

}

   }

}


