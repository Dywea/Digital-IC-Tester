# Digital-IC-Tester
Being in electronics Major,I was needed to make something that was related to electronics. As I have already experienced due to not working of ICs, so I made one DIGITAL IC TESTER, although i wasn,t able to use arduino because I have made it during quarantine . So Just let's start with it. I am writing codes here, and rest of the images can be seen in the word file linked.
1.02  Introduction To Microcontroller
 Microcontroller is an electronic device which is used as a computing unit or arithmetic unit like a computer
On the other hand, it can be said that it is a data processing unit. Sometimes it may be used to control a device, i.e. turn on or turn off  a device or control a device. It is a 40pin IC having HARVARD architecture with 16 bit address bus and 8 bit data bus and 64KByte programming memory and 64Kbyte data memory

1.02.1	 What is microcontroller?
        A microcontroller is also known as a true computer on a single chip. It has a CPU,PC ,SP registers, in addition to a fixed amount of RAM,ROM and I/O ports, including               serial communication & timer, all embedded together on a single chip. In some microcontrollers an ADC & DAC are also embedded in a single chip.
1.02.2	 Microcontroller Chip Details Which We Use
         The next part of the proposed work is the temperature monitoring. The 8051 microcontroller is used here as the main controller. The microcontroller used here is known as           AT89C52 which has 8KB on-chip flash memory, 256 bytes of Ram, 4 ports each of 8 bit P0-P3, 3 timers, serial communication module and interrupt module makes the system             more versatile for our present project work.
2	BRIEF DESCRIPTION OF 8051 MICROCONTROLLER

2.01	General Details:
     A microcontroller is also known as a true computer on a single chip. It has a CPU, PC,SP registers, in addition to a fixed amount of RAM,ROM and I/O ports, including serial        communication system and timer, all embedded together on a single chip. In some microcontrollers an ADC & DAC are also embedded on a single chip
  
2.02  Comparisons between microprocessor and microcontroller:

                       It is a 40 pin IC		                                                             It is a 40 pin IC
                       It has a 16 bit address bus	                                                     It has a 16 bit address bus
                       It has a 8 bit data bus	                                                         It has a 8 bit data bus
                       Developed by VON NEUMANN architecture	                                           Developed by Harvard architecture.

                       Slower than 8051 controller	                                                     Faster than 8085 processor
                       Available memory-64kbyte		                                                       Available memory-64kbyte program memory 
                                                                                                         64kbyte data memory
                      Operating frequency-3 to 5 MHz	                                                   Operating frequency-12 MHz
                      RAM,ROM Interrupt 	Controller, bus controller,                                    RAM,ROM Interrupt 	Controller, bus controller,
                      I/O ports etc are connected externally.		                                         I/O ports etc are connected internally.	
                                                                                                        
                      Multi-purpose(single processor Can be used for many jobs)                 	Used for dedicated purpose (single controller can be used for  single purpose)   
                      Costlier.	                                                                          Cheaper.
                     It is much bulkier due to attached circuitry                                       	Lighter as on chip circuitry.
                                                    Table.1: Comparisons between microprocessor and microcontroller
                                                    
                                                    
   2.03  Advantages of Harvard Architecture:
                 •	 It has two types of memories separated.
                 •	Data can be accessed even when program is being executed i.e. instruction fetches can occur in parallel with data transfers.
                 •	Much faster due to presence of separate data and program memory.
                 •	Data  much secured.
                                                 
                                                    
2.04 Memory Organization: 

       The 8051 has three very general types of memory. To effectively program the 8051 it is necessary to have a basic understanding of these memory types.
       The memory types are illustrated in the following graphic. They are: On-Chip Memory, External Code Memory, and External RAM.


 External Code Memory:
        External Code Memory is code (or program) memory that resides off-chip. This is often in the form of an external EPROM. Code memory is the memory that holds the                 actual 8051 program that is to be run. This memory is limited to 64K and comes in many shapes and sizes: Code memory may be found on-chip, either burned into the                 microcontroller as ROM or EPROM. Code may also be stored completely off-chip in an external ROM or, more commonly, an external EPROM. Flash RAM is also another popular           method of storing a program. Various combinations of these memory types may also be used--that is to say, it is possible to have 4K of code memory on-chip and 64k of             code memory off-chip    in an EPROM.
        When the program is stored on-chip the 64K maximum is often reduced to 4k, 8k, or 16k. This varies depending on the version of the chip that is being used. Each version         offers specific capabilities and one of the distinguishing factors from chip to chip is how much ROM/EPROM space the chip has.
        However, code memory is most commonly implemented as off-chip EPROM. This is especially true in low-cost development systems and in systems developed by students.
 External RAM: 

       External RAM is RAM memory that resides off-chip. This is often in the form of standard static RAM or flash RAM. As an obvious opposite of Internal RAM, the 8051 also            supports what is called External RAM.
       As the name suggests, External RAM is any random access memory which is found off-chip. Since the memory is off-chip it is not as flexible in terms of accessing, and is          also slower. For example, to increment an Internal RAM location by 1 requires only 1 instruction and 1 instruction cycle. To increment a 1-byte value stored in External          RAM requires 4 instructions and 7 instruction cycles. In this case, external memory is 7 times slower!
       What External RAM loses in speed and flexibility it gains in quantity;  While Internal RAM is limited to 128 bytes (256 bytes with an 8052), the 8051 supports External          RAM up to 64K.
