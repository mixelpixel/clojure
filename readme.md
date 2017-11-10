# Clojure
1. https://www.braveclojure.com/
2. https://www.braveclojure.com/foreword/
3. https://www.braveclojure.com/acknowledgements/
4. https://www.braveclojure.com/introduction/
5. https://www.braveclojure.com/getting-started/

### Download the latest Java Developers Kit (JDK, it includes JRE - runtime env)
- http://www.oracle.com/technetwork/java/javase/downloads/index.html
#### Uninstalling Java9
- https://gist.github.com/schnell18/bcb9833f725be22f6acd01f94b486392
```
sudo rm -fr /Library/Java/JavaVirtualMachines/jdk-9.jdk/
sudo rm -fr /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin
sudo rm -fr /Library/PreferencePanes/JavaControlPanel.prefPane
```

## INSTALLATION
- From: http://www.oracle.com/technetwork/java/javase/downloads/index.html
  * JavaSE 9.0.1 JDK
- `brew install leiningen`

### Additional Clojure Resources
- http://www.4clojure.com/problems
- https://youtu.be/j-kj2qwJa_E
- http://lambdaisland.com/

### First!
`lein new app clojure-noob`

# Chapter 1
https://www.braveclojure.com/getting-started/

# Chapter 2
https://www.braveclojure.com/basic-emacs/




***

### Installing Leiningen the hard and unsuccessful way
- http://leiningen.org/
1. Download the lein script (or on Windows lein.bat)
2. Place it on your $PATH where your shell can find it (eg. ~/bin)
3. Set it to be executable (chmod a+x ~/bin/lein)
4. Run it (lein) and it will download the self-install package

To display the current $PATH directories:
```console
$ echo $PATH
/opt/local/bin:
/opt/local/sbin:
/usr/local/bin:
/Users/mixelpix/.rbenv/shims:
/usr/bin:
/bin:
/usr/sbin:
/sbin:
/usr/local/bin:
/opt/X11/bin:
/Applications/Postgres.app/Contents/Versions/latest/bin
```

To modify $PATH per https://apple.stackexchange.com/a/70621/216401
```console
echo 'export PATH=/Users/mixelpix/bin:$PATH' >> ~/.bash_profile
```

Now $PATH is set to:
```console
/Users/mixelpix/bin:
/opt/local/bin:
/opt/local/sbin:
/usr/local/bin:
/Users/mixelpix/.rbenv/shims:
/usr/bin:
/bin:
/usr/sbin:
/sbin:
/usr/local/bin:
/opt/X11/bin:
/Applications/Postgres.app/Contents/Versions/latest/bin
```

...and to reload the active console with the updated $PATH:
```console
$ source ~/.bash_profile
```
or
```console
$ . ~/.bash_profile
```

more on $PATH: https://coolestguidesontheplanet.com/add-shell-path-osx/


`lein` install FAIL:
```console
$  lein
Downloading Leiningen to /Users/mixelpix/.lein/self-installs/leiningen-2.7.1-standalone.jar now...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   618    0   618    0     0   1955      0 --:--:-- --:--:-- --:--:--  1955
100 14.6M  100 14.6M    0     0  2366k      0  0:00:06  0:00:06 --:--:-- 2627k

Exception in thread "main" java.lang.ExceptionInInitializerError
	at java.base/java.lang.Class.forName0(Native Method)
	at java.base/java.lang.Class.forName(Class.java:375)
	at clojure.lang.RT.classForName(RT.java:2168)
	at clojure.lang.RT.classForName(RT.java:2177)
	at clojure.lang.RT.loadClassForName(RT.java:2196)
	at clojure.lang.RT.load(RT.java:443)
	at clojure.lang.RT.load(RT.java:419)
	at clojure.core$load$fn__5677.invoke(core.clj:5893)
	at clojure.core$load.invokeStatic(core.clj:5892)
	at clojure.core$load.doInvoke(core.clj:5876)
	at clojure.lang.RestFn.invoke(RestFn.java:408)
	at clojure.core__init.load(Unknown Source)
	at clojure.core__init.<clinit>(Unknown Source)
	at java.base/java.lang.Class.forName0(Native Method)
	at java.base/java.lang.Class.forName(Class.java:375)
	at clojure.lang.RT.classForName(RT.java:2168)
	at clojure.lang.RT.classForName(RT.java:2177)
	at clojure.lang.RT.loadClassForName(RT.java:2196)
	at clojure.lang.RT.load(RT.java:443)
	at clojure.lang.RT.load(RT.java:419)
	at clojure.lang.RT.doInit(RT.java:461)
	at clojure.lang.RT.<clinit>(RT.java:331)
	at clojure.main.<clinit>(main.java:20)
Caused by: java.lang.ClassNotFoundException: java/sql/Timestamp
	at java.base/java.lang.Class.forName0(Native Method)
	at java.base/java.lang.Class.forName(Class.java:375)
	at clojure.lang.RT.classForName(RT.java:2168)
	at clojure.lang.RT.classForNameNonLoading(RT.java:2181)
	at clojure.instant$loading__5569__auto____6869.invoke(instant.clj:9)
	at clojure.instant__init.load(Unknown Source)
	at clojure.instant__init.<clinit>(Unknown Source)
	... 23 more
```
