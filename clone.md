# clone.md

Cloning simply means copying files from Git (AKA GitHub) onto your computer.

This can be useful if you need to copy specific files from a Git repo (repository) to a directory on your computer, like GRUB theme files.

To clone a repo, you'll use the `$ git clone` command.

As an example, I'll use a GRUB theme repo, called "HyperFluent-GRUB-Theme" from Coopydood. It's found at <https://github.com/Coopydood/HyperFluent-GRUB-Theme/>

To clone the repo to your current directory, run:

    $ git clone https://github.com/Coopydood/HyperFluent-GRUB-Theme.git

The link to the repo (including the .git at the end) can be copied by hitting the "<> Code" button in the top right of the repo site.

All contents of the repo will now be copied to your current directory, into a folder with a title identical to the title of the repo.

If you want to create a new folder and copy the repo into there, add the name of the folder you wish to create after the repo link.

For example, if I wanted to copy the HyperFluent-GRUB-Theme repo into a folder simply called `HyperFluent`, I'd run the following command:

    $ git clone https://github.com/Coopydood/HyperFluent-GRUB-Theme.git HyperFluent

With that, you now have a copy of a git repo of your choice on your computer.
