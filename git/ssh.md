---
description: Information about SSH.
---

# SSH

SSH can be a little tricky. Below I have the various things I have come across to help me out. Most commands currently are for Mac, once I mess with Windows more I will update.

## Resources

* Traversy Media Video
  * [https://youtu.be/hQWRp-FdTpc](https://youtu.be/hQWRp-FdTpc)
* GitLab Docs
  * [https://docs.gitlab.com/ee/ssh/README.html](https://docs.gitlab.com/ee/ssh/README.html)
* GitHub Docs
  * [https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)

## SSH version installed on your system

```text
$ ssh -V
```

## Create an SSH Key

Run the following command and pick all the defaults to the prompts.  This tutorial doesn't explain how to use passphrases.

```text
$ ssh-keygen
```

{% hint style="info" %}
Be mindful the command above is a super basic way.  GitLab mentioned the following options at the end of the ssh-keygen command.  See the picture below or visit the [GitLab Docs](https://docs.gitlab.com/ee/ssh/README.html#generate-an-ssh-key-pair)
{% endhint %}

![](../.gitbook/assets/generate-ssh-key%20%281%29.png)

## Add SSH Key To GitHub or GitLab

* GitHub
  * [https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
* GitLab
  * [https://docs.gitlab.com/ee/ssh/README.html\#add-an-ssh-key-to-your-gitlab-account](https://docs.gitlab.com/ee/ssh/README.html#add-an-ssh-key-to-your-gitlab-account)

## Test SSH Connection

The following commands should say Hello or Welcome followed by your username if you set everything up correctly.  Learn more at the [GitLab Docs](https://docs.gitlab.com/ee/ssh/README.html#verify-that-you-can-connect) or [GitHub Docs](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/testing-your-ssh-connection).

```text
$ ssh -T git@github.com
$ ssh -T git@gitlab.com
```

## Are you still getting Permission Denied?

{% hint style="info" %}
Make sure you are in your root when running this command.  Also, be mindful you will replace SSH\_FILENAME with your filename.
{% endhint %}

```text
$ ssh-add ~/.ssh/SSH_FILENAME
```

