$ export GITHUB_USERNAME=<evgenijj88>
$ export GITHUB_EMAIL=<evgenijj.88@yandex.ru>
$ export GITHUB_TOKEN=<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 >
$ alias edit=<nano|vi|vim|subl>
$ cd ${GITHUB_USERNAME}/workspace
$ source scripts/activate
$ mkdir ~/.config
$ cat > ~/.config/hub <<EOF
github.com:
- user: ${GITHUB_USERNAME}
  oauth_token: ${GITHUB_TOKEN}
  protocol: https
EOF
$ git config --global hub.protocol https
$ mkdir projects/lab02 && cd projects/lab02
$ git init
$ git config --global user.name ${GITHUB_USERNAME}
$ git config --global user.email ${GITHUB_EMAIL}
# check your git global settings
$ git config -e --global
$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
$ git pull origin master
$ touch README.md
$ git status
$ git add README.md
$ git commit -m"added README.md"
$ git push origin master
