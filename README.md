# Configuring GitHub and Flatiron Student Portal

## Install `git`

<!-- ### Action item

Git generally comes pre-installed with most operating systems, but you can check
by running `git version` in the terminal. If this gives you an error or does not
come back with a version number, you'll need to install Git. you can get it
using Homebrew:

```sh
brew install git
```

### Check your work -->

## Create a GitHub account

To work on and get credit for the labs and lessons that you work on during the program, you will need to sign up for a GitHub account _if you don’t already have one_.

### Action item

1. Open the GitHub signup webpage at https://github.com/join
2. Fill out the form and create your account
3. Verify the email address connected to your GitHub account

### Check your work

If you were able to verify your email address, continue below.

## Configure Git and GitHub

Git is the tool that we’ll use to download and upload the work that we do in labs and lessons. In order to use Git without signing in every time, you can create a Secure Shell (SSH) key and associate that to your GitHub account. Lastly, you will want to run a few commands to make sure that when you use Git, you get the proper credit for your work. This step will ask you to do work both in your browser and your terminal.

### Action item

1. Open the "Terminal" application using "Spotlight Search"
2. Type “git config --global color.ui true” and press <Enter>
3. Type “git config --global user.name” + <Space> + your name and press <Enter>
4. Type “git config --global user.email” + <Space> + the email address you used to sign up to GitHub and press <Enter>
5. Type “ssh-keygen” and press <Enter>
6. For each prompt do not type anything, just continue to press <Enter>
7. Type “cat ~/.ssh/id_rsa.pub | pbcopy” and press <Enter>
8. Open the GitHub New SSH key form at https://github.com/settings/ssh/new (Note: you need to be logged in to GitHub to access that link.)
9. Type “My personal Mac” in the “Title” input field
10. Paste what’s on your clipboard in the “Key” input field
11. Click “Add SSH Key”

### Check your work

If you see your new SSH key beneath the “SSH keys” heading, continue below.

## Connect your GitHub account to your Flatiron School Portal account

Flatiron School has some helpful tools for you when it comes to working on your labs and lessons through GitHub. In order for those tools to work, you will need to connect your Flatiron School Portal account to your GitHub account.

### Action item

1. Open the Flatiron School Student Portal webpage at https://portal.flatironschool.com (Note: you need to be logged in to Flatiron School Student Portal.)
2. Click on “Course” in the navigation bar at the top of the screen
3. Click the blue “Switch Materials” button in the dropdown
4. Click on the course that you are about to start
5. Open the GitHub Account Management webpage at https://learn.co/account/github (Note: you may be asked to log in. Use your Flatiron School Student Portal username and password here.)<!-- Note: this domain is not the Portal because of Canvas flows -->
8. Connect your GitHub account to your Flatiron School Portal account

### Check your work

If you refresh the page and see a red “Disconnect” button, continue below.

## Configure the learn-co gem on Ubuntu

The learn-co gem is the tool that we’ll be using to test and submit the labs and lessons that we’re working on. Before you can use it, you will need to connect your Flatiron School Portal account to the copy of the learn-co gem on your computer. This step will ask you to do work both in your browser and your terminal.

### Action item

1. Open the "Terminal" application using "Spotlight Search"
2. Type “touch ~/.netrc && chmod 0600 ~/.netrc” and press <Enter>
3. You may be asked to enter your password
4. Type “learn whoami” and press <Enter>
5. Don’t type anything here yet
6. Go to your Public Profile Management webpage at https://portal.flatironschool.com/account/profile in your browser (Note: if you’re not logged in, you will need to log in again.)
7. Look for the "Username" heading and copy your username, but not `https://learn.co/`
8. Go to `https://portal.flatironschool.com/` and add your username after the `/`, press `<Enter>`
9.  Scroll all the way to the bottom of the page to the heading “The information below is sensitive and unique to your account. Only you can view this information.” with a red background.
10. Copy the string of characters under the “OAuth token” header
11. Paste the string of characters into the terminal and press <Enter>

### Check your work

If you see a message with your name, username, and email, continue below.