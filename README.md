# Brewfile

## Update  
`$ brew file update`

## Apply  
`$ brew bundle Brewfile`

## Switch multiple java versions

1. install homebrew-cask-version  
	`$ brew tap caskroom/versions`

1. install jdk  
	`$ brew cask search java`

	```
	==> Exact Match  
	java  
	==> Partial Matches  
	charles-applejava      eclipse-java         java-jdk-javadoc       java6                    	java8                netbeans-java-ee       netbeans-java-se       yourkit-java-profiler
	
	```

	`$ brew cask install java` (latest version)

	`$ brew cask install java${JAVA_VERSION}`

1. install jEnv

	`$ brew install jenv`

   `$ echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.bashrc`

   `$ echo 'eval "$(jenv init -)"' >> ~/.bashrc`
    
   `$ source ~/.bashrc`

	`$ /usr/libexec/java_home -V`
		
    ```
    Matching Java Virtual Machines (2):
    9.0.1, x86_64:	"Java SE 9.0.1"	/Library/Java/JavaVirtualMachines/jdk-9.0.1.jdk/Contents/Home
    1.8.0_152, x86_64:	"Java SE 8"	/Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Home

    /Library/Java/JavaVirtualMachines/jdk-9.0.1.jdk/Contents/Home
	
    ```

   `$ jenv add /Library/Java/JavaVirtualMachines/jdk${JDK_VERSION}.jdk/Contents/Home`
   
   ```
   oracle64-1.8.0.152 added
   1.8.0.152 added
   1.8 added
   
   ```

1. switch

    `$ jenv global oracle64-${JDK_VERSION}`

    `$ java -version`
