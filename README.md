A custom puppet module skeleton for using with `puppet module generate`.

## Installation

Puppet uses the contents of `~/.puppet/var/puppet-module/skeleton` as the template. Once you've cloned this repo, run `install.sh` to install the skeleton.

  git clone https://github.com/danfoster/puppet-module-skeleton 
  cd puppet-module-skeleton
  find skeleton -type f | git checkout-index --stdin --force --prefix="$HOME/.puppet/var/puppet-module/" --

## Usage

Generate your module using:

  puppet module generate my-module

Install deps using:

    cd my-module
    bundle install

View rake tasks:

    bundle exec rake help
    rake beaker            # Run beaker acceptance tests
    rake beaker_nodes      # List available beaker nodesets
    rake build             # Build puppet module package
    rake clean             # Clean a built module package
    rake coverage          # Generate code coverage information
    rake help              # Display the list of available rake tasks
    rake lint              # Check puppet manifests with puppet-lint / Run puppet-lint
    rake spec              # Run spec tests in a clean fixtures directory
    rake spec_clean        # Clean up the fixtures directory
    rake spec_prep         # Create the fixtures directory
    rake spec_standalone   # Run spec tests on an existing fixtures directory
    rake syntax            # Syntax check Puppet manifests and templates
    rake syntax:hiera      # Syntax check Hiera config files
    rake syntax:manifests  # Syntax check Puppet manifests
    rake syntax:templates  # Syntax check Puppet templates
    rake validate          # Check syntax of Ruby files and call :syntax / Validate manifests, templates, and ruby files

Running `bundle exec rake` will run a sensible default set of tests, useful for CI.
