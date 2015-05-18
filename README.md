# Git workflow

This document describes the git workflow that should be used when contributing
to open source projects. It assumes a very basic understanding of git
(commits, branches, etc.) using the command line.

*Note: This workflow is designed for open source (i.e., public)
repositories. The workflow for private repositories may be slightly different,
in particular, the repository's team may prefer for you to not fork the repo
but rather push branches to it directly (although note that GitHub does allow
you to fork private repositories that you have push access to and keeps the
fork private).*

For this document, we will suppose that you want to contribute a patch to
[conda/conda](https://github.com/conda/conda).

## Cloning and forking the repository

**Note: The steps in this section only need to be performed once per
repository (i.e., if you contribute a second change to conda/conda, you would
not need to repeat them, but if you contribute to
[conda/conda-build](https://github.com/conda/conda-build) you will need to
repeat them for that repository.**

1. **Clone the repository.** Copy the url <font color="blue">①</font> and type, in this case

   ```
   git clone <clone url>
   ```

   at the terminal (replace `<clone url>` with the url that has been copied to
   your clipboard. For conda/conda, it will be
   `git@github.com:conda/conda.git`. If you have not set up your ssh keys with
   GitHub, use the https url by first clicking the `https` button <font
   color="blue">②</font>.

   ![clone.png](clone.png)

   *Note: It is important that you clone from the repo you are contributing
   to (like conda/conda),* not *your fork of the repo.*

2. **Fork the repo on GitHub to your personal account.** Click the `Fork`
   button on the conda/conda page.

   ![fork.png](fork.png)

   If you are presented with a list of organizations, click on your GitHub
   username.

3. **Add your fork as a remote.** You can name this remote anything, but
   common choices are `github` or your GitHub username. For consistency in
   this document, we will call the remote `github`. Go to the fork of your
   repository, in this case, https://github.com/<your username>/conda (replace
   `<your username>` with your GitHub username), and copy the clone url as in
   step 1. `cd` to your clone from step 1 and run

   ```
   git remote add github <fork url>
   ```

   (replace `<fork url>` with the url that was copied to your
   clipboard). You will be able to tell it is your fork url because it will
   have your GitHub username in it. For instance, if your username is
   `github_user`, your fork url would be
   `git@github.com:github_user/conda.git`.

Remember, the above three steps only need to be performed once per
repository. Once you have cloned and forked a repository once, there is no
need to clone or fork it again.
