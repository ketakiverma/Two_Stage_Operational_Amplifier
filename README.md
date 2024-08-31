# two_stage_op_amp
Design and analysis of 2-stage op-amp

Concept:
A two-stage operational amplifier (op-amp) is a type of electronic amplifier circuit that consists of two separate amplifier stages connected in series. The primary purpose of using two stages in an op-amp is to achieve higher levels of gain, bandwidth, and other performance characteristics compared to a single-stage op-amp design.

The two stages typically found in a two-stage op-amp are the differential amplifier stage and the output amplifier stage. Let's go through each of these stages and their functions:

1. **Differential Amplifier Stage:**
   The first stage of a two-stage op-amp is the differential amplifier stage. Its primary function is to amplify the voltage difference between its two input terminals while rejecting common-mode signals (signals that are present on both inputs in-phase). The differential amplifier is responsible for the high gain and high common-mode rejection ratio (CMRR) of the op-amp.

   The differential amplifier usually consists of transistors (bipolar or MOSFET) arranged in a specific configuration. The most common configuration is the long-tailed pair, where two transistors share a common emitter/source resistor and have their collectors/drains connected to form a differential pair.

   The output of the differential amplifier stage is a voltage that represents the amplified difference between the two input voltages. This voltage is then fed into the second stage for further amplification.

2. **Output Amplifier Stage:**
   The second stage of the op-amp is the output amplifier stage. This stage takes the differential signal from the first stage and further amplifies it to achieve the desired overall gain. The output amplifier stage also provides the necessary current drive to the output load.

   The output amplifier stage can be designed using various configurations, such as common-emitter for bipolar transistors or common-source for MOSFETs. This stage provides the final amplification and buffering required to deliver the output voltage swing with the desired gain.

In a two-stage op-amp, the overall gain of the op-amp is the product of the gains of both stages. The first stage provides a relatively high gain to amplify the small differential input voltage, while the second stage provides additional gain and output drive capability.

Key advantages of a two-stage op-amp include improved gain-bandwidth product, increased linearity, better noise performance, and enhanced CMRR. However, two-stage op-amps are generally more complex to design and may require careful consideration of stability, compensation, and biasing.


Design Specification:

• Av=2000; GBW = 15MHz; CL = 10pF; ICMR = 0.8-1.6V;
Slew Rate = 10V/µs
• MOSFET length of 180nm is assumed.
• A bias current of 40µA is assumed.
• A voltage supply of 1.8V is used.

Tools Used: LTspice IV

FORMULAE
1. Id =(1/2)*µCox(W/L)[|Vgs|-|Vth|]^2(In active mode)
2. Ad = −gm(ron || rop)
3. ro =1/(λ*Idsat)
4. gm =squareroot(2µCox(W/L)Idsat)
5. f3−dB =1/(2*pi*ro*CL)
W/L ratios kept in the circuit below are kept by following certain design
procedure and those values are
• S1=S2=7.84
• S3=S4=4.311
• S5=5.75
• S6 = 147.1
• S7 = 49.96
• S8 = 9.58
where,
• Id = drain current
•1/2 µnCox = process transconductance parameter
• Vth = threshold voltage
• Vgs = gate to source voltage
• λ = channel length modulation parameter
• gm = transconductance
• Ad = Voltage gain
• ro = output resistance
• f3−dB = 3-dB frequency
