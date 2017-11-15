# CLOJURE for the BRAVE and TRUE
## Learn the Ultimate Language and Become a Better Programmer
### by Daniel Higginbotham
1. https://www.braveclojure.com/ √
2. https://www.braveclojure.com/foreword/ √
3. https://www.braveclojure.com/acknowledgements/ √
4. https://www.braveclojure.com/introduction/ √
  * Printed book sample: [chapter 3](https://www.nostarch.com/download/Clojure%20for%20the%20Brave%20and%20True_sample_ch3.pdf)
  * ["Emacs Resources for Chapter 2"](https://github.com/flyingmachine/emacs-for-clojure/archive/book1.zip)
    * [GNU Emacs](https://www.gnu.org/software/emacs/)
  * ["Clojure for the Brave and True" source code](https://github.com/braveclojure/cftbat-code/)

# Part I: Environment Setup
> To stay motivated and learn efficiently, you need to actually write code and build executables. These chapters take you on a quick tour of the tools you’ll need to easily write programs. That way you can focus on learning Clojure, not fiddling with your environment.

NOTE: 11/2017, macOS High Sierra, 11" 2012 AirBook, 2GHz i7, 8GB RAM.

## Chapter 1 - Building, Running, and the REPL √
https://www.braveclojure.com/getting-started/

> There’s something powerful and motivating about getting a real program running. Once you can do that, you’re free to experiment, and you can actually share your work!

> In this short chapter, you’ll invest a small amount of time to become familiar with a quick way to build and run Clojure programs. You’ll learn how to experiment with code in a running Clojure process using a read-eval-print loop (REPL). This will tighten your feedback loop and help you learn more efficiently.

### Download the latest Java Developers Kit (JDK, it includes JRE - runtime env)
- http://www.oracle.com/technetwork/java/javase/downloads/index.html

##### INSTAL JAVA SE
- From: http://www.oracle.com/technetwork/java/javase/downloads/jdk9-downloads-3848520.html
- [JavaSE 9.0.1 JDK](http://download.oracle.com/otn-pub/java/jdk/9.0.1+11/jdk-9.0.1_osx-x64_bin.dmg)
##### Uninstalling Java9
- https://gist.github.com/schnell18/bcb9833f725be22f6acd01f94b486392
```
sudo rm -fr /Library/Java/JavaVirtualMachines/jdk-9.jdk/
sudo rm -fr /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin
sudo rm -fr /Library/PreferencePanes/JavaControlPanel.prefPane
```

##### INSTAL LEININGEN
- `brew install leiningen`
- NOTE: do NOT install per book instructions re: http://leiningen.org/ ([see below](#installing-leiningen-the-hard-and-unsuccessful-way))
##### Uninstalling Leiningen
- `brew uninstall leingingen`

### First!
`lein new app clojure-noob`
```clojure
(ns clojure-noob.core
  (:gen-class))

(defn -main
  "I don't do a whole lot ... yet."
  [& args]
  (println "I'm a little teapot!"))
```
1. `lein run`
2. `lein uberjar`
3. `java -jar target/uberjar/clojure-noob-0.1.0-SNAPSHOT-standalone.jar`
4. `lein repl`

### Emacs not your cup of tea? Try Clojure with [Vim](http://www.vim.org/)!
http://mybuddymichael.com/writings/writing-clojure-with-vim-in-2013.html

## Chapter 2 - How to Use Emacs, an Excellent Clojure Editor
https://www.braveclojure.com/basic-emacs/
> A quick feedback loop is crucial for learning. In this chapter, I cover Emacs from the ground up to guarantee you have an efficient Emacs/Clojure workflow.

- http://emacsformacosx.com/
- https://www.gnu.org/software/emacs/
- https://www.gnu.org/software/emacs/download.html#macos


# Part II: Language Fundamentals
> These chapters give you a solid foundation on which to continue learning Clojure. You’ll start by learning Clojure’s basics (syntax, semantics, and data structures) so you can do things. Then you’ll take a step back to examine Clojure’s most used functions in detail and learn how to solve problems with them using the functional programming mindset.

## Chapter 3 - Do Things: A Clojure Crash Course
https://www.braveclojure.com/do-things/
> This is where you’ll start to really dig into Clojure. It’s also where you’ll need to close your windows because you’ll start shouting, “HOLY MOLEY THAT’S SPIFFY!” at the top of your lungs and won’t stop until you’ve hit this book’s index.

> You’ve undoubtedly heard of Clojure’s awesome concurrency support and other stupendous features, but Clojure’s most salient characteristic is that it is a Lisp. You’ll explore this Lisp core, which is composed of two parts: functions and data.

## Chapter 4 - Core Functions in Depth
https://www.braveclojure.com/core-functions-in-depth/
> In this chapter, you’ll learn about a couple of Clojure’s underlying concepts. This will give you the grounding you need to read the documentation for functions you haven’t used before and to understand what’s happening when you try them.

> You’ll also see usage examples of the functions you’ll be reaching for the most. This will give you a solid foundation for writing your own code and for reading and learning from other people’s projects. And remember how I mentioned tracking glittery vampires? You’ll do that in this chapter (unless you already do it in your spare time).

## Chapter 5 - Functional Programming
https://www.braveclojure.com/functional-programming/
> In this chapter, you’ll take your concrete experience with functions and data structures and integrate it with a new mindset: the functional programming mindset. You’ll show off your knowledge by constructing the hottest new game that’s sweeping the nation: Peg Thing!

## Chapter 6 - Organizing Your Project: A Librarian’s Tale
https://www.braveclojure.com/organization/
> This chapter explains what namespaces are and how to use them to organize your code. I don’t want to give away too much, but it also involves an international cheese thief.

## Chapter 7 - Clojure Alchemy: Reading, Evaluation, and Macros
https://www.braveclojure.com/read-and-eval/
> In this chapter, we’ll take a step back and describe how Clojure runs your code. This will give you the conceptual structure you need to truly understand how Clojure works and how it’s different from other, non-Lisp languages. With this structure in place, I’ll introduce the macro, one of the most powerful tools in existence.

## Chapter 8 - Writing Macros
https://www.braveclojure.com/writing-macros/
> This chapter thoroughly examines how to write macros, starting with basic examples and advancing in complexity. You’ll close by donning your make-believe cap, pretending that you run an online potion store and using macros to validate customer orders.

# Part III: Advanced Topics
> These chapters cover Clojure’s extra-fun topics: concurrency, Java interop, and abstraction. Although you can write programs without understanding these tools and concepts, they’re intellectually rewarding and give you tremendous power as a programmer. One of the reasons people say that learning Clojure makes you a better programmer is that it makes the concepts covered in these chapters easy to understand and practical to use.

## Chapter 9 - The Sacred Art of Concurrent and Parallel Programming
https://www.braveclojure.com/concurrency/
> In this chapter, you’ll learn what concurrency and parallelism are and why they matter. You’ll learn about the challenges you’ll face when writing parallel programs and about how Clojure’s design helps to mitigate them. You’ll use futures, delays, and promises to safely write parallel programs.

## Chapter 10 - Clojure Metaphysics: Atoms, Refs, Vars, and Cuddle Zombies
https://www.braveclojure.com/zombie-metaphysics/
> This chapter goes into great detail about Clojure’s approach to managing state and how that simplifies concurrent programming. You’ll learn how to use atoms, refs, and vars, three constructs for managing state, and you’ll learn how to do stateless parallel computation with pmap. And there will be cuddle zombies.

## Chapter 11 - Mastering Concurrent Processes with core.async
https://www.braveclojure.com/core-async/
> In this chapter, you’ll ponder the idea that everything in the universe is a hot dog vending machine. By which I mean you’ll learn how to model systems of independently running processes that communicate with each other over channels using the core.async library.

## Chapter 12 - Working with the JVM
https://www.braveclojure.com/java/
> This chapter is like a cross between a phrase book and cultural introduction to the Land of Java. It gives you an overview of what the JVM is, how it runs programs, and how to compile programs for it. It also gives you a brief tour of frequently used Java classes and methods, and explains how to interact with them from Clojure. More than that, it shows you how to think about and understand Java so you can incorporate any Java library into your Clojure program.

## Chapter 13 - Creating and Extending Abstractions with Multimethods, Protocols, and Records
https://www.braveclojure.com/multimethods-records-protocols/
> In Chapter 4 you learn that Clojure is written in terms of abstractions. This chapter serves as an introduction to the world of creating and implementing your own abstractions. You’ll learn the basics of multimethods, protocols, and records.

## Appendix A: Building and Developing with Leiningen
https://www.braveclojure.com/appendix-a/
> This appendix clarifies some of the finer points of working with Leiningen, like what Maven is and how to figure out the version numbers of Java libraries so that you can use them.

## Appendix B: Boot, the Fancy Clojure Build Framework
https://www.braveclojure.com/appendix-b/
> Boot is an alternative to Leiningen that provides the same functionally, but with the added bonus that it’s easier to extend and write composable tasks. This appendix explains Boot’s underlying concepts and guides you through writing your first tasks.

## Afterword
- https://www.braveclojure.com/afterword/
- http://www.clojure-toolbox.com/
- [Luminus framework](http://www.luminusweb.net/)
- [Eric Normand’s Clojure Gazzette](http://www.clojuregazette.com/)
- [Clojure mailing list](https://groups.google.com/forum/#!forum/clojure)
- [Clojure subreddit](http://www.reddit.com/r/clojure)
- If Twitter is your social media outlet of choice, then @swannodette (David Nolen), @gigasquid (Carin Meier), @puredanger (Alex Miller), @ztellman (Zach Tellman), @bbatsov (Bozhidar Batsov), and @stuartsierra (Stuart Sierra) are your huckleberries. You could also follow me, @nonrecursive!

## Additional Clojure Resources
- http://www.4clojure.com/problems
- https://youtu.be/j-kj2qwJa_E
- http://lambdaisland.com/
- https://github.com/ahrjarrett/clojure-brave

## Build Electron Apps with Clojure
- https://github.com/Gonzih/cljs-electron

***

### Installing Leiningen the hard and unsuccessful way
- Per: http://leiningen.org/
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
- Possibly this was the result of installing the JAVA SE JRE instead of JDK, but whatevs... JDK + `brew install leiningen`... much easier!
