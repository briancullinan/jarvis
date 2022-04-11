# Jarvis

Like Jenkins, but with shoes, and a hat, and the rest. Jarvis is just a 3D build system.
When I worked on an education app, I wrote a graph of all the automated integration tests.
Years later, I realize this kind of visual is hardly available. Github Actions still has 
some problems that make it painful to use. The same kind of painful the job servers from
20 years ago had. Nothing has changed.

### Until now!

What if you could build your entire software stack, from a web browser? That is Jarvis' goal.
That way, someone else can build your entire stack from their browser too!

## Short term

1) Use WASM git-scm and Ace9 to make a basic code editor, parse build instructions
2) Display code in 3D, contributor are Roots, trunk and branches are code features. Leaves are 
small trees of code changes, either function call tree, or the AST (abstract syntax tree) of the 
changes we're looking at for that specific file and branch. Small branches for #includes, leaves
for code.
3) Build automation tools, pure-Make (a prolog alternative with FS), cross-compiling architecture,
disassembly, project a binary file using spatial indexing. Treat all #ifdef results as 1 long piece
of binary executable, as if the #ifdef was compiled to x86 assembly and you use a COMPILE_FLAG on
and exe instead of on the compile. i.e. Combine postgis/botlib with static-lib .a outputs from many
pre-built features / generizing dependency order.
4) Gameifying building open-source projects that are missing features like WASM, or
different OSes builds, or making mashups.


## How do stacks work?

Morpheus' build

* Webkit/DevTools
* planet_quake/clang/Ace9 - should be grouped together because Ace9 will be built in for editing .cfg with a word theme
* text to speech/NLP - intent
* keywhiz/sequins/leveldb - secure database for credentials and storage
* morpheus/goals - automated tasks, searches and scraping, communications and data bank

Jarvis' build:

* Webkit
* planet_quake/clang/Ace9
* text to speech/NLP - intent
* secure database - for git token and dev API keys
* jarvis/goals - self-hosted web worker code kernels, git wasm local, mesh VFS (opt-in), 
  cloud deploy apis, mesh WASM job server (opt-in)


1) Do checkouts, configure
2) Do patches, fractalize code tree. i.e. every #ifdef is switched on and off, try to compile,
    on positive results, iterate every branch. On every branch, positive result, iterative every
    code line change. On every line change, iterate every unit test/integration test. On every
    positive test, build final output. Compare assembly code tree.
3) Deploy jobs to mesh job server for static hosting or functional use. Deploy job to job store
  for employment by other jarvis instances in player graph.


