# Huffman-Shannon_fano
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.
# Aim:
To apply the Huffman and Shannon-Fano source with symbols and statistics {0.125,
 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output.
# Tools Required:
Python IDE with Numpy and Scipy.
# Program:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# calculations:
![Screenshot 2025-03-30 195512](https://github.com/user-attachments/assets/3c3a0db4-fb4c-4287-bd67-464540be472c)
![Screenshot 2025-03-30 195604](https://github.com/user-attachments/assets/4234797d-3b7e-4f33-93fd-cd8951e20510)
![Screenshot 2025-03-30 195640](https://github.com/user-attachments/assets/1bbb3a6d-6c52-4477-a69a-cb51139db4b4)
![Screenshot 2025-03-30 200009](https://github.com/user-attachments/assets/7b5d75e0-6df7-4c88-a2ce-708082e378b2)
# Results:
The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625,
 0.125, 0.125, 0.25} using python are verified.


