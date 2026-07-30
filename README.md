# dotfiles, for fedora linux

install using GNU stow.

## Usage

https://brandon.invergo.net/news/2012-05-26-using-gnu-stow-to-manage-your-dotfiles.html

```
home/
    brandon/
        .config/
            uzbl/
                [...some files]
        .local/
            share/
                uzbl/
                    [...some files]
        .vim/
            [...some files]
        .bashrc
        .bash_profile
        .bash_logout
        .vimrc
```

You would then create a dotfiles subdirectory and move all the files there:

```
home/
    /brandon/
        .config/
        .local/
            .share/
        dotfiles/
            bash/
                .bashrc
                .bash_profile
                .bash_logout
            uzbl/
                .config/
                    uzbl/
                        [...some files]
                .local/
                    share/
                        uzbl/
                            [...some files]
            vim/
                .vim/
                    [...some files]
                .vimrc

```

Then, perform the following commands:

```
$ cd ~/dotfiles
$ stow bash
$ stow uzbl
$ stow vim
```

All original files will be symlinked to the dotfiles location.