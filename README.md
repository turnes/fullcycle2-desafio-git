# fullcycle2-desafio-git
Desafio git - Assinatura de commits


# setup

```bash
# list current keys
gpg --list-secret-keys --keyid-format LONG

# create one
gpg --full-generate-key

# export public key
gpg --armor --export YOUR_KEY_ID

# Import the public in your github account.
https://github.com/settings/gpg/new

# configure the key in your git
git config --global user.signingkey YOUR_KEY_ID

# create a enverionment variable.
export GPG_TTY=$(tty)

# set globally or localy to sign every commit.
git config --global commit.gpgsign true  # global
git config commit.gpgsign true # specific project

```

# Commit
Create a commit and check if it is signed.

```bash
git log --show-signature -1
```


