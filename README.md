# Languages cheatsheet

With this little helper, be always wary of the respective use-cases of the main programming languages.
*Warning: this is neither consistent nor professional, make your own opinion!*

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
 
 **What's that?** Compiled object oriented language

**How does it work?** Write .java files, compile them to .class files thanks to the javac compiler, and run those things on the Java Virtual Machine.

**What is it good for?** Cross plaftorm desktop applications, sometimes web (play framework) and server (glassfish). Since the JVM takes the hurdle of running your code on every supported platform, cross-platform comes easy.
*A lot of people hate on java for being slow. That is true compared to C or other languages, since the JVM has to transform java bytecode on the fly*
