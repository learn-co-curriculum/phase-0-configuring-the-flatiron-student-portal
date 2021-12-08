# Configuring the Flatiron Student Portal

## The `learn-co` Gem

The `learn-co` gem is a tool that simplifies the process of completing labs and
submitting your work in Canvas. Under the hood, this process consists of a
number of steps:

1. **Fork** (create your own copy of) the assignment's repo on GitHub.

2. **Clone** your copy of the repo down to your local machine.

3. Run a command (`npm install` for JavaScript labs, `bundle install` for Ruby
   labs) to install any necessary **dependencies** for the repository (_...tools
   others have built to make things easier for us_).

4. Run `npm test` (JavaScript) or `rspec` (Ruby) to run tests.

5. Use git commands to **commit** your changes and push them up to your repo on
   GitHub.

6. Submit a link to your GitHub repo in Canvas to get credit for completing the
   lab.

The `learn-co` gem will handle several of these steps for you automatically,
substantially simplifying the workflow so you can focus your attention on
learning to code. You will learn how to complete and submit assignments using
the gem in the next section; for now, let's get it installed and ready to use.

## Install the `learn-co` Gem

To install the gem, open the "Terminal" application (or "Ubuntu" for WSL users)
and run this command:

```console
$ gem install learn-co
```

Before we can use the gem, we'll need to do two things:

- Connect your Flatiron School Portal account to GitHub
- Connect the local gem to your Flatiron School Portal account

## Connect Your GitHub Account to your Flatiron School Portal Account

### Action Item

1. Open [Flatiron School's Base Account Management page][base]
   (https://base.flatironschool.com/account/manage)
2. Connect your GitHub account to your Flatiron School Portal account

Your Account Management page should now look similar to this:

![Github Successfully Connected](https://curriculum-content.s3.amazonaws.com/phase-0/configuring-the-flatiron-student-portal/base-account-manage.png)

## Configure the `learn-co` Gem

This step will ask you to do work both in your browser and your terminal.

### Action Item

1. Open the "Terminal" application (or "Ubuntu" for WSL users).
2. Type `touch ~/.netrc && chmod 0600 ~/.netrc` and press `<Enter>`. _(Note: you
   may be asked to enter your password.)_
3. Open [Flatiron School's Base Account Management page][base]
   (https://base.flatironschool.com/account/manage)
4. Click the icon under "OAuth Token" to reveal your GitHub OAuth token.
5. Copy the string of characters under the "OAuth Token" header.
6. Go back to the terminal, type `learn whoami` and press `<Enter>`.
7. Paste the string of characters at the prompt and press `<Enter>`.

### Check Your Work

Type `learn whoami` in the terminal. If you see a message with your name,
username, and email, continue to the next lesson, **Verify and Troubleshoot Your
Environment Setup**.

[base]: https://base.flatironschool.com/account/manage
