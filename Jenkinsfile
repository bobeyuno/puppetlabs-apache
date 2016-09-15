node{
	stage 'checkout'
	checkout scm
	//stage 'Run puppet-lint'
	//sh '''#!/bin/bash -l
	//ruby -v
	//puppet-lint manifests/*.pp
	//'''
	//stage 'Run spec test'
	//sh '''#!/bin/bash -l
	//ruby -v
	//bundle install
	//bundle exec rake spec
	//bundle exec rspec spec/acceptance
	//RS_DEBUG=yes bundle exec rspec spec/acceptance


	//''' 
	stage 'tag'
	git tag -a $BUILD_NUMBER
}
