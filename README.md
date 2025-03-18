# Collection of resources and lesson learned using Arch Linux, that may be useful for me in the future (and maybe for you too).
See the other files in this repository for more specific topics, here there are the general stuff.

## Random stuff that I find useful in Arch Linux

### Many will be applicable to linux in general

1. SSH No Password: 
    ```
    ssh-copy-id user@host
    ```
2. Make Kitty (and other funky terminals) work in ssh: 
    ```
    infocmp -x | ssh YOUR-SERVER -- tic -x -
    ```
