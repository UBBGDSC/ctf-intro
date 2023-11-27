# Insp3ct0r - PicoCTF 2019 (web)

### Description
Kishor Balan tipped us off that the following code may need inspection: https://jupiter.challenges.picoctf.org/problem/41511/ (link) or http://jupiter.challenges.picoctf.org:41511
### Hints
How do you inspect web code on a browser?
There's 3 parts

<details>
<summary>Solution</summary>
Use inspect element, or view source to look in the source code of the page. We see a part of the flag as a comment
We can then do the same with `mycss.css` and `myjs.js` to get the other parts.
Final flag: `picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?832b0699}`
</details>

