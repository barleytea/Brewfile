# Brewfile

## Update
`$ brew file update`

## Apply
`$ mkdir ~/.config`  
`$ cd ~/.config`  
`$ git clone https://github.com/barleytea/Brewfile.git`  
`$ brew bundle Brewfile`

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
