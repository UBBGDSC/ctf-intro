# unpackme.py - PicoCTF 2022 (rev)

### Description

Can you get the flag?Reverse engineer this [Python program](https://artifacts.picoctf.net/c/50/unpackme.flag.py).

<details>
<summary>Solution</summary>

Replace the call to `exec` with `print`. When run the program will output the unpacked  code containing the flag.

Final flag: `picoCTF{175_chr157m45_85f5d0ac}`
</details>

