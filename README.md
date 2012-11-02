Installation
------------

Install 'p4d' (the Perforce server daemon) if you don't already have it.  Go [here](http://www.perforce.com/downloads/complete_list) and choose the one for your platform. For Mac, choose darwin 64 or 32 as applicable (slightly counter intuitive).  Put the resulting executable in your path and make it executable.

Install 'p4' (the Perforce command line client) if you don't already have it.  Go [here](http://www.perforce.com/downloads/complete_list) and choose the one for your platform. For Mac, choose darwin 64 or 32 as applicable (slightly counter intuitive).  Put the resulting executable in your path and make it executable.

Install Ruby Gems if you have not already.

The app requires at least Ruby 1.9.3 to run. 

```
$ bundle install
$ rvm install 1.9.3 # if needed
$ rvm 1.9.3
```

First Time
----------

You need to setup some users in perforce. Say you're name is 'foo', from the command line:

```
$ ruby useradd.rb
$ p4port: localhost:1666
$ username: foo
$ email: foo@bar.com
$ password: YOUR_PASSWORD
$ User foo saved.
$ Client fooClient saved.
```

This command will also create a copy of stack_configuration.json in perforce the first time you run it.

Running it
----------

First launch the Perforce Daemon:

```
$ ./perforce_daemon.sh
```

Then run the Sinatra web server:

```
$ rackup
```

Then crank up your browser, and go to [http://localhost:9292](http://localhost:9292)
