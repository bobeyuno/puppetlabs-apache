node{
	stage 'checkout'
	checkout scm
	sh '''#!/bin/bash -l
	ruby -v
	puppet-lint manifests/*.pp
	'''
	stage 'Run spec test'
	sh 'rspec spec'  
	echo 'sup world'
	stage 'test'
	echo 'Do test'
}
