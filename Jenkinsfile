node{
	stage 'checkout'
	checkout scm
	stage 'validate puppet files'
	sh 'env'
	sh 'who; puppet-lint manifests/*.pp'
	stage 'Run spec test'
	sh 'rspec spec'  
	echo 'sup world'
	stage 'test'
	echo 'Do test'
}
