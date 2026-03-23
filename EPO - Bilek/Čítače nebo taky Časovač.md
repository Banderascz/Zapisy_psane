
|   **Čítač**    |        **Časovač**        |
| :------------: | :-----------------------: |
| externí signál | interní signál, oscilátor |

---
## Potřebuji každou 1 ms přetečení č/čo

$$
f přet. = 1/10^-3 = 1000 Hz
$$
$$
f osc. = 16 MHz = 16 000 000Hz
$$
---
[[Epo časovače=čítače.xopp]]
č/čo, č/č^2
reg(č/č) = <0, 2^8>
		<0, 2^16>
záporné hodnoty nelze dát do registeru
$$
reg_č = 2^8 - f osc./předdělič/fpř.
$$
$$
reg = 256 - 16*10^6/8/10^3
$$
$$
reg = -1744 //8
$$
$$
= -774 //16
$$
$$= 6 //64 (toto| je|pro|pintlich)
$$$$= 193,5//256$$
$$=240,375 //1024$$
