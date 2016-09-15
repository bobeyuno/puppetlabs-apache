node{
	stage 'checkout'
	checkout scm
	stage 'validate puppet files'
	sh 'ruby -v'
	sh 'rvm use "ruby@gemset"; who; puppet-lint manifests/*.pp'
	stage 'Run spec test'
	sh 'rspec spec'  
	echo 'sup world'
	stage 'test'
	echo 'Do test'
}
