node{
	stage 'checkout'
	checkout scm
	stage 'validate puppet files'
	sh 'ls'
	//sh '/usr/local/bin/puppet-lint manifests/*.pp'
	stage 'Run spec test'
	sh 'echo "$PATH"'
	sh 'export PATH=$PATH:/usr/local/bin'
	//sh 'source /usr/local/bin/'
	sh 'ruby -v'
	//sh 'rails generate rspec:install'
	sh '/usr/local/bin/rspec spec'  
	echo 'sup world'
	stage 'test'
	echo 'Do test'
}