On-Chip Memory:
       On-Chip Memory refers to any memory (Code, RAM, or other) that physically exists on the microcontroller itself.
       The 8051 includes a certain amount of on-chip memory. On-chip memory is really one of two types: Internal RAM and Special Function Register (SFR) memory. The layout of          the 8051's internal memory is presented in the following memory map:

What Are SFRs? 
      The 8051 is a flexible microcontroller with a relatively large number of modes of operations. Your program may inspect and/or change the operating mode of the 8051 by           manipulating the values of the 8051's Special Function Registers (SFRs).
      SFRs are accessed as if they were normal Internal RAM. The only difference is that internal RAM is from address 00h through 7Fh whereas SFR registers exist in the address       range of 80h through FFH.       
      Each SFR has an address (80h through FFH) and a name as shown in the above figure (a). As you can see, although the address range of 80h through FFH offers 128 possible         addresses, there are only 21 SFRs in a standard 8051. All other addresses in the SFR range (80h through FFH) are considered invalid. Writing to or reading from these             registers may produce undefined values or behavior.

 SFR Types 
      As we can see in the figure (a) itself, SFRs related to the I/O ports. The 8051 has four I/O ports of 8 bits, for a total of 32 I/O lines. Whether a given I/O line is high       or low and the value read from the line are controlled by the other SFRs in green. 

      Some SFRs which in some way control the operation or the configuration of some aspect of the 8051; For example, TCON controls the timers, SCON controls the serial port.

      The remaining SFRs, with green backgrounds, are "other SFRs." These SFRs can be thought of as auxiliary SFRs in the sense that they don't directly configure the 8051 but         obviously the 8051 cannot operate without them. For example, once the serial port has been configured using SCON, the program may read or write to the serial port using         the SBUF register.

SFR Descriptions

     In This section we will discuss each of the standard SFRs found in the above SFR figure (a)

     P0 (Port 0, Address 80h, and Bit-Addressable): This is input/output port 0. Each bit of this SFR corresponds to one of the pins on the microcontroller. For example, bit 0        of port 0 is pin P0.0, bit 7 is pin P0.7. Writing a value of 1 to a bit of this SFR will send a high level on the corresponding I/O pin whereas a value of 0 will bring it        to a low level.
SP (Stack Pointer, Address 81h): 
     This is the stack pointer of the microcontroller. This SFR indicates where the next value to be taken from the stack will be read from in Internal RAM. If you push a value      onto the stack, the value will be written to the address of SP + 1. That is to say, if SP holds the value 07h, a PUSH instruction will push the value onto the stack at          address 08h. This SFR is modified by all instructions which modify     the stack, such as PUSH, POP, and LCALL, RET, RETI, and whenever interrupts are provoked by the            microcontroller.
DPL/DPH (Data Pointer Low/High, Addresses 82h/83h): 
    The SFRs DPL and DPH work together to represent a 16-bit value called the Data Pointer. The data pointer is used in operations regarding external RAM and some instructions       involving code memory. Since it is an unsigned two-byte integer value, it can represent values from 0000h to FFFFH (0 through 65,535 decimal).
PCON (Power Control, Addresses 87h): 
   The Power Control SFR is used to control the 8051's power control modes. Certain operation modes of the 8051 allow the 8051 to go into a type of "sleep" mode which requires      much less power. These modes of operation are controlled through PCON. Additionally, one of the bits in PCON is used to double the effective baud rate of the 8051's serial      port.
 
                                                          D7 	D6 	D5 	D4 	D3 	D2 	D1 	D0 
                                                       SMOD 	x 	x 	x 	GF1 	GF0 	PD 	IDL 
 
         •	SMOD – Serial mode bit used to determine the baud rate with Timer 1. 
                    Baud rate= Oscillator frequency in Hz / N [256-(TH1)]
         •	If SMOD = 0 then N = 384. If SMOD = 1 then N = 192. TH1 is the high byte of timer 1 when it is in 8-bit auto reload mode. 
         •	GF1 and GF0 are General purpose flags not implemented on the standard device 
         •	PD is the power down bit. Not implemented on the standard device 
         •	IDL activate the idle mode to save power. Not implemented on the standard device

TCON (Timer Control, Addresses 88h, and Bit-Addressable): 
           The Timer Control SFR is used to configure and modify the way in which the 8051's two timers operate. This SFR controls whether each of the two timers is running or              stopped and contains a flag to indicate that each timer has overflowed. Additionally, some non-timer related bits are located in the TCON SFR. These bits are used to            configure the way in which the external interrupts are activated and also contain the external interrupt flags which are set when an external interrupt has occurred.
                                                                D7 	D6 	D5 	D4 	D3 	D2 	D1 	D0 
                                                       TF1 	TR1 	TF0 	TR0 	IE1 	IT1 	IE0 	IT0 

            •	TF1 – Timer 1 overflow flag 
            •	TR1 – Timer 1 run control bit 
            •	TF0 – Timer 0 overflow flag 
            •	TR0 – Timer 0 run control bit 
            •	IE1 – External interrupt 1 edge flag. Set to 1 when edge detected. 
            •	IT1 – Edge control bit for external interrupt 1. 1 = edge, 0 = level 
            •	IE0 – External interrupt 0 edge flag. Set to 1 when edge detected 
            •	IT0 – Edge control bit for external interrupt 0. 1 = edge, 0 = level

TMOD (Timer Mode, Addresses 89h): 
           The Timer Mode SFR is used to configure the mode of operation of each of the two timers. Using this SFR your program may configure each timer to be a 16-bit timer, an            8-bit auto reload timer, a 13-bit timer, or two separate timers. Additionally, you may configure the timers to only count when an external pin is activated or to                count "events" that are indicated on an external pin.




                                                         D7 	D6 	 D5 	D4 	D3 	D2 	D1 	D0 
                                                        Gate 	C/T  M1 	M0 	Gate 	C/ TM1 	M0 
       Timer 1 	Timer 0 

        •	Gate – if 1 timer x is enabled when INTx is high and TRx is high. if 0 timer x is enabled when TRx is high. 
        •	C/T- if 1 timer x is clocked from Tx pin. if 0 timer x is clocked from oscillator/12  



                                 M1	  M0	                                    MODE
                                 0	   0	13- bit  mode for compatibility to 8084 family
                                 0	   1	16-bit timer/counter. user must reload in software
                                 1	   0	8-bit auto reload. TLx is automatically reloaded from THx
                                 1	   1	TL0 is 8-bit counter controlled by Timer0 control bits.TH0 is 8-bit counter controlled by Timer1 control bits.Timer1 is stopped

TL0/TH0 (Timer 0 Low/High, Addresses 8Ah/8Ch): 
         These two SFRs, taken together, represent timer 0. Their exact behavior depends on how the timer is configured in the TMOD SFR; however, these timers always count up.            What is configurable is how and when they increment in value.
TL1/TH1 (Timer 1 Low/High, Addresses 8Bh/8Dh):
         These two SFRs, taken together, represent timer 1. Their exact behavior depends on how the timer is configured in the TMOD SFR;            however, these timers always          count up. What is configurable is how and when they increment in value.
P1 (Port 1, Address 90h, and Bit-Addressable): 
          This is input/output port 1. Each bit of this SFR corresponds to one of the pins on the microcontroller. For example, bit 0 of port 1 is pin P1.0, bit 7 is pin P1.7.             Writing a value of 1 to a bit of this SFR will send a high level on the corresponding I/O pin whereas a value of 0 will bring it to a low level.

SCON (Serial Control, Addresses 98h, Bit-Addressable): 
         The Serial Control SFR is used to configure the behavior of the 8051's on-board serial port. This SFR controls the baud rate of the serial port, whether the serial port          is activated to receive data, and also contains flags that are set when a byte is successfully sent or received.  
                                                                           D7 	D6 	D5 	D4 	D3 	D2 	D1 	D0 
                                                                        SM0 	SM1 	SM2 	REN 	TB8 	RB8 	TI 	RI 


                     •	SM2 – Enables multiprocessor communication in modes 2 and 3. 
                     •	REN – Receiver enable 
                     •	TB8 – Transmit bit 8. This is the 9th bit transmitted in modes 2 and 3. 
                     •	RB8 – Receive bit 8. This is the 9th bit received in modes 2 and 3. 

                     •	TI – Transmit interrupt flag. Set at end of character transmission. Cleared in software. 
                     •	RI – Receive interrupt flag. Set at end of character reception. Cleared in software.

                                                               SM0	      SM1	 Operation 	Baud rate
                                                                0	      0	Shift register	Osc/12
                                                                0	      1	8-bit UART	Set by timer
                                                                1	      0	9-bit UART	Osc/12 or Osc/64
                                                                1	      1	9-bit UART	Set by timer

SBUF (Serial Control, Addresses 99h):
             The Serial Buffer SFR is used to send and receive data via the on-board serial port. Any value written to SBUF will be sent out the serial port's TXD pin. Likewise,              any value which the 8051 receives via the serial port's RXD pin will be delivered to the user program via SBUF. In other words, SBUF serves as the output port when               written to and as an input port when read from.

P2 (Port 2, Address A0h, and Bit-Addressable):
             This is input/output port 2. Each bit of this SFR corresponds to one of the pins on the microcontroller. For example, bit 0 of port 2 is pin P2.0, bit 7 is pin                  P2.7. Writing a value of 1 to a bit of this SFR will send a high level on the corresponding I/O pin whereas a value of 0 will bring it to a low level.

IE (Interrupt Enable, Addresses A8h): The Interrupt Enable SFR is used to enable and disable specific interrupts. The low 7 bits of the SFR are used to enable/disable the specific interrupts, where as the highest bit is used to enable or disable ALL interrupts. Thus, if the high bit of IE is 0 all interrupts are disabled regardless of whether an individual interrupt is enabled by setting a lower bit.

                                                           D7 	D6 	D5 	D4 	D3 	D2 	D1 	D0 
                                                          EA 	x 	ET2 	ES 	ET1 	EX1 	ET0 	E 


                                                          •	EA – Global interrupt enable 
                                                          •	x – not defined 
                                                          •	ET2 – Timer 2 interrupt enable 
                                                          •	ES – Serial port interrupt enable 
                                                          •	ET1 – Timer 1 interrupt enable 
                                                          •	EX1 – External interrupt 1 enable 
                                                          •	ET0 – Timer 0 interrupt enable 
                                                          •	EX0 – External interrupt 0 enable

P3 (Port 3, Address B0h, and Bit-Addressable):
                 This is input/output port 3. Each bit of this SFR corresponds to one of the pins on the microcontroller. For example, bit 0 of port 3 is pin P3.0, bit 7 is pin                  P3.7. Writing a value of 1 to a bit of this SFR will send a high level on the corresponding I/O pin whereas a value of 0 will bring it to a low level.


IP (Interrupt Priority, Addresses B8h, and Bit-Addressable): 
                The Interrupt Priority SFR is used to specify the relative priority of each interrupt. On the 8051, an interrupt may either be of low (0) priority or high (1)                   priority. An interrupt may only interrupt interrupts of lower priority. For example, if we configure the 8051 so that all interrupts are of low priority except                   the serial interrupt, the serial interrupt will always be able to interrupt the system, even if another interrupt is currently executing. However, if a serial 
                interrupt is executing no other interrupt will be able to interrupt the serial interrupt routine since the serial interrupt routine has the highest priority. 0


                                                               D7 	D6 	D5 	D4 	D3 	D2 	D1 	D0 
                                                           x 	x 	PT2 	PS 	PT1 	PX1 	PT0 	PX 


                                                                  •	x – not defined 
                                                                  •	PT2 – Priority for timer 2 interrupt 
                                                                  •	PS – Priority for serial port interrupt 
                                                                  •	PT1 – Priority for timer 1 interrupt 
                                                                  •	PX1 – Priority for external interrupt 1 
                                                                  •	PT0 – Priority for timer 0 interrupt 
                                                                  •	PX0 – Priority for external interrupt
                                                                  
                                                                 
 PSW (Program Status Word, Addresses D0h, and Bit-Addressable):
              The Program Status Word is used to store a number of important bits that are set and cleared by 8051 instructions. The PSW SFR contains the carry flag, the                       auxiliary carry flag, the overflow flag, and the parity flag. Additionally, the PSW register contains the register bank select flags which are used to select which               of the "R" register banks are currently selected.

                                                                 CY	  AC	 F0	  RS1	   RS0	   OV	--	   P

                                                                    •	CY	PSW.7	 	Carry flag. 
                                                                    •	AC	PSW.6		Auxiliary carry flag.
                                                                    •	F0      	PSW.5		Available to the user for general purpose.
                                                                    •	RS1	PSW.4       	           Register Bank selector bit 1.
                                                                    •	RS0	PSW.3 		Register Bank selector bit 0.
                                                                    •	OV	PSW.2		Overflow flag.
                                                                    •	--	           PSW.1		User definable bit.
      	P		PSW.0		Parity flag. Set/cleared by hardware each instruction cycle to indicate an Odd / even number of 1 bit in the accumulator.     
        
                                                                   RS1	     RS0	Register bank	Address
                                                                    0	      0	    0	00H-07H
                                                                    0	      1	    1	08H-0FH
                                                                    1	      0	    2	10H-17H
                                                                    1 	      1	    3	18H-1FH

ACC (Accumulator, Addresses E0h, and Bit-Addressable): The Accumulator is one of the most-used SFRs on the 8051 since it is involved in so many instructions. The Accumulator resides as an SFR at E0h, which means the instruction MOV A, #20h is really the same as MOV E0h,#20h. However, it is a good idea to use the first method since it only requires two bytes whereas the second option requires three bytes.

B (B Register, Addresses F0h, Bit-Addressable): The "B" register is used in two instructions: the multiply and divide operations. The B register is also commonly used by programmers as an auxiliary register to temporarily store values.


Basic Registers

The Accumulator: 
    The Accumulator, as its name suggests, is used as a general register to accumulate the results of a large number of instructions. It can hold an 8-bit (1-byte) value and is     the most versatile register the 8051 has due to the shear number of instructions that make use of the accumulator. More than half of the 8051’s 255 instructions manipulate       or use the accumulator in some way. 
    For example, if you want to add the number 10 and 20, the resulting 30 will be stored in the Accumulator. Once you have a value in the Accumulator you may continue               processing the value or you may store it in another register or in memory.
 
The "R" registers: 
     The "R" registers are a set of eight registers that are named R0, R1, etc.  Up to and including R7. These registers are used as auxiliary registers in many operations. 
     Perhaps you are adding 10 and 20. The original number 10 may be stored in the Accumulator whereas the value 20 may be stored in, say, register R4. To process the addition        you would execute the command: 
                                                                 ADD A, R4 
                                After executing this instruction the Accumulator will contain the value 30. 
            You may think of the "R" registers as very important auxiliary, or "helper", registers.The Accumulator alone would not be very useful if it were not for these "R"                registers. The "R" registers are also used to temporarily store values.

The "B" Register: 
           The "B" register is very similar to the Accumulator in the sense that it may hold an 8-bit (1-byte) value. 
           The "B" register is only used by two 8051 instructions: MUL AB and DIV AB. Thus, if you want to quickly and easily multiply or divide A by another number, you may                store the other number in "B" and make use of these two instructions. 
           Aside from the MUL and DIV instructions; The “B” register is often used as yet another temporary storage register much like a ninth "R" register.

The Data Pointer (DPTR):
            The Data Pointer (DPTR) is the 8051’s only user-accessible 16-bit (2-byte) register. The Accumulator, "R" registers, and "B" register are all 1-byte values. 
            DPTR, as the name suggests, is used to point to data. It is used by a number of commands which allow the 8051 to access external memory. When the 8051 accesses                   external memory; it will access external memory at the address indicated by DPTR. 
            While DPTR is most often used to point to data in external memory, many programmers often take advantage of the fact that it’s the only true 16-bit register                     available. It is often used to store 2-byte values which have nothing to do with memory locations.

The Program Counter (PC): 
            The Program Counter (PC) is a 2-byte address which tells the 8051 where the next instruction to execute is found in memory. When the 8051 is initialized PC always                starts at 0000h and is incremented each time an instruction is executed. It is important to note that PC isn’t always incremented by one. Since some instructions                require 2 or 3 bytes the PC will be incremented by 2 or 3 in these cases. 
             The Program Counter is special in that there is no way to directly modify it’s value. That is to say, you can’t do something like PC=2430h. On the other hand, if 
             you execute LJMP 2430h you’ve effectively accomplished the same thing. 
              It is also interesting to note that while you may change the value of PC (by executing a jump instruction, etc.) there is no way to read the value of PC.

The Stack Pointer (SP) 
              The Stack Pointer, like all registers except DPTR and PC, may hold an 8-bit (1-byte) value. The Stack Pointer is used to indicate where the next value to be                     removed from the stack should be taken from. 
              When you push a value onto the stack, the 8051 first increments the value of SP and then stores the value at the resulting memory location. 
              When you pop a value off the stack, the 8051 returns the value from the memory location indicated by SP and then decrements the value of SP. 
              This order of operation is important. When the 8051 is initialized SP will be initialized to 07h. If you immediately push a value onto the stack, the value will be               stored in Internal
              RAM address 08H. This makes sense taking into account what was mentioned two paragraphs above: First the 8051 will increment the value of SP (from 07h to 08h) and               then will store the pushed value at that memory address (08h). 
      SP is modified directly by the 8051 by six instructions: PUSH, POP, ACALL, LCALL, RET, and RETI. It is also used intrinsically whenever an interrupt is triggered.


2.06	Features Of 8051:

              •	It has internally 4K ROM.
              •	It has 128 Bytes on chip RAM.
              •	Two 16bit TIMER or COUNTER to count the internal or external pulses.
              •	One FULL DUPLEX UART (Universal Asynchronous Receiver Transmit) for SERIAL communication where TxD stands for TRANSMIT DATA and RxD received data.
              •	Four ON-CHIP I/O port (P0,P1,P2,P3),each are 8bitwise.So microcontroller have 32bit I/O lines, where P0,P2 are used for  address and data bus as well as I/O                     port.P1 port is used only as I/O port and P3 is used for various job purpose.
              •	INTERRUPTs: interrupts are six-two external, three internal and RESET is another interrupt.
              •	On chip bus controller which controls all the buses.
              •	On chip oscillator circuit.
              •	8bit CPU optimization for process control. It may be used as an ALU or data processing unit.
              •	On chip interrupt controller which have three internal interrupts and two external interrupt. From these five only one interrupts goes to CPU.
              •	The operating frequency 12MHZ.
              •	The maximum memory capacity of a 8051 microcontroller is 64KByte programming memory and 64Kbyte data memory.




