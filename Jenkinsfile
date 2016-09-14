node{
	stage 'checkout'
	checkout scm
	stage 'validate puppet files'
	sh 'ls'
	sh '/usr/local/bin/puppet-lint manifests/*.pp'
	stage 'build puppet file'
	echo 'sup world'
	stage 'test'
	echo 'Do test'
}
