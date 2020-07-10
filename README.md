# Jetson-Nano_RE - Reading EEPROM on the Jetson Nano 

### Note : This is an attempt on using a EEPROM Programmer to Read Flash Memory from the Jetson Nano.

### This is NOT the BIOS of Jetson Nano as "ARM processors do not typically have a BIOS. Jetson Nano uses the C-Boot bootloader " [See here](https://forums.developer.nvidia.com/t/bios/73787) 

So what does this data contain ? I do not know that either. 

#### Jetson Nano Developer Board and Jetson Nano Module   :
<p>
<img src="https://github.com/aswinkumar1999/Jetson-Nano_RE/blob/master/images/IMG_20200710_161456.jpg" width="600" height="460" />
<img src="https://github.com/aswinkumar1999/Jetson-Nano_RE/blob/master/images/IMG_20200710_160747.jpg" width="345" height="460" />
<p/>

#### The EEPROM to Read Data from ( [W25X40](https://www.winbond.com/resource-files/w25x40cl_f%2020140325.pdf)  ): 

Flash Size : 4 M-Bit / 512 Kb 
<p>
<img src="https://github.com/aswinkumar1999/Jetson-Nano_RE/blob/master/images/IMG_20200710_154226.jpg" width="345" height="460" />
<img src="https://github.com/aswinkumar1999/Jetson-Nano_RE/blob/master/images/IMG_20200710_161010.jpg" width="345" height="460" />
<p/>

#### Reading EEPROM Memory 

```bash
# Read Flash Memory ( SPI ) and dump it to new.bin
sudo flashrom --programmer ch341a_spi -r new.bin
```

<p>
<img src="https://github.com/aswinkumar1999/Jetson-Nano_RE/blob/master/images/IMG_20200710_161550.jpg" width="600" height="460" />
<img src="https://github.com/aswinkumar1999/Jetson-Nano_RE/blob/master/images/IMG_20200710_160946.jpg" width="345" height="460" />
<p/>

#### Output 

``` bash 
$ strings new.bin
''''D
}2|c
}2|c
}2|c
}2|c
}2|c
=d	E<p
Mp:1
Mp&1
Mp^1
t]%=
Mps1
tm%=
7l%C
Mpu1
Mpb1
Zd@pW
@oP/
} |_
`%}*|c
}*|c"
VCp9
pSu[
yZ"u
yU"t
dUp@
=E<`
E>p!
E>p.
=E<p
=E<p
=E<p
E=p"
=E<`
=E<`
`	$@p
$@p	
=d	E<p
Du@)
t	%=
tc%=
E<p#
E<p.
E<"t
"QF1
p	QV
QE{ } 
avq}
avq}
5q}EB`
0q}EB`
q}EB`
q}EB`
*PE{
CEBp
CEB`N
`;$1
E<p2
Gd`	
CEBp
}`|2
}m|0
u]_u^ 
u]]u^
u][u^
}*|c
^d E]p
^d0E]p
}`|2
}m|0
u]_u^ 
u]]u^
u][u^
}*|c
^d E]p
^d0E]p
"T0u]
^E]"
},|q
Z+PZ
d pw
d pF
d p*
Q+PXQ"
1E0`
6P+{
qWpJ
qWpJ
qWpJ
qWpJ
0d@pT
2E1p
2E1p
5@qc
@d@E@p
EEDp
EED`1
E^P5
E^P<
G"%=
?E>"{
E=p5
=E<`
=E<`
=E<`
=E>`	
?E>p
wzP=
IEHp
IEH` 
wzP;
IEHp
IEH`
201811071711
Generic
USB3.0 Hub
201811071711
?E>`
p#1	
=E<`
1Z@	
?E>`
?E>p
G_\j{
B0'|M
.H"|
;"OG
```
