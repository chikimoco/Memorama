// Powered by Infostretch 

timestamps {

node () {

	stage ('Memorama - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'chiki1', url: 'https://github.com/chikimoco/Memorama.git']]]) 
	}
	stage ('Memorama - Build') {
 			// Batch build step
bat """ 
phpunit core/test/ 
 """ 
	}
	stage ('Deploy Memorama - Build') {
 	
// Unable to convert a build step referring to "hudson.plugins.ws__cleanup.PreBuildCleanup". Please verify and convert manually if required.
// Unable to convert a build step referring to "hudson.plugins.copyartifact.CopyArtifact". Please verify and convert manually if required. 
	}
}
}