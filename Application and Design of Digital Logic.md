# Application and Design of Digital Logic-----Gla.UESTC
## Topic 1--Introduction 

### Background
1. Why to learn?
* Digital systems are the core of modern electronic devices.
* Digital logic is the foundation for cutting-edge technologies like AI chips, embedded systems, 和 communication devices.
2. What to learn?
* Architecture of Computer---- `Von Neumann architecture` and its modules (controller, ALU, memory, etc.)
* Organization of CPU---***design logic of the control unit and datapath***, how the CPU operates internally.
* **Combinational logic, sequential circuits, testbenches, CPU design, timing analysis** ---组合逻辑、时序逻辑、测试平台、CPU设计与时序分析
3. How to Learn?
* Mathematic Foundations + EDA Technology  

### Architecture of Von Neumann computer
<img width="1195" height="934" alt="image" src="https://github.com/user-attachments/assets/7858e926-455a-407e-b0cb-70475eb2d395" />
1. Computer = CPU + Memory + Input + Output \ 
2. CPU = Controller + Datapath  \
3. Datapath = ALU + Registers + MUX + Shifters + Bus + ……  \
> Finction of datapath  \
> * Execute instruction operations (arithmetic, logic, comparison, etc.)  \
> * Transfer and temporarily store data (between registers or between memory and registers)  \
> * Provide input and output paths for the ALU (Arithmetic Logic Unit)  \
> * Act as a bridge between the control unit and memory  \
4. Bus = Data Bus + Address Bus + Control Bus   
<img width="885" height="537" alt="image" src="https://github.com/user-attachments/assets/10e878a8-7336-4e81-9f55-7a32ef43ab79" />
