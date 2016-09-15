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
	//sh 'env'
	sh 'git remote set-url origin git@github.com:bobeyuno/puppetlabs-apache.git && git tag 0.0.$BUILD_NUMBER && git push origin --tags'

	stage 'Update control repo'
	sh '''#!/bin/bash -l
	cd ../
	if [ ! -d control_repo_working ]; then
			git clone -b development git@github.com:bobeyuno/control_repo.git control_repo_working
	fi
	cd control_repo_working
	git checkout development
	git pull	
	//less Puppetfile
	sed "s/[0-9].[0-9].[0-9]*/0.0.$BUILD_NUMBER/" <Puppetfile > Puppetfile.new
	mv -f Puppetfile.new Puppetfile
	less Puppetfile
	git add Puppetfile && git commit -m "Auto-Commit # Upgrading module" && git push origin 
	'''
}
