```text
██████╗  ██████╗ ██████╗  ██████╗ ████████╗ ██████╗ ██████╗ ███╗   ██╗████████╗██████╗  ██████╗ ██╗     
██╔══██╗██╔═══██╗██╔══██╗██╔═══██╗╚══██╔══╝██╔════╝██╔═══██╗████╗  ██║╚══██╔══╝██╔══██╗██╔═══██╗██║     
██████╔╝██║   ██║██████╔╝██║   ██║   ██║   ██║     ██║   ██║██╔██╗ ██║   ██║   ██████╔╝██║   ██║██║     
██╔══██╗██║   ██║██╔══██╗██║   ██║   ██║   ██║     ██║   ██║██║╚██╗██║   ██║   ██╔══██╗██║   ██║██║     
██║  ██║╚██████╔╝██████╔╝╚██████╔╝   ██║   ╚██████╗╚██████╔╝██║ ╚████║   ██║   ██║  ██║╚██████╔╝███████╗
╚═╝  ╚═╝ ╚═════╝ ╚═════╝  ╚═════╝    ╚═╝    ╚═════╝ ╚═════╝ ╚═╝  ╚═══╝   ╚═╝   ╚═╝  ╚═╝ ╚═════╝ ╚══════╝
                                                                                                        
██████╗ ███████╗██╗   ██╗██╗      ██████╗  ██████╗ 
██╔══██╗██╔════╝██║   ██║██║     ██╔═══██╗██╔════╝ 
██║  ██║█████╗  ██║   ██║██║     ██║   ██║██║  ███╗
██║  ██║██╔══╝  ╚██╗ ██╔╝██║     ██║   ██║██║   ██║
██████╔╝███████╗ ╚████╔╝ ███████╗╚██████╔╝╚██████╔╝
╚═════╝ ╚══════╝  ╚═══╝  ╚══════╝ ╚═════╝  ╚═════╝ 
```

## BUILD 1105
- [ ] Develop 'Offline' mode with the new framework

## BUILD 1104
- [ ] Implement RobotPointers class
    - [ ] Low-level state description of Virtual, Streaming and Real robots
    - [ ] Link the virtual one to API-level instructions

## BUILD 1103
- [ ] Implement API-level instructions
    - [ ] .Move()
    - [ ] .MoveTo()
    - [ ] .Rotate()
    - [ ] .RotateTo()
    - [ ] .Transform()  // movement and rotation combined
    - [ ] .TRansformTo()
    - [ ] All the above in J mode (joint movement)
    - [ ] .Joints()    // relative joint movement
    - [ ] .JointsTo()  // absolute joint movement
    - [ ] .FullTransform()  // a full constructor with all 
    - [ ] .FullJoint()      // a full constructor

## BUILD 1102
- [x] Create a framework for abstract Actions
    - [x] Create Action class, very low-level: mostly just primitive properties.
    - [x] Design it to be either two types (transform vs joints) or a single one (how?)
    - [x] Add properties for abs/rel Pos, abs/rel Rot, abs/rel Joint, movement type (lin/joint), vel, zone.
    - [x] Create an ActionBuffer class where issued actions get buffered until released somewhere (to a file as a module, to the controller as an uploaded program, to he controller as individual targets).

## BUILD 1101
- [x] New class structure: 
    - [x] Split all the public Robot API from all the internal actual operations
    - [x] Centralize private methods into a Control class
    - [x] Add placeholder classes for future developments (Tool, Library, Solvers, etc.)
    - [x] Create a dedicated Communication class to handle connections to real/virtual controllers
- [x] Port all current functionality into the new structure
- [x] Make sure everything works as before with the new structure
- [x] Add Build number 
- [x] Merged ConnectionMode & OnlineMode into ControlMode 
- [x] Split off the Comm object
- [x] Remove all references to ABB objects from Control class.
- [x] Big comments review
- [x] Deep port of all functionality (make the Robot class basically a very shallow middleware for API purposes)
- [x] Dead code cleanup

## BUILD 1100
- [x] Recheck all examples are working correctly and nothing is broken before branching

## BUILDS 10xx
- Previous test and prototyping builds
- Transitioning to a split class architecture and more programmatic implementation


