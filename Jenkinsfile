node{
	stage 'checkout'
	checkout scm
	stage 'validate puppet files'
	sh 'ls'
	#sh '/usr/local/bin/puppet-lint manifests/*.pp'
	stage 'Run spec test'
	sh '/usr/local/bin/rspec spcec'  
	echo 'sup world'
	stage 'test'
	echo 'Do test'
}