2.07 8051 Buses & CPU Functioning In Data Transfer:


        Microcontroller buses:

               1.	DATA BUS-Instructions and data are transferred through this bus.
               2.	ADDRESS BUS-Used to point the memory or I/O locations that is to be read from or written to.
               3.	CONTROL BUS-controls the system that determine what kind of information is on the data bus and determines where the data will go,along with the address bus.

CPU controlled data transfers:
               •	CPU reads data/instructions from memory(memory read)
               •	CPU writes data to memory(memory write)
               •	CPU reads data from input device(I/O read)
               •	CPU writes data to  an output device(I/O write)















2.08  MICROCONTROLLER 89S52 DETAILS:

      2.08.1  BLOCK DIAGRAM: Please Access the word file attached for images
 

      
       2.08.2 IMPORTANT FEATURES:
                      •	It provides many functions (CPU, RAM, ROM, I/O, interrupt logic, timer, etc.) in a single package
                      •	8-bit ALU, Accumulator and Registers; hence it is an 8-bit microcontroller
                      •	8-bit data bus - It can access 8 bits of data in one operation
                      •	16-bit address bus - It can access 216 memory locations - 64 kiB (65536 locations) each of RAM and ROM
                      •	On-chip RAM - 128 bytes (data memory)
                      •	On-chip ROM - 4 KB (program memory)
                      •	Four byte bi-directional input/output port
                      •	UART (serial port)
                      •	Two 16-bit Counter/timers
                      •	Two-level interrupt priority
                      •	Power saving mode
2.08.3  PIN CONFIGURATION: Please access the world file for images

 
	
       2.08.4  PIN DESCRIPTION:

              	P1.0-P1.7(1 to 8): stands for PORT 1, used in simple I/O operation.
              	P0.0-P0.7(39 to 32): stands for PORT 0, used in simple I/O operation as well as ADDRESS and DATA bus multiplexing.
              	P2.0-P2.7(21 to 28):stands for PORT 2,used in I/O operation as well as higher order ADDRESS bus(A8-A15)
              	P3.0-P3.7(10-17): stands for PORT 3 used in I/O operation and other functions as follows:
              o	RxD(10): used for serial data reception. The data is serially received through this pin into SBUF register.
              o	TxD(11): used for serial data transmission. The data is serially transmitted through this pin from SBUF register.
              o	INT0 bar(12): External interrupt zero, active low signal. Interrupt zero comes through this pin into the microcontroller.
              o	INT1 bar(13): External interrupt one, active low signal. Interrupt one comes through this pin into the microcontroller.
              o	T0(14): Timer zero, external pulse comes through this pin.
              o	T1(15): Timer one, external pulse comes through this pin.
              o	WR’(16): when this signal goes low, MEMORY WRITE or I/O WRITE operation takes place.
              o	RD’(17): when this signal goes low, MEMORY READ or I/O READ operation takes place.
              	Vcc(40): this pin is connected with +5V DC
              	/EA/Vpp(31): external access: GND if programmed, is accessed externally.
              	ALE//PROG(30): Address Latch Enable (ALE) is used to demultiplex address    and data bus. At the time of EPROM programming, 50ms pulse is connected to       this                 pin.
              	/PSEN(29): Program Store Enable: distinguishes between programming memory and data memory. When signal goes LOW, programming ROM is activated.

2.09  8051 Interrupt:
              There are 5 interrupt sources for the 8051. Since the main RESET input can be also considered as an interrupt, there can be 6 interrupts listed.
              1. RESET: When the reset pin is activated, the 8051 jumps to the address location 0000H
              2. Two interrupts are set aside for the timers. One for timer 0 and another for timer
                  1. Memory locations 000BH and 001BH in the interrupt vector table belong to timer 0 and
                 timer 1 respectively
              3. Two interrupts are set aside for hardwire interrupts. Pin no 12(p3.2) and pin no. 13
                 (p3.3) in the port 3 are for the external hardwire interrupts INT0 and INT1 respectively.
                  This external interrupts are also referred as an EX1 and EX2.
              4. Serial communications has a single interrupt that belongs to both receive and
                   transmit.





                                            System RESET	RST	0000H

                                            External interrupt 0	IE0	0003H
                                            Timer/counter 0
	                                          TF0	000BH
                                            External interrupt 1	IE1	0013H
                                            Timer/counter 1	TF1	001BH
                                            Serial interrupt
                                            RI or TI	0023H

                                            2.08	2222
                                            2.10 ADDRESSING MODES:

 Each instruction requires certain data on which it has to operate. There are various techniques to specify data for instruction.
 These techniques are called addressing modes.8051 microcontroller uses the following addressing modes-
