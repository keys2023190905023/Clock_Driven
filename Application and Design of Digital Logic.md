# Application and Design of Digital Logic-----Gla.UESTC

### Table of Contents
- [Topic 1--Introduction](#topic-1--introduction)
  - [Background](#background)
  - [Architecture of Von Neumann computer](#architecture-of-von-neumann-computer)
  - [Organization of Center Processor Unit](#organization-of-center-processor-unit)
  - [Analog to Digital](#analog-to-digital)
  - [Mathematic Foundations](#mathematic-foundations)
  - [Number Systems](#number-systems)

---

## Topic 1--Introduction 
### Background
---
1. Why to learn?
* Digital systems are the core of modern electronic devices.
* Digital logic is the foundation for cutting-edge technologies like AI chips, embedded systems, 和 communication devices.
2. What to learn?
* Architecture of Computer---- `Von Neumann architecture` and its modules (controller, ALU, memory, etc.)
* Organization of CPU---***design logic of the control unit and datapath***, how the CPU operates internally.
* **Combinational logic, sequential circuits, testbenches, CPU design, timing analysis** ---组合逻辑、时序逻辑、测试平台、CPU设计与时序分析
3. How to Learn?
* Mathematic Foundations + EDA Technology  <br/><br/>
---
### Architecture of Von Neumann computer
---
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
   <img width="885" height="537" alt="image" src="https://github.com/user-attachments/assets/10e878a8-7336-4e81-9f55-7a32ef43ab79" /><br/>
   
* 可以复用
---
### Organization of Center Processor Unit
---
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

* CPU will be discussed in another storage
  
---
### Analog to Digital
---
Sampling--->quantifying & coding--->representing<br/>
#### Digital VS Analog
1. Analog signal<br/>
   <img width="776" height="152" alt="image" src="https://github.com/user-attachments/assets/d92919a4-5beb-45d0-ab9b-47215f399f34" />
2. Digital signal<br/>
   <img width="806" height="187" alt="image" src="https://github.com/user-attachments/assets/793f89da-ca55-4135-9c48-dd63a0b030bb" /><br/>

   
---
### Mathematic Foundations
---
#### Boolean / Logic / Switch Algebra
####  Positional & Polynomial Notation of Number
> A fundamental concept in digital systems: how numbers are represented using position and base (radix).<br/>
#####  General Form
A number `N` in radix `r` can be expressed as:
N = (dₙ₋₁ dₙ₋₂ ... d₁ d₀ . d₋₁ d₋₂ ... d₋ₘ)ᵣ


- `dᵢ`: digit at position `i`
- `r`: radix (base), e.g. 10 for decimal, 2 for binary
- `.`: radix point (decimal point)
- Digits to the **left** of the radix point: **integer digits**
- Digits to the **right**: **fractional digits**
- `dₙ₋₁`: Most Significant Digit (MSD)
- `d₋ₘ`: Least Significant Digit (LSD)

  
#### Polynomial Expansion

The value of `N` is calculated as: N = dₙ₋₁·rⁿ⁻¹ + dₙ₋₂·rⁿ⁻² + ... + d₀·r⁰ + d₋₁·r⁻¹ + d₋₂·r⁻² + ... + d₋ₘ·r⁻ᵐ

---
### Number Systems
---

- Digital system are built from circuits that process binary digits – 0s and 1s  ## 所有数字系统的底层运算和逻辑都是基于“0/1”进行的
- Real-life numbers, events,  conditions → binary digits  ## “编码”（Encode）过程的核心 —— 把模拟世界的信息转成数字世界可识别的格式。
- Binary number system and binary arithmetic  ## 加法、减法、乘法、除法等运算规则，都是基于 0 和 1 的逻辑推导
- Encode ## 编码：将文字、图像、声音等现实信息编码成“0/1”二进制形式，用于计算和传输

#### Positional Number Systems
> A number is represented by a string of digits where each digit position has an associated weight. ## 按位计数法
* Decimal Number<br/>
  <img width="814" height="450" alt="image" src="https://github.com/user-attachments/assets/4a3dc60e-85b0-4be5-8914-2753e08cef54" />
> Most significant digit(MSD):(p-1)<br/>
> Least significant digit(LSD):-n
* Binary Number<br/>
<img width="847" height="226" alt="image" src="https://github.com/user-attachments/assets/0b1e1472-310d-4e19-887e-cd7a76553f53" />

> Most significant bit(MSB)<br/>
> Least significant bit(LSB)
* Supplementary Knowledge
> bit<br/>
> 1 byte = 8 bit<br/>
> Memory:<br/>
> 256M = 256M bytes<br/>
> 1KB = 1024 bytes<br/>
> 1MB = 1024 * 1024 bytes<br/>
> 1GB = 1024 * 1024 * 1024 bytes

#### Analyze according to precision
<img width="1117" height="376" alt="image" src="https://github.com/user-attachments/assets/98a41cbd-8cad-41f5-a4ef-cdfa5b5d8f18" />

#### Number Conversion 
1. Octal number <---> Binary number
> `each octal number = 3-bit binary number`<br/>
> 2 nibbles = 1 byte = 8 bits<br/>
<img width="684" height="310" alt="image" src="https://github.com/user-attachments/assets/256a31b2-980c-48ba-9972-540f84dcfa29" /><br/>
2. Hexadecimal number <---> Binary number
> `each hexademical number = 4-bit binary number`<br/>
<img width="678" height="343" alt="image" src="https://github.com/user-attachments/assets/53f4f87a-0b27-4bb7-ba19-3fdad9173052" /><br/>

#### Binary addition and subtraction
<img width="575" height="381" alt="image" src="https://github.com/user-attachments/assets/17ded020-3149-4785-9591-215e250f3d64" />
<img width="585" height="355" alt="image" src="https://github.com/user-attachments/assets/c72a05cf-525d-4871-b6ef-0f4e9cd1d2ef" />
<img width="577" height="319" alt="image" src="https://github.com/user-attachments/assets/79677ca8-cebe-4e9a-bad7-72f8545b149b" />

#### Signed-Magnitude Representation  --  符号-数值表示法  ***True Form真值***
> `MSB --->  Sign Bit  ( 0 = plus, 1 = minus )`
1. +0 = 00000000 | -0 = 10000000
2. n-bit signed-magnitude 整数范围公式 
<img width="271" height="44" alt="image" src="https://github.com/user-attachments/assets/f31e4d4f-8c06-4c4a-87d1-f8b3f475b437" /><br/>
3. The signed-magnitude system has an equal number of positive and negative integers

#### Complement Number Systems -- ***反码补码***
1. Radix-Complement(基数补码）
If a number D is complemented twice, the result is D.
<img width="679" height="225" alt="image" src="https://github.com/user-attachments/assets/d9941b8c-7f67-4b28-9059-dba66811cb9e" /><br/>
2. Diminished Radix – Complement（基数减1补码表示法（反码））
<img width="571" height="167" alt="image" src="https://github.com/user-attachments/assets/2a7adc9b-49ee-4245-a694-d4c0b447a834" /><br/>
---
`In digital systems, positive integers are treated consistently across different number representations:`

> **For positive numbers, the original code, one’s complement, and two’s complement are exactly the same.** 正数的反码补码就是本身

There is no need to perform any transformation like bit inversion or addition.<br/>
<img width="649" height="159" alt="image" src="https://github.com/user-attachments/assets/01f4258c-ae23-4b36-bb70-f1b7637e1839" /><br/>

> **For positive numbers,Why No Changes for Positive Numbers?** 为什么不变

- The special transformations (bitwise NOT, +1) are only used for **negative numbers**.
- Positive values are already in a form that can be directly interpreted and used in arithmetic.  ## 加法器
- This simplifies hardware design — no need to convert before using adders or ALUs.

> ** Why Negative Numbers Need One's and Two's Complement？ **
In digital logic systems, negative numbers cannot be directly handled by binary adders if we simply use sign bits (original code). To allow a unified circuit (adder) to process both positive and negative numbers without separate subtraction hardware, negative numbers are encoded in a way that makes subtraction possible via addition.<br/>

---

### Code
> A set of n-bit strings in which different bit strings represent different numbers or other things is called a code.<br/>

* 代表某事或某物的一组n位二进制码
* three data units（3位二进制码）：bit/byte/word
  
<img width="645" height="149" alt="image" src="https://github.com/user-attachments/assets/b4a033cd-4bf0-4b6a-b04f-4b4b4bf52da4" />
> Binary Codes for Decimal Numbers(十进制数的二进制编码)

#### Binary-code decimal(BCD）
> encodes the digits 0 through 9 by their 4-bit unsigned binary representations, 0000 through 1001.

> The code words 1010 through 1111 are not used.(用 0000－1001 来表示十进制数 0－9.)---》一字节可表示0-99

