= Knife  install

= DESCRIPTION:

This is a Knife plugin for local installation. 

This plugin gives knife the ability to install cookbook recipes, but leave them unmanaged in future chef-client runs.

The use case is, for example to provide a securely configured tomcat and manager instance, which is then further customized by a developer with local administrator rights for their own purposes.

It is a work-around to the issue that developer users often require more flexibility to customize their node than would be permitted with a production installion, and often do not have chef skills to work in the chef paradigm and toolset.

= INSTALLATION:

You need to run this command with root privileges.

Be sure you are running the latest version Chef. Versions earlier than 0.10.0 don't support plugins:

    gem install chef

This plugin is distributed as a Ruby Gem. To install it, run:

    gem install knife-install

= CONFIGURATION:

None as yet

= SUBCOMMANDS:

You need to run these commands with root privileges.

This plugin provides the following Knife subcommands.  Specific command options can be found by invoking the subcommand with a <tt>--help</tt> flag

== Knife install --help

The goal  The main assumption is to bypass chef server and client install  and  just install a recipe 

== Knife  install 

Generates instance metadata in meant to be used with Opscode's custom AMIs. This will read your knife configuration <tt>~/.chef/knife.rb</tt> for the validation certificate and Chef server URL to use and output in JSON format. The subcommand also accepts a list of roles/recipes that will be in the node's initial run list.


knife node run_list add NODE 'role[chef-client],recipe[getting-started],recipe[chef-client::service]' type syntax

knife install [ENTRY[,ENTRY]]  (options)

= LICENSE:

Author::
Copyright:: 
License:: 

