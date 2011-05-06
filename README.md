# Vagrant

## This version of vagrant fixes the issue when running 'vagrant up' for the first time.

    The local file Vagrant uses to store data ".vagrant" already exists
    and is a directory! If you are in your home directory, then please run
    this command in another directory. If you aren't in a home directory,
    then please rename ".vagrant" to something else, or configure Vagrant

I will attempt to keep this branch as updated as possible with the vagrant source.

I implore the vagrant developers to either merge in my fix, or fix the issue on their own, as currently any new installations of vagrant are completely broken, which I believe is stifling this otherwise excellent project.


Now on to your regularly scheduled program...

* Website: [http://vagrantup.com](http://vagrantup.com)
* Source: [http://github.com/mitchellh/vagrant](http://github.com/mitchellh/vagrant)
* IRC: `#vagrant` on Freenode
* Mailing list: [Google Groups](http://groups.google.com/group/vagrant-up)

Vagrant is a tool for building and distributing virtualized development environments.

By providing automated creation and provisioning of virtual machines using [Oracle’s VirtualBox](http://www.virtualbox.org),
Vagrant provides the tools to create and configure lightweight, reproducible, and portable
virtual environments. For more information, see the part of the getting started guide
on “[Why Vagrant?](http://vagrantup.com/docs/getting-started/index.html)”

## Quick Start

First, make sure your development machine has [VirtualBox](http://www.virtualbox.org)
installed. The setup from that point forward is very easy, since Vagrant is simply
a rubygem.

    gem install vagrant

To build your first virtual environment:

    vagrant init lucid32 http://files.vagrantup.com/lucid32.box
    vagrant up

Note: The above `vagrant up` command will also trigger Vagrant to download the
`lucid32` box via the specified URL. Vagrant only does this if it detects that
the box doesn't already exist on your system.

## Getting Started Guide and Video

To learn how to build a fully functional rails development environment, view the
[getting started guide](http://vagrantup.com/docs/getting-started/index.html).

There is also a fairly short (12 minute) [getting started video](http://vimeo.com/9976342) which
explains how to build a fully functional LAMP development environment, which
covers a few parts of Vagrant in more detail than the website guide.

## Installing the Gem from Git

If you want the bleeding edge version of Vagrant, we try to keep master pretty stable
and you're welcome to give it a shot. The following is an example showing how to do this:

    rake install

## Contributing to Vagrant

To hack on vagrant, you'll need [bundler](http://github.com/carlhuda/bundler) which can
be installed with a simple `gem install bundler --pre`. Afterwords, do the following:

    bundle install
    rake

This will run the test suite, which should come back all green! Then you're good to go!

If you want to run Vagrant without having to install the gem, you may use `bundle exec`,
like so:

    bundle exec bin/vagrant help
