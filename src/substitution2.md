# substitution2 - PicoCTF 2022 (crypto)
### Description
It seems that another encrypted message has been intercepted. The encryptor seems to have learned their lesson though and now there isn't any punctuation! Can you still crack the cipher?Download the message [here](https://artifacts.picoctf.net/c/112/message.txt).
### Hints
Try refining your frequency attack, maybe analyzing groups of letters would improve your results?

<details>
<summary>Solution</summary>

You would usually solve something like this using statistical analysis for letters and groups of letters. 
Knowing that the text is English we can assume that the most common letter is also the most common letter in English text.
Same goes for groups of letters. This would also be easier if we had spaces and punctuation.
If you promise you understand all that I'll let you use [quipqiup](https://quipqiup.com/) so it can do all that for you. (select statistics in the drop down)

Final flag: `picoCTF{N6R4M_4N41Y515_15_73D10U5_8E1BF808}`
</details>
