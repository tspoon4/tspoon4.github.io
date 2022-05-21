<style>body { background-color:black; color:grey; }</style>

[https://github.com/tspoon4](https://github.com/tspoon4)  
A list of topics with pointers to start reflecting...

## Entries
* [2022-05-19 NVMe the game changer](#2022-05-19-nvme-the-game-changer)
* [2022-01-17 Everything is a Table](#2022-01-17-everything-is-a-table)
* [2022-01-04 Everything is a FSM](#2022-01-04-everything-is-a-fsm)
* [2021-12-31 Code quality](#2021-12-31-code-quality)
* [2021-12-11 Amazing software](#2021-12-11-amazing-software)

## 2022-05-19 NVMe the game changer
We have lived with slow HDD for a long time.  
All of the sudden, we get SSD and then NVMe that provides a x40 boost factor to load data.  
This new support raises multiple challenges in the way we program applications.  
* NVMe bandwidth (~3GB/s) is fast compared to the fastest software decompression: keep data uncompressed
* NVMe bandwidth (1MB/325us) is slow compared to CPU processing: blocking IO still has be avoided
* Leverage IO libraries that expose asynchronous IO commands such as libaio (Linux), DirectStorage (Windows)
* Prepare the data so that it doesn't have to be moved and processed by CPU: load in place
* Design code to send IO requests in advance and avoid blocking the threads

## 2022-01-17 Everything is a Table
A big part of everyday's work is actually about producing data tables, either manually or automatically.  
I often review verbose documents that miss the target: an exhaustive list of items so we can draw correct conclusions.  
Like any table, it is very important to carefully design the data (i.e. columns) so we can extract as much information as possible.  
Maybe this page should be a big markdown table...  
* A backlog is a task list used to organize work and create burndown charts (name, priority, estimation, details...)  
* A comparison matrix allows to visualize differences and similarities between products (columns are your feature requirements)  
* Pros and cons tables help you to make decisions (feature, advantages, drawbacks, comments...)  

## 2022-01-04 Everything is a FSM
Everything is a Finite State Machine or a hierarchy of Finite State Machines from a higher perspective.  
FSM transitions and states should be made obvious when programming by using FSM related designs.  
* Input messages and their processing in GUI applications
* Game states (loading, menu, gameplay, cutscene...) in games
* Behavior states (idle, goto, fight, retreat...) for NPC game logic
* Animation states (idle, walk, run, jump...) for character animation
* A simple door (closed, opening, opened, closing, broken...)

switch(state)  
{  
  case STATE_0: // This is a state  
    ...  
    state = STATE_1; // This is a transition  
    break;  
  ...  
}  

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

