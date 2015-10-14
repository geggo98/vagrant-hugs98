Vagrantfile for hugs98
========

Use this file to work with hugs98 in a virtual machine. With this method you can run hugs98 on Windows or on Mac OS X without problems.

Howto
====

Prerequisite: You have to install [Vagrant][Vagrant] on your machine. Vagrant uses a software that can run virtual machines. Usually vagrant comes bundled with Virtual Box, which can be used without charge. If you use Parallels or VmWare on a mac, please be aware that you must use an edition that works with Vagrant. Usually this means an additional fee (for Parallels you need the ["Pro" version][ParallelsPro], for VMWare you need a [separate Vagrant provider][FusionProvider]).

[Vagrant]: https://www.vagrantup.com/
[ParallelsPro]: http://kb.parallels.com/en/123296
[FusionProvider]: https://www.vagrantup.com/vmware

1. Clone the reository `git clone https://github.com/geggo98/vagrant-hugs98.git`
2. Go to the project directory `cd vagrant-hugs98`
3. Start vagrant `vagrant up`
4. Wait until vagrant has done its job (fetch some coffee, this might take a while)
5. Connect with the virtual machine `vagrant ssh`
6. Go to the directory "/vagrant" inside the VM `cd /vagrant`
7. Run hugs with one of the demo files `hugs helloworld.hs` or `hugs greetings.hs`. Inside hugs, startthe program with `main`, edit it with `:edit` (quit vim with `:q!`), reload with `:relaod` and quit hugs98 with `:quit`

When you edit a file on your machine and put it in the project directory ("vagrant-hugs98"), vagrant will sync it automatically with the "/vagrant" directory inside the VM. So you can use your favorite editor and don't have to use vim inside the VM.

Screencast
====

[![asciicast](https://asciinema.org/a/27938.png)](https://asciinema.org/a/27938)
