# Configuring the Flatiron Student Portal

## Introduction

As you continue your journey into programming, you will learn to use many tools
to make your work easier that you only _sort of_ understand. Node packages, Ruby
gems, libraries, command-line applications, frontend frameworks, etc... many of
these tools are actually built out of _other_ tools, things you may never have
heard of. That is okay.

Thanks to the collective work of many programmers around the world, we're able
to tap in to a diverse ecosystem of tools. We don't need to know how they all
work together for them to be useful to us. You might one day know JavaScript
well enough to build your own version of [React](https://reactjs.org/), but
you'll be able to use React long before you know how all the parts work. Many of
these tools are designed to solve problems so we can focus our energy and time
elsewhere.

We've already used a few tools to help us get started with programming. If you
recall from the previous installation instructions, we've installed NVM, the
Node Version Manager, which manages which version of Node you're using on your
computer. We've been using NPM, Node **Package** Manager, to run local tests.
We've also been using Git in the command line to interface remotely with GitHub.

In this lesson, we're going to introduce another tool that will help us going
forward, the `learn-co` gem.

## The `learn-co` Gem

So, if all these tools we use are meant to solve problems, what problems does
the `learn-co` gem solve?

In your assignments so far, after cloning a repository, you typically do a few
things while working through the assignment:

1. Run `npm install` or `bundle` to install any necessary dependencies for the
   repository (_...tools others have built to make things easier for us_)

2. Run `npm test` or `rspec` to run tests

3. Git commit and push your work to your GitHub remote repo

Once you've pushed your solution up to GitHub, you then have to submit a link in
Canvas.

The `learn-co` gem will take care of all of these steps using a single command,
`learn test`! Let's get the gem installed and configured so we can test it out.

**Note:** The instructions here assume you've successfully installed Ruby and
Node in the previous environment setup instructions.

## Install the `learn-co` Gem

To install the gem, run the following in your terminal:

```sh
gem install learn-co
```

Before we can use the gem, we'll need to do a few things:

- Connect your Flatiron School Portal account to GitHub
- Connect the local gem to your Flatiron School Portal account

## Connect Your GitHub Account to your Flatiron School Portal Account

### Action Item

1. Open [Flatiron School's Base Account Management page][]
   (https://base.flatironschool.com/account/manage)
2. Connect your GitHub account to your Flatiron School Portal account

You should now see something similar to this:

![Github Successfully Connected](https://curriculum-content.s3.amazonaws.com/phase-0/configuring-the-flatiron-student-portal/base-account-manage.png)

## Configure the `learn-co` Gem

This step will ask you to do work both in your browser and your terminal.

### Action Item

1. Open the "Terminal" application (or "Ubuntu" for WSL users).
2. Type `touch ~/.netrc && chmod 0600 ~/.netrc` and press `<Enter>`. _(Note: you
   may be asked to enter your password.)_
3. Open [Flatiron School's Base Account Management page][]
   (https://base.flatironschool.com/account/manage)
4. Click the icon under "OAuth Token" to reveal your GitHub OAuth token.
5. Copy the string of characters under the "OAuth Token" header.
6. Go back to the terminal, type `learn whoami` and press `<Enter>`.
7. Paste the string of characters at the prompt and press `<Enter>`.

[Flatiron School's Base Account Management page]: https://base.flatironschool.com/account/manage

### Check Your Work

Type `learn whoami` in the terminal. If you see a message with your name,
username, and email, you've successfully configured the gem.

## Using the `learn-co` Gem

The `learn-co` gem replaces some steps in the assignment workflow you've learned
so far and alters others. Let's walk through the updated process. Use this
assignment to follow along:

1) On this assignment's Canvas page, click the **Fork** button in the upper
   right corner of the page:

   ![fork buttton](https://curriculum-content.s3.amazonaws.com/fork-link.png)

   You should notice a change in the button's behavior — rather than bringing
   you to the fork page in GitHub, you'll be redirected to your repository
   _already in the process_ of being forked.
   
 2) Once your fork is ready, click the **Code** button and copy the **SSH**
    repository info by clicking the clipboard button.

   ![clone with SSH](https://curriculum-content.s3.amazonaws.com/canvas-welcome/clone-with-ssh.png)

   **Note:** Make sure you're choosing SSH and not HTTPS.

 3) In your terminal, navigate to where you'd like to put this repository
    locally, clone it down and navigate into the folder.

```
git clone git@github.com:<your-github-account-name>/macos-env-flatiron-student-portal.git
cd macos-env-flatiron-student-portal
```

 4) Instead of running `npm install` and `npm test` (or `bundle` and `rspec`),
    you can now run one command, `learn test`, to handle this step.  This command
    will automatically run the installation and test commands. You should see a
    flurry of text as dependencies are installed, then the results of your test.
    This assignment has the same test as the previous **Complete Your First
    Software Engineering Assignment**. By cloning this assignment down, you've
    already passed the test!

```
This assignment
    ✓ has been correctly cloned to your local environment


  1 passing (5ms) 
```

When all tests are passing, you can head back to the assignment on Canvas.
Refresh the assignment page and you should see that Canvas now registers the
assignment as both **Submitted** and **Complete**. A URL to your fork of the
assignment has been submitted in Canvas, so you are ready to move on to the next
lesson.

Each assignment will be different and will include instructions on what is
required to complete it. Some labs will have many tests. You can run `learn
test` as many times as you'd like while working to solve these labs. You will
submit your work to Canvas each time you do, but the assignment will be marked
**Incomplete** until all tests are passing.

### Your Work in GitHub

Every time you run `learn test`, all the changes you've made locally will be
stored on your GitHub fork of the repo. If you head back to your repo after
running `learn test`, you should see a message that a new branch, `fis-wip`, has
been created. This branch contains the work you've done so far. If you ever want
to go back to a previous solution, go to that repository on GitHub and switch to
the `fis-wip` branch.

You no longer need to commit and push your local work for these assignments.

**Note:** if you see the following message on your repo's page in GitHub, please disregard it: 

![pr_prompt](https://curriculum-content.s3.amazonaws.com/phase-0/configuring-the-student-portal/fis-wip.jpg)

## Types of Assignments

For most assignments, you will go through the process we just walked through. In
our curriculum, these assignments are often referred to as **labs** — coding
lessons that include tests. There are a few other types of assignments, though,
that require slightly different submission steps:

- **Code-alongs:** These also require code, but will guide you through what
  needs to be written. There are no tests to pass, but you will still need to go
  through forking, cloning, and running `learn test`. You should see a message
  stating that no tests were found, but if you check the assignment in Canvas,
  you should see it is marked as **Complete**.
- **Portfolio Projects:** For these assignments, you'll be building fully
  functional applications. Some guidelines and requirements will be provided,
  but it will be up to you to design and create your own app. These will
  eventually become the projects you showcase to potential employers! You will
  submit your projects in Canvas by submitting a link to your GitHub repo.
- **Blog Submissions:** Blogs are a required part of our Software Engineering
  courses. They help to develop your online presence and are a great way to
  reinforce the concepts you learn. You'll write your blog posts on a different
  platform, but submit links to them in Canvas.

## Submitting Projects and Blogs

For both portfolio projects and blog posts, you'll need to manually submit a
link to your work on Canvas. While viewing the assignment, you should see a
**Submit Assignment** button in the upper-right section of the page.

![submit assignment button](https://curriculum-content.s3.amazonaws.com/canvas-welcome/submit-assignment-canvas.png)

Clicking this button will bring you to the bottom of the page where you can
submit a URL link to your work.

![submit assignment form](https://curriculum-content.s3.amazonaws.com/canvas-welcome/submit-assignment-canvas-form.png)

Upon submission you should see confetti appear, indicating that your submission
has been accepted.

> **Note:** It is possible to submit lab and code-along assignments manually
> this way. However, the assignment will only be marked as **Submitted**, not
> **Complete**.

## Conclusion

You've completed your first assignment using the `learn-co` gem! You now know
how to work on and submit assignments going forward:

- Click the **Fork** button on the Canvas assignment
- Once the assignment is forked, clone it down to your local machine
- Complete any required work, then run `learn test`
- If all tests pass, the assignment will be submitted to Canvas and marked as
  **Complete**
- Your work will also be pushed to GitHub and will be available on the `fis-wip`
  branch

Equipped with this knowledge, you are now ready to tackle greater challenges!

[GitHub Account Management webpage]: https://portal.flatironschool.com/account/github
