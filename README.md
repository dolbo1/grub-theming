# grub-theming

GRUB as a boot-loader looks pretty ugly, but that's easy to fix.

## Finding a Theme

Finding a theme you like is completely up to personal taste.

My personal favorite theme at the moment is called "Distribution," and it includes a theme which has slight alterations depending on the version you select.

A good source I've found for some themes is [Gorgeous-GRUB](https://github.com/Jacksaur/Gorgeous-GRUB), but [pling.com](https://www.pling.com/browse?cat=109&ord=latest) is also a great source.

## Applying the Theme

### Move the theme

First, you'll have to download the theme and [extract](extract.md) it.

\*Downloading from [pling.com](https://www.pling.com/browse?cat=109&ord=latest) will give you tar.gz archives, but some themes may require to [clone](clone.md) them from GitHub.

Upon extracting your theme, check the folder to make sure it contains a `theme.txt` file.

Once you've confirmed that it does, move the **entire folder** into `/boot/grub/themes`.

This can me done with either the `mv` (move) or the `cp` (copy) commands, whichever you prefer.

To use `mv`, run:

    # sudo mv FolderName/ /boot/grub/themes/

To use 'cp', run:

    # sudo cp -r FolderName/ /boot/grub/themes/

- `sudo` must be used due to the end directory being a root directory.
- `/` at the ends are not strictly necessary, but are recommended to ensure you are working with a folder, not an individual file.
- `-r` stands for "recursively," and is used indicate that you wish to copy a folder, not a file. This is required for the `cp` command.

### Tell GRUB to use the theme

Then you'll have to modify GRUB's config file. I'll use `nano` as the text editor in this example. Run:

    # sudo nano /etc/default/grub

You must use sudo because /etc/ is in the root directory, meaning editing any files there will require super user access.

In the file, find (<kbd>CTRL</kbd> + <kbd>F</kbd>) the line reading:

    #GRUB_THEME=""

Uncomment the line, and type the **entire** path to the `theme.txt` file in the theme you've copied earlier

For example, if my theme was called "Thinkpad", my new modified line would look like this:

    GRUB_THEME="/boot/grub/themes/Thinkpad/theme.txt"

### Apply the changes to the config

To force GRUB to re-compile the config file, run:

    # sudo grub-mkconfig -o /boot/grub/grub.cfg

And upon reloading your computer, your new theme will be applied!
