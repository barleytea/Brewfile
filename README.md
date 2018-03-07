# Brewfile

## Update
`$ brew file update`

## Apply
`$ mkdir ~/.config`  
`$ cd ~/.config`  
`$ git clone https://github.com/barleytea/Brewfile.git`  
`$ brew bundle -v`

## Switch multiple Java versions


1. add new Java
   `$ jenv add /Library/Java/JavaVirtualMachines/jdk${JDK_VERSION}.jdk/Contents/Home`

   ```
   oracle64-1.8.0.152 added
   1.8.0.152 added
   1.8 added
   ```

1. switch

    `$ jenv global oracle64-${JDK_VERSION}`  

    `$ java -version`

## use Ricty font

1. `$ brew cask install xquartz`  
1. `$ brew install --use-gcc fontforge`  
1. `$ brew tap sanemat/font`  
1. `$ brew install ricty`  
1. `$ cp -f /usr/local/Cellar/ricty/4.0.1/share/fonts/Ricty*.ttf ~/Library/Fonts/`  
1. `$ fc-cache -vf`