ADDRESSING MODES	DESCRIPTION	EXAMPLE
                  Immediate addressing	Operand (which immediately follows the instruction op. code) is the data value to be used.	
                                                        MOV A,#25h
                                     (25h are immediately stored into the accumulator)
                  Register addressing	One of the 8 general purpose registers,R0-R7,can be specified as the instruction operand. Register is generally referred as Rn.  	
                                                         MOV A,R0
                 (Copy the content of R0 into accumulator. If any data is previously stored in the accumulator, that will be deleted completely)
                 Direct addressing	Data value is directly obtained from the memory location specified in the operand.	MOV A,22h
                 (22h acts as an address and content of that particular address are copied into accumulator)
                 Indirect addressing	The address of the operand is specified by a register.
                                              It supports only R0 & R1.	MOV A,@R0
                     (The content of R0 acts as an address and the content of that particular address will be copied into the accumulator.)
                    Absolute addressing	Used only with AJMP (Absolute Jump) and ACALL(Absolute Call) instructions.	
                                                                 ACALL SADD (a11)
                                            (jump to short range address.the destination address will be within 2K.)
                  Long addressing	Used with instructions LJMP and CALL. It is full 16 bit address is specified in operand so that  the jump can be made to 
                  a location within 64Kbyte code memory space	LJMP 5000H
                  (After executing, it jumps to memory location 5000H.)


ADDRESSING MODES	DESCRIPTION	EXAMPLE
                      Indexed addressing	A separate register, either PC or DPTR, is used as base address and accumulator is used as an offset address.
                      Effective address= base address value + offset address value
                                                             MOVC A,@A+DPTR
