timestamps {
    
environment {
       env.PATH = env.PATH + ";c:\\Windows\\System32"
    
}

node () {

	stage ('Memorama - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'chiki1', url: 'https://github.com/chikimoco/Memorama.git']]]) 
	}
	stage ('Memorama - Build') {
 			// Batch build step
bat 'phpunit core/test/'
fileOperations([fileCopyOperation(excludes: '', flattenFiles: false, includes: '**', targetLocation: 'C:\\wamp64\\www\\MemoDeploy')])
	}
}
}