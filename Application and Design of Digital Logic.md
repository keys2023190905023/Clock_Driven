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
* Mathematic Foundations + EDA Technology  <br/><br/>

### Architecture of Von Neumann computer
<img width="1195" height="934" alt="image" src="https://github.com/user-attachments/assets/7858e926-455a-407e-b0cb-70475eb2d395" />
1. Computer = CPU + Memory + Input + Output<br/>
2. CPU = Controller + Datapath<br/>
4. Datapath = ALU + Registers + MUX + Shifters + Bus + ……  <br/>
<blockquote>
 Finction of datapath:<br/>
* Execute instruction operations (arithmetic, logic, comparison, etc.)<br/>
* Transfer and temporarily store data (between registers or between memory and registers)<br/>
* Provide input and output paths for the ALU (Arithmetic Logic Unit)<br/>
* Act as a bridge between the control unit and memory<br/>
</blockquote>
5. Bus = Data Bus + Address Bus + Control Bus   
<img width="885" height="537" alt="image" src="https://github.com/user-attachments/assets/10e878a8-7336-4e81-9f55-7a32ef43ab79" /><br/><br/>

### Organization of Center Processor Unit
<img width="1592" height="872" alt="image" src="https://github.com/user-attachments/assets/d227727e-8966-4b01-bfbb-84a06c6c1af9" />
MUX：A multiplexer is a combinational circuit that selects one of many input signals and forwards the selected input to a single output line.
<blockquote>
MUX（Multiplexer，多路选择器）是一种能够从多个输入中“选择”一个，并将其传送到输出的电路。<br/>
  Select one of multiple inputs to feed the ALU <br/>
  Switch between external data input and constant '0'<br/>
  Selection controlled by control signals
</blockquote>
Register:<br/>
| ① 暂存计算结果------| 存储 ALU 的输出，为下一步运算做准备----------| *Stores the result from ALU temporarily for further operations*               <br/>
| ② 提供 ALU 操作数---| 当前寄存器内容可以再次送入 ALU，形成数据回环--| *Acts as operand input to ALU, forming a feedback loop*                      <br/>
| ③ 数据输出接口------| 作为系统的 `Data Outputs`，可输出到外部------| *Provides final data output to the external bus/system*                      <br/>
| ④ 与状态控制联动----| 配合状态机形成多周期操作的中间存储------------| *Works with controller to hold intermediate values in multi-cycle execution* <br/>

