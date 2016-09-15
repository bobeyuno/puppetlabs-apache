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
	//stage 'tag'
	//sh 'env'
	//sh 'git remote set-url origin git@github.com:bobeyuno/puppetlabs-apache.git && git tag 0.0.$BUILD_NUMBER && git push origin --tags'

	stage 'Update control repo'
	sh '''#!/bin/bash -l
	cd ../
	if [ ! -d control_repo ]; then
			git clone -b development git@github.com:bobeyuno/control_repo.git
	fi
	git checkout development
	git pull	
	cd control_repo
	less Puppetfile
	sed s/:tag => '[0-9].[0-9].[0-9]'/:tag => '0.0.$BUILD_NUMBER/' Puppetfile
	less Puppetfile
	'''
}
