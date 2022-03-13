
<!DOCTYPE html>
<html lang="en">
<head>
<meta name="robots" content="noindex, nofollow" />
<meta name="viewport" content="width=device-width">
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<link rel="stylesheet" type="text/css" href="/ugly.css">
<title>gopher://codevoid.de/1/posts/2019-04-27-manage-dotfiles-with-git.gph</title>
</head>
<body>
<pre>
       Manage dotfiles with git
       ========================================================================
       
       I&#39;m managing my dotfiles with git. My method serves me well for a few
       years already and so I think it&#39;s time to write it down.
       
       If you think git, you might think of a dotfile repository and dozens of
       symlinks into the home directory. This is precisely what kept me from
       using git until I discovered bare repositories.
       
       Create your dotfile repository with the --bare parameter
       
         $ git init --bare $HOME/.cfg
       
       This creates only a folder for git control files, which normally reside
       inside the .git folder within the repository.
       
       You can now tell git to use $HOME as your work-tree directory. This
       makes git handle your home directory like all the files would be within
       the git repository. Now you can:
       
         $ git --git-dir=$HOME/.cfg/ --work-tree=$HOME add .vimrc
         $ git --git-dir=$HOME/.cfg/ --work-tree=$HOME commit -m &quot;my .vimrc&quot;
       
       If course it is silly to type out such a long command every time you
       want to interract with your dotfiles. So why not create an alias?
       
         $ alias config=&#39;git --git-dir=$HOME/.cfg/ --work-tree=$HOME&#39;
       
       Put this in your .bashrc or .kshrc and you can now use the command
       &quot;config&quot; in the same way you usually use git.
       
         $ config add .vimrc
         $ config commit -m &quot;my vimrc&quot;
       
       Maybe you were brave and typed &quot;config status&quot; already. This will list
       the content of your whole home directory as &quot;untracked files&quot;. This is
       not what we want. We can run &quot;git config&quot; and tell it to stop doing
       this. But of course we must run our git, which is called &quot;config&quot;.
       
         $ config config --local status.showUntrackedFiles no
       
       Now git status will only check what&#39;s being tracked. So if you add your
       vimrc file and later change it, &quot;config status&quot; will show it, &quot;config
       diff&quot; will diff it...
       
       You can now use the power of git with your new &quot;config&quot; command.
       
       The solution is not perfect, so I&#39;m using a few workarounds.
       
       1. Passwords
           Try to keep your passwords out of your dotfiles. In many
           cases, this can be done with gpg (or password-store
           https://www.passwordstore.org).
       Examples:
       
           - .msmtprc:
               passwordeval &quot;gpg2 -d $HOME/.msmtp-pw.gpg&quot;
           - .offlineimaprc:
               pythonfile=~/.offlineimap.py
               remotepasseval=get_pass(&quot;mail&quot;,&quot;user&quot;,&quot;993&quot;)
           - .muttrc:
               source &quot;gpg2 -d $HOME/.mutt-pw.gpg |&quot;
       
           Actually, I use &quot;password store&quot; and prefer to use it to retrieve
           passwords. In mutt this would be something like:
               source &quot;pass Accouts/private-mutt |&quot;
       
           Another method I use is that I keep the origin of some files gpg
           encrypted. For example my .ssh/config file, as I don&#39;t want to leak
           hostnames user and ports.
       
           My vim has the vim-gpg plugin loaded and can therefore edit .gpg
           files directoy (decrypt, edit, encrypt). So I create a simple shell
           alias for convenience:
       
             $ sshconfig() {
             $   vim ~/.ssh/config.gpg &amp;&amp; \
             $   gpg2 -qd ~/.ssh/config.gpg &gt; ~/.ssh/config
             $ }
         
           With this I run &quot;sshconfig&quot;, update my file, save, done.
           of course I added only config.gpg to my git. On a new
           system I have to run sshconfig once to create the config file.
       
       2. Stuff outside $HOME
           I wanted to add a few files that reside in /etc. Here I took the
           lazy route and created $HOME/.etc and copied the files there. On a
           new machine I have the files, but need to copy them manually. Works
           fine for me.
       
       3. Host specific files
           I try to keep my dotfiles compatible to all computers I use. But
           sometimes this is not possible and there are a few methods to battle
           this.
       
           If your configuration allows code evaluation, you may do something
           like &quot;. myconfig.$(hostname -s)&quot; and just check in individual files
           per host.
       
           If this does not work or you have a file that needs to have a
           password in it, you could copy the file, remove the password and
           check it in as template or sample file.
       
       The methods above served me very well over the past years and I&#39;m not
       seeing why I would want to change it. It&#39;s easy and simple and I don&#39;t
       need to remember anything beside a few git commands.
       
       Well okay, because I&#39;m lazy and don&#39;t want to think about git commit
       messages, I&#39;m using this to push my changes:
       
         $ dotfiles_autoupdate() {
         $     MSG=&quot;Update $(date +&quot;%Y-%m-%d %H:%M&quot;) $(uname -s)/$(uname -m)&quot;
         $     config add -u &amp;&amp; \
         $     config commit -m &quot;$MSG&quot; &amp;&amp; \
         $     config push
         $ }
       
       This command takes all changed files and commits them with the date and
       some machine information. Not creative, but I don&#39;t care. YMMV.
       
       # Changelog:
       # * 2019-04-27: Created
       # * 2019-04-28: Added password evaluation examples
       # * 2020-05-17: Added password-store and sshconfig examples
</pre>
</body>
</html>
