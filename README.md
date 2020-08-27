# Website for matrix-library

This website is used to host some docs/manuals/tutorials for mathematical packages of BLAS/LAPACK/SCALAPACK. More detailed information can be found in [this website](https://ericzhng.github.io/docs-matrix-library/).

## Getting Started

Jekyll Doc Theme is used for setting up this website. Users need to install Jekyll to make it work. More details regarding setting up Jekyll environment is given in [this page](https://ericzhng.github.io/psn-blogs/blog/github-page-jekyll/). 

General steps involve installing the environment in WSL, a Ubuntu system in Windows operating system. Start by issuing following commands:
'''
	sudo apt-get update -y 
	sudo apt-get upgrade -y
	sudo apt-get install build-essential patch ruby ruby-dev zlib1g-dev liblzma-dev dh-autoreconf
	sudo gem update
	sudo gem install jekyll bundler
	jekyll -v
	bundle install
'''

To run and check the website, follow below steps:
	1) Run following command to run the Jekyll site: 
		bundle exec jekyll build
		bundle exec jekyll serve
	2) Preview the changes in your web browser at “localhost:4000”.

## Others

Remember to update data/docs.yml when adding a new doc



