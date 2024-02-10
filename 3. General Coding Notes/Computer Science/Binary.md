All data in a computer is stored in **Binary**, which can be either a 0 or a 1. These are called **bits**. 

- A **byte** is a collection of bits, usually 8 bits long. A byte can represent **256 different values**.
- Code is interpreted, or compiled, into a binary format.
- It is much easier to represent data in a [[Transistor]] with binary than it is with any other system of counting.
---
# Logic
**Base 10** uses ten different symbols. When you get to the number 10, you add an extra digit. Then another for 100, and so on. This is called **positional notation**, where each position represents a value 10x greater than the position on its right.

| 100x | 10x | 1x |
| ---- | ---- | ---- |
| 1 | 3 | 8 |

**Binary** has the same logic, but ==the position on the left is 2x greater== than the one on the right. It is read from right to left. You can think of each binary digit representing a single number, and adding them together gives you the sum.

| 1 | 1 | 0 | *Sum* |
| ---- | ---- | ---- | ---- |
| 4 | 2 | 1 | *6* |

Because binary is **hard to read**, it is often converted to a **hexadecimal** format, which is a **base-16** numbering system. It uses the symbols **0-9, A-F**. Each hexadecimal digit can represent **4 bits**. This is called a **nybble**. You can take a **hex dump** (lmao) to analyse the raw data of a file, which is easier to comprehend.

| D | E | C |
| ---- | ---- | ---- |
| 1101 | 1110 | 1100 |
## How Data Works
Any technique that can turn data into numbers can convert those numbers to bits. This is how a computer stores data. This is a good example of #abstraction, and it is the most fundamental abstraction in Computer Science. Each layer builds new things out of the pieces that the previous layer provides.

*Bits -> Numbers -> Colours -> Images -> Videos*

A computer needs to keep track of what the data represents, because one string of bits could represent text, but that exact same string of bits could also be intended to represent an image. This is what a **file extensions** are for. A .jpg interprets bits in a particular way and .mp3s are interpreted in another way, however it is possible for a .jpg and .mp3 to have identical bits in the files. **Firmware** is the basic set of instructions that a computer uses to interpret data, which informs other more abstract systems of interpretation, and so on.

Audio is changes in air pressure, so audio data represents how much the air should change in pressure to produce a certain sound. 3D models are collections of triangles, so store a list of sets of 3 numbers to represent each point. Then, store a list of numbers to represent which points to connect to make each triangle. 

Computers use electricity, which has voltage. Voltage is like water pressure. Commonly, a 0 bit represents 0 volts, and a 1 bit represents 5 volts. This is how a circuit works: when it receives 5 volts, it represents the value of 1. This is also how electromagnetic interference works: something like a solar flare can destroy digital data by scrambling the data stored in these circuits by flipping them on and off by to it voltages that it should not have. It is also how interference happens in wifi signals, radio, etc.

---
# Tangential Cool Info
## History
It first appeared in ancient Egypt with Horus Eye fractions, and was used in many other cultures, such as the I Ching in China. It is also the basis for morse code. The Eniac (1945) was programmed by manually flicking switches, and then punch cards, which represented binary values. Today, microchips use [[Boolean Algebra]] to combine logic gates to execute binary code billions of times a second.

8-bit games are called that because they can work with 8 bits at once (0-255, one byte).
## Colours
The visible spectrum of colours consists of an infinite number of primary colours which can be combined in any way you want. However, the human eye can only see three groups of colours: reddish, greenish, and blueish. The combination of these senses lets us perceive a colour. 

You can trick the sensors in your eye into seeing a colour by shining colours lights, which combine, from your perspective, to be a new colour, but in reality they are not that colour. A red spotlight + a green one appears to emit yellow light. There a colours that a screen can't represent. 

Pictures are grids of colours, with each pixel representing a colour. Combine the pixels and you have an image. Videos are sequences of images, images are sequences of colours, colours are sequences of numbers, and numbers are sequences of bits. Therefore, videos on a computer are just very long sequences of bits. A 1080p, 15m video is about 10 trillion bits.
### Compression Algorithms
The goal is to represent the data with as little data as possible. The Youtube compression algorithm is particularly bad at representing confetti.

When an object moves across the screen, a compression algorithm can detect which parts of a video's image is moving and which parts are not. It can then save space when rendering a video by keeping the stationary bits of the image static, as in, not change the bits, and only change the bits for the moving section of the video's image.

---
**Links:**
[How Binary Works, and the Power of Abstraction](https://www.youtube.com/watch?v=PMpNhbMjDj0)
[Binary Explained in 01100100 Seconds](https://www.youtube.com/watch?v=zDNaUi2cjv4)