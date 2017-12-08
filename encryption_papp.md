# Encryption pApp - generate One Time Pads
shortened version of this [example](https://airvpn.org/topic/14999-how-to-one-time-pads-perfect-encryption/)

## What we need:
  * 2x ten-sided dice
  * 2x mapping of symbols to digit combinations/numbers = checkerboard [CT-37](https://airvpn.org/topic/14999-how-to-one-time-pads-perfect-encryption/#)
  * 2x pieces of paper
  * 2 people, who want to securely communicate, with some patience and basic math skills
  
## 1. Generate One Time Pads

![](https://airvpn.org/index.php?app=core&module=attach&section=attach&attach_rel_module=post&attach_id=15882)

First we create unique keys using ten-sided dice for our one-time pad. 
A common one-time pad contains 50 groups of 5 random digits, which is sufficient for the length of one "normal" message, and each one-time pad sheet should have a unique first group of five digits.
To generate each of the 50 groups roll a ten-sided dice 5 times and append each resulting digit to form the 5 digit blocks.
If you think your message will not be that long you can also generate less than 50 groups. Plus you have 2 ten-sided dices, so you can also generate those groups in parallel to speed up the generation.

If you are done, make sure to create a copy of this one time pad, so that each one has a copy of this.
Remember: Only use this one time pad once, and destroy it after using.


## 2. Prepare you plain text message for encryption

Use the checkerboard or some form of mapping to convert the characters into digits first.

