vagrant-template
================

Basic Vagrant template for LAMP projects.

### Download

Clone the repo, or download archive using:

    curl -L http://git.io/x1j1Dw | tar zx

### Installation

Requires [Vagrant](http://www.vagrantup.com) and [Librarian-Chef](https://github.com/applicationsonline/librarian).

First, edit `chef/Cheffile` and specify the required Chef cookbooks. Then run the following command from within the `chef` directory.

    $ librarian-chef install
    
This will download the required cookbooks.

Now, edit `Vagrantfile` in the root directory, and build the box by running:

    $ vagrant up
    