(MOVC moves data from the external code memory space. Address operand= base address(DPTR) + index address(accumulator)
Relative addressing	Relative address is a 8-bit signed number (-128 to 127), which is added to PC to determine the address of the next instruction. Before addition, PC is incremented. Therefore the new address is relative to the next instruction and then jump to the new address instruction.	SJMP LABEL_X
(after executing, 
                                      new address= PC+ relative offset needed to reach LABEL_X)


2.11	 Types Of Instructions:

                                                   1.	ARITHMETIC INSTRUCTIONS
                                                   2.	LOGICAL INSTRUCTIONS
                                                   3.	DATA TRANSFER INSTRUCTIONS
                                                   4.	BIT-ORIENTED INSTRUCTIONS
                                                   5.	BRANCH INSTRUCTIONS

Arithmetic Operations
                     Mnemonic	Description	Bytes	Cycles
                                                  ADD A,Rn	       Add register to A	1	1
                                                  ADD A,direct	   Add direct byte to A	2	1
                                                  ADD A,@Ri	       Add indirect RAM to A	1	1
                                                  ADD A,#data	     Add immediate data to A	2	1
                                                  ADDC A,Rn	       Add register to A with Carry	1	1
                                                  ADDC A,direct	   Add direct byte to A with Carry	2	1
                                                  ADDC A,@Ri	     Add indirect RAM to A with Carry	1	1
                                                  ADDC A,#data	   Add immediate data to A with Carry	2	1
                                                  SUBB A,Rn	       Subtract register from A with Borrow	1	1
                                                  SUBB A,direct	Subtract direct byte from A with Borrow	2	1
                                                  SUBB A,@Ri	Subtract indirect RAM from A with Borrow	1	1
                                                  SUBB A,#data	Subtract immediate data from A with Borrow	2	1
                                                  INC A	Increment A	1	1
                                                  INC Rn	Increment register	1	1
                                                  INC direct	Increment direct byte	2	1
                                                  INC @Ri	Increment indirect RAM	1	1
                                                  DEC A	Decrement A	1	1
                                                  DEC Rn	Decrement register	1	1
                                                  DEC direct	Decrement direct byte	2	1
                                                  DEC @Ri	Decrement indirect RAM	1	1
                                                  INC DPTR	Increment Data Pointer	1	2
                                                  MUL AB	Multiply A and B (A x B => BA)	1	4
                                                  DIV AB	Divide A by B (A/B => A + B)	1	4
                                                  DAA	Decimal Adjust A	1	1


Logical Operations
                Mnemonic	Description	Bytes	Cycles
                                                 ANL A,Rn	AND register to A	1	1
                                                 ANL A,direct	AND direct byte to A	2	1
                                                 ANL A,@Ri	AND indirect RAM to A	1	1
                                                 ANL A,#data	AND immediate data to A	2	1
                                                 ANL direct,A	AND A to direct byte	2	1
                                                 ANL direct,#data	AND immediate data to direct byte	3	2
                                                 ORL A,Rn	OR register to A	1	1
                                                 ORL A,direct	OR direct byte to A	2	1
                                                 ORL A,@Ri	OR indirect RAM to A	1	1
                                                 ORL A,#data	OR immediate data to A	2	1
                                                 ORL direct,A	OR A to direct byte	2	1
                                                 ORL direct,#data	OR immediate data to direct byte	3	2
                                                 XRL A,Rn	Exclusive-OR register to A	1	1
                                                 XRL A,direct	Exclusive-OR direct byte to A	2	1
                                                 XRL A,@Ri	Exclusive-OR indirect RAM to A	1	1
                                                 XRL A,#data	Exclusive-OR immediate data to A	2	1
                                                 XRL direct A	Exclusive-OR A to direct byte	2	1
                                                 XRL direct,#data	Exclusive-OR immediate data to direct byte	3	2
                                                 CLR A	Clear A	1	1
                                                 CPL A	Complement A	1	1
                                                 RL A	Rotate A Left	1	1
                                                 RLC A	Rotate A Left through Carry	1	1
                                                 RR A	Rotate A Right	1	1
                                                 RRC A	Rotate A Right through Carry	1	1
                                                 SWAP A	Swap nibbles within A	1	1



Data Transfer Operations
                  Mnemonic	Description	Bytes	Cycles
                                               MOV A,Rn	Move register to A	1	1
                                               MOV A,direct	Move direct byte to A	2	1
                                               MOV A,@Ri	Move indirect RAM to A	1	1
                                               MOV A,#data	Move immediate data to A	2	1
                                               MOV Rn,A	Move A to register	1	1
                                               MOV Rn,direct	Move direct byte to register	2	2
                                               MOV Rn,#data	Move immediate data to register	2	1
                                               MOV direct,A	Move A to direct byte	2	1
                                               MOV direct,Rn	Move register to direct byte	2	2
                                               MOV direct,direct	Move direct byte to direct byte	3	2
                                               MOV direct,@Ri	Move indirect RAM to direct byte	2	2
                                               MOV direct,#data	Move immediate data to direct byte	3	2
                                               MOV @Ri,A	Move A to indirect RAM	1	1
                                               MOV @Ri,direct	Move direct byte to indirect RAM	2	2
                                               MOV @Ri,#data	Move immediate data to indirect RAM	2	1
                                               MOV DPTR,#data16	Load Data Pointer with 16-bit constant	3	1
                                               MOVC A,@A+DPTR	Move Code byte relative to DPTR to A	1	2
                                               MOVC A,@A+PC	Move Code byte relative to PC to A	1	2
                                               MOVX A,@Ri	Move External RAM (8-bit addr) to A	1	2
                                               MOVX A,@DPTR	Move External RAM (16-bit addr) to A	1	2
                                               MOVX @Ri,A	Move A to External RAM (8-bit addr)	1	2
                                               MOVX @DPTR	A Move A to External RAM (16-bit addr)	1	2
                                               PUSH direct	Push direct byte onto stack	2	2
                                               POP direct	Pop direct byte from stack	2	2
                                               XCH A,Rn	Exchange register with A	1	1
                                               XCH A,direct	Exchange direct byte with A	2	1
                                               XCH A,@Ri	Exchange indirect RAM with A	1	1
                                               XCHD A,@Ri	Exchange low-order Digit indirect RAM with A	1	1




Single Bit (Boolean Variable) Operations
                    Mnemonic	Description	Bytes	Cycles
                                              CLR C	Clear Carry flag	1	1
                                              CLR bit	Clear direct bit	2	1
                                              SETB C	Set Carry flag	1	1
                                              SETB bit	Set direct bit	2	1
                                              CPL C	Complement Carry flag	1	1
                                              CPL bit	Complement direct bit	2	1
                                              ANL C,bit	AND direct bit to Carry flag	2	2
                                              ANL C,/bit	AND complement of direct bit to Carry flag	2	2
                                              ORL C,bit	OR direct bit to Carry flag	2	2
                                              ORL C,/bit	OR complement of direct bit to Carry flag	2	2
                                              MOV C,bit	Move direct bit to Carry flag	2	1
                                              MOV bit,C	Move Carry flag to direct bit	2	2





Program Flow Control
                     Mnemonic	Description	Bytes	Cycles
                                              ACALL addr11	Absolute subroutine call	2	2
                                              LCALL addr16	Long subroutine call	3	2
                                              RET	Return from subroutine	1	2
                                              RETI	Return from interrupt	1	2
                                              AJMP addr11	Absolute Jump	2	2
                                              LJMP addr16	Long Jump	3	2
                                                 
