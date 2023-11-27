# keygenme-py
### Description
[keygenme-trial.py](https://mercury.picoctf.net/static/9cc50abd5b012891d5a1132e05f15a07/keygenme-trial.py)

<details>
<summary>Solution</summary>

Looking at the source we see a function called check_key. It does a bunch of checks to see if our input is a valid key.
Thankfully we have all the info necessary to recreate it, instead of comparing we can just print the correct value.
I just copy-pasted the original code and deleted some of the unnecessary parts.

Code:
```
import hashlib
from cryptography.fernet import Fernet
import base64



# GLOBALS --v
arcane_loop_trial = True
jump_into_full = False
full_version_code = ""

username_trial = "SCHOFIELD"
bUsername_trial = b"SCHOFIELD"

key_part_static1_trial = "picoCTF{1n_7h3_|<3y_of_"
key_part_dynamic1_trial = "xxxxxxxx"
key_part_static2_trial = "}"
key_full_template_trial = key_part_static1_trial + key_part_dynamic1_trial + key_part_static2_trial


def get_key(username_trial):

        key = key_part_static1_trial


        key = key + hashlib.sha256(username_trial).hexdigest()[4]
        key = key + hashlib.sha256(username_trial).hexdigest()[5]
        key = key + hashlib.sha256(username_trial).hexdigest()[3]
        key = key + hashlib.sha256(username_trial).hexdigest()[6]
        key = key + hashlib.sha256(username_trial).hexdigest()[2]
        key = key + hashlib.sha256(username_trial).hexdigest()[7]
        key = key + hashlib.sha256(username_trial).hexdigest()[1]
        key = key + hashlib.sha256(username_trial).hexdigest()[8]

        key += key_part_static2_trial

        print(key)

get_key(bUsername_trial)
```

Final flag: `picoCTF{1n_7h3_|<3y_of_e584b363}`
</details>
