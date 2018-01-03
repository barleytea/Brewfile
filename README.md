# Brewfile

## Update

    $ brew file update

## Apply

    $ brew bundle Brewfile

## Switch multiple java version

1. install homebrew-cask-version

    `$ brew tap caskroom/versions`

2. install jdk
    `$ brew cask search java`

    `$ brew cask install java` (latest version)

    `$ brew cask install java${JAVA_VERSION}`

3. install jEnv

    `$ brew install jenv`


    `$ echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.bashrc`

    `$ echo 'eval "$(jenv init -)"' >> ~/.bashrc`

    `$ source ~/.bashrc`

### see available jdk

    $ /usr/libexec/java_home -V

### add java

    $ jenv add /Library/Java/JavaVirtualMachines/jdk${JDK_VERSION}.jdk/Contents/Home

4. switch

    `$ jenv global oracle64-${JDK_VERSION}`

    `$ java -version`
