node{
	stage 'checkout'
	checkout scm
	//stage 'Run puppet-lint'
	//sh '''#!/bin/bash -l
	//ruby -v
	//puppet-lint manifests/*.pp
	//'''
	stage 'Run spec test'
	sh '''#!/bin/bash -l
	ruby -v
	rspec spec
	''' 
	stage 'test'
	echo 'Do test'
}
