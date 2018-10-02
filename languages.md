# Languages cheatsheet

With this little helper, be always wary of the respective use-cases of the main programming languages.  

***Warning**: this is not an objective work, it represents my thoughts about each language according to how they were introduced to me.  
 Make your own opinion!*

## WebAssembly

**What's that?** Bytecode format for in-browser client-side scripting

**How does it work?** Write code in one language,compile it to WA,  making it portable everywhere .wasm is supported
  - mostly browsers
  
**Why doing that?** After all, many languages compile to JS, so....
  - JS parsing takes time, WA promises up to 20x speedup

*For the moment, only C/C++ is supported*  
source: https://tomassetti.me/introduction-to-webassembly/
 
## JS

**What's that?** Scripting &  interpreted language, running on all main browsers
  
 **How does it work?** Write many .js files with a bunch of imports/exports, use webpack to minimize it to one file and run it on your browser's JS engine:
  - Chrome: V8 engine
  - Firefox: Spidermonkey engine
  - Safari: Nitro engine, but who cares ?
  - Edge: Chakra engine
  
 **What is it good for?** Web apps, cross-platform apps using webviews, but also REST APIs thanks to NodeJS.
 
 ## Java
 
 **What's that?** One of the most famous object-oriented language out there.

**How does it work?** Write .java files, compile them to .class files thanks to the javac compiler, and run those things on the Java Virtual Machine.

**What is it good for?** Cross plaftorm desktop applications, sometimes web (play framework) and server (glassfish). Since the JVM takes the hurdle of running your code on every supported platform, cross-platform comes easy.
*A lot of people hate on java for being slow. That is true compared to C or other languages, since the JVM has to transform java bytecode on the fly*


## Go

**What's that?** Developed by Google, compiled, performs well parrallel computations & networking. Close to C. Compiles fast.

**How does it work?** Write your .go file, compile it to bytecode thanks to the [Go Toolchain](https://golang.org/doc/install).

**What's particular with it?**
  - Concise variable declaration:  `i:=2` equivalent to `var i int = 2`  
  -> basically trough type inference the compiler knows i is an integer

  - Efficient thread-like routines 
  - Toolchain produces statically linked binaries. That is, you don't need any additionnal dependency to execute your binary!

  **What is it good for?** High performance REST APIs, close to C performance but easier to use. Basically for back-end purposes, or to balance another language's weaknesses.  
  *Ex:* Machine learning in python, but HTML requests handled by a Go module.

## C

**What's that?**   
  - Compiled  
  - Imperative (you describe what happens in the program),
  - Procedural (it calls procedures - aka functions - and handles their results) 

**How does it work?** 

 Write your .c files, compile it to bytecode thanks to any C compiler ([gcc](https://gcc.gnu.org/) for instance).  
In my opinion, the build process is pretty painful, and involves:
  - **A Makefile**: this explains to the compiler how your program should be compiled, according to which architecture, etc.
  - **CMake**: tool aiming to reduce the pain of generating a correct Makefile (useful if you want to support many architectures, or need compilation flags per platform,..)

**What's particular with it?**

Due to its low-level nature,developers have to **take care of the memory by themselves** - that is, allocate memory space for the different variables, etc.  
> This allows fast and memory-efficient programs, at the cost of developer time

**What is it good for?** High performance low-level programs, for example:
  - integrated systems
  - linux kernel
  - video/audio codecs
  