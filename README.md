# analog kickdrum circuit
an analog kickdrum circuit designed for the *electronics workshop 2* course at iiit hyderabad.  

## features
- **trigger** - gate-to-pulse conversion using tl081
- **pitch** - voltage-controlled oscillator (60-120hz range) with pitch envelope
- **decay** - adjustable sustain via feedback control
- **tone** - variable low-pass filter (23-234hz cutoff)
- **distortion** - diode clipping stage with smoothing control
- **output** - lm386 amplifier for 4ohm speaker

## hardware
**core components:**
- tl081 op-amp (trigger/comparator)
- 2n3904 npn transistor (vco)
- 1n4148 diodes (clipping/protection)
- 220nf capacitor + 100k resistor (envelope generator)
- 10k and 100k potentiometers (pitch/decay/tone controls)

**power:**
- ±12v dual power supply

**output stage:**
- ua741 attenuation stage
- lm386 audio amplifier

## setup instructions
1. connect +12v, -12v and gnd to power rails
2. input: 5v gate signal (1hz square wave recommended)
3. output: connect to lm386 amplifier driving 4ohm speaker

## controls
| control | function |
|---------|----------|
| pitch | adjusts base frequency via rc timing |
| decay | controls sustain length through feedback gain |
| tone | sets high-frequency cutoff (1k-10k range) |
| distortion | adjusts clipping intensity via diode bypass |

## troubleshooting
- **missed triggers**: adjust comparator threshold resistors
- **signal too hot**: ua741 attenuation stage (gain = 1/13) helps match lm386 input levels
- **noise issues**: add 100nf decoupling caps and minimize wire lengths

## project files
- `/simulations` - ltspice simulation files
- `/hardware` - breadboard implementation photos
- `/datasheets` - datasheets of the ics used
- `/documents` - relevant theory and full report 

## contributors
  priyanshi jain  
  sudhanva joshi  
  
for details, see [project-report.pdf](documents/project-report.pdf).

---
*note: this circuit is inspired by similar synth and kick circuits by moritz klein*

