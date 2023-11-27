# Pixelated - PicoCTF 2021 (crypto)
### Description
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled2.png)

### Hints
[https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
Think of different ways you can "stack" images

<details>
<summary>Solution</summary>

Use python PIL
If you play around with different operation for each pail of pixels you’ll notice that a lot of them turn white when using xor.
Make the non white ones obvious.

Code:
```
from PIL import Image

image1 = Image.open("scrambled1.png")
image2 = Image.open("scrambled2.png")
output = Image.new("RGB", size=image1.size)

data = []

for pixel1, pixel2 in zip(image1.getdata(), image2.getdata()):
    data.append((pixel1[0] ^ pixel2[0], pixel1[1] ^ pixel2[1], pixel1[2] ^ pixel2[2]))
    if data[-1] != (255, 255, 255):
        data[-1] = (0, 0, 0)

output.putdata(data)

output.save("output.png")

```

Final flag: `picoCTF{2a4d45c7}`
</details>
