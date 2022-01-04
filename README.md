<style>body { background-color:black; color:grey;}</style>

A list of topics with pointers to start reflecting...

## Entries
* [2022-01-04 Everything is a FSM](#2022-01-04-everything-is-a-fsm)
* [2021-12-31 Code quality](#2021-12-31-code-quality)
* [2021-12-11 Amazing software](#2021-12-11-amazing-software)

## 2022-01-04 Everything is a FSM
Everything is a Finite State Machine or a hierarchy of Finite State Machines from a higher perspective.  
FSM transitions and states should be made obvious when programming by using FSM related designs.  
* Input messages and their processing in GUI applications
* Game states (loading, menu, gameplay, cutscene...) in games
* Behavior states (idle, goto, fight, retreat...) for NPC game logic
* Animation states (idle, walk, run, jump...) for character animation
* A simple door (closed, opening, opened, closing, broken...)

> switch(state)  
> {  
>     case STATE_0: // This is a state  
>       ...  
>       state = STATE_1; // This is a transition
>       break;
> ...  
> }  

## 2021-12-31 Code quality
Code quality is often defined with aspects difficult to measure.  
We should instead value and promote code with:  
* Minimal API surface
* Minimal set of dependencies
* Minimal amount of LOC
* Fast compilation time
* Energy efficient execution

## 2021-12-11 Amazing software
I have infinite admiration for these pieces of software.  
1. [Linux](https://github.com/torvalds/linux)
2. [Firefox](https://www.mozilla.org/en-US/firefox/)
3. [PostgreSQL](https://www.postgresql.org/)
4. [Renderdoc](https://renderdoc.org/)
5. [Wine](https://www.winehq.org/)
6. [Ghidra](https://github.com/NationalSecurityAgency/ghidra)
7. **C/C++**: Eigen, OpenCV, Vulkan, ImGui
8. **Python**: Pandas, NumPy, SciPy, Scikit-Learn, Matplotlib
9. **CLI**: gcc, git, rsync, curl
