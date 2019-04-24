# Changing a remote's URL

Mac Windows Linux All

## The `git remote set-url` command changes an existing remote repository URL.

**Tip:** For information on the difference between HTTPS and SSH URLs, see "[Which remote URL should I use?](/en/articles/which-remote-url-should-i-use)"

The `git remote set-url` command takes two arguments:

  * An existing remote name. For example, `origin` or `upstream` are two common choices.
  * A new URL for the remote. For example:

  * If you're updating to use HTTPS, your URL might look like:
        
                https://github.com/_spark7x_/_41447608-spark7x-users.noreply.github.com_.git
        
        
        
        
        
  * If you're updating to use SSH, your URL might look like:
        
        
        
        
                git@github.com:_spark7x_/_41447608-spark7x-users.noreply.github.com_.git
        
        
        
### [Switching remote URLs from SSH to HTTPS](https://help.github.com/en/articles/changing-a-remotes-url#switching-remote-urls-from-ssh-to-https)
    
    
1. Open TerminalTerminalGit Bashthe terminal.
    
2. Change the current working directory to your local project.
    
3. List your existing remotes in order to get the name of the remote you want to change.
    
    
      
    
          $ git remote -v
          > origin  git@github.com:_spark7x
          41447608-spark7x-users.noreply.github.com_.git (fetch)
          > origin  git@github.com:_spark7x
          41447608-spark7x-users.noreply.github.com_.git (push)
    
4. Change your remote's URL from SSH to HTTPS with the git remote set-url command.
    
    
    
    
        $ git remote set-url origin https://github.com/_spark7x_/_41447608-spark7x-users.noreply.github.com_.git
    
    
    
    
    
5. Verify that the remote URL has changed.
    
    
      
    
        $ git remote -v
        # Verify new remote URL
        > origin  https://github.com/_spark7x
        41447608-spark7x-users.noreply.github.com_.git (fetch)
        > origin  https://github.com/_spark7x
        41447608-spark7x-users.noreply.github.com_.git (push)
    
    
The next time you git fetch, git pull, or git push to the remote repository, you'll be asked for your GitHub username and password.
    
* If you have [two-factor authentication](/en/articles/securing-your-account-with-two-factor-authentication-2fa) enabled, you must [create a personal access token](/en/articles/creating-a-personal-access-token-for-the-command-line) to use instead of your GitHub password.
    
* You can [use a credential helper](/en/articles/caching-your-github-password-in-git) so Git will remember your GitHub username and password every time it talks to GitHub.
    
### [Switching remote URLs from HTTPS to SSH](https://help.github.com/en/articles/changing-a-remotes-url#switching-remote-urls-from-https-to-ssh)
    
1. Open TerminalTerminalGit Bashthe terminal.
    
2. Change the current working directory to your local project.
    
3. List your existing remotes in order to get the name of the remote you want to change.
    
        $ git remote -v
        > origin  https://github.com/_spark7x
        41447608-spark7x-users.noreply.github.com_.git (fetch)
        > origin  https://github.com/_spark7x
        41447608-spark7x-users.noreply.github.com_.git (push)
    
4. Change your remote's URL from HTTPS to SSH with the git remote set-url command.
    
        $ git remote set-url origin
        git@github.com:_spark7x_/_41447608-spark7x-users.noreply.github.com_.git
      
5. Verify that the remote URL has changed.
    
        $ git remote -v
        # Verify new remote URL
        > origin  git@github.com:_spark7x
        41447608-spark7x-users.noreply.github.com_.git (fetch)
        > origin  git@github.com:_spark7x
        41447608-spark7x-users.noreply.github.com_.git (push)
    
    
### [Troubleshooting](https://help.github.com/en/articles/changing-a-remotes-url#troubleshooting)
    
You may encounter these errors when trying to change a remote.
    
    
#### No such remote '[name]'
    
This error means that the remote you tried to change doesn't exist:
    
    
    $ git remote set-url sofake https://github.com/octocat/Spoon-Knife
    > fatal: No such remote 'sofake'
    
    
    
Check that you've correctly typed the remote name.
    
    
### [Further reading](https://help.github.com/en/articles/changing-a-remotes-url#further-reading)
    
* "[Working with Remotes" from the _Pro Git_ book](https://git-scm.com/book/en/Git-Basics-Working-with-Remotes)
    
    
### Ask a human

#### Can't find what you're looking for?
    
    
[Contact us](https://github.com/contact)
          
[](https://github.com/)
          
    
#### Product
           
* [Features](https://github.com/features)
    
              
* [Security](https://github.com/security)
    
              
* [Enterprise](https://github.com/enterprise)
    
              
* [Case studies](https://github.com/case-studies?type=customers)
    
              
* [Pricing](https://github.com/pricing)
    
              
* [Resources](https://resources.github.com)
    
#### Platform
* [Developer API](https://developer.github.com/)
    
              
* [Partners](http://partner.github.com/)
    
              
* [Atom](https://atom.io)
    
              
* [Electron](http://electron.atom.io/)
    
              
* [GitHub Desktop](https://desktop.github.com/)

#### Support
         
* [Help](/)
    
              
* [Community Forum](https://github.community)
    
              
* [Training](https://services.github.com/)
    
              
* [Status](https://githubstatus.com/)
    
              
* [Contact GitHub](https://github.com/contact)
    
#### Company
* [About](https://github.com/about)
    
              
* [Blog](https://github.blog/)
    
              
* [Careers](https://github.com/about/careers)
    
              
* [Press](https://github.com/about/press)
    
              
* [Shop](https://shop.github.com)
    
* ![](https://img.icons8.com/color/48/000000/twitter.png)

* ![](https://img.icons8.com/color/48/000000/facebook.png)

* ![](https://img.icons8.com/color/48/000000/youtube.png)

* ![](https://img.icons8.com/color/48/000000/linkedin.png)
           
* ![](https://img.icons8.com/color/48/000000//github.png)

* (C) 2019 GitHub, Inc.
    
* [Terms ](/articles/github-terms-of-service/)
    
* [Privacy ](/articles/github-privacy-statement/)
