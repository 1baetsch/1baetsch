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

Use the checkerboard or some form of mapping to convert the characters of your plain text message into digits first.
A most basic method is to assign a two-digit value to each letter (eg. A=01, B=02 and so on through Z=26).

![CT-37](https://airvpn.org/uploads/monthly_08_2015/post-158612-0-10453100-1439821943.png)

But this CT-37 offers ways to also integrate digits and other symbols.
TODO: further explain how to use the CT-37

"To convert numbers, always use "FIG" before and after one or more digits. Each digit is written out three times to exclude errors. You can use spaces and punctuations within the "FIG" mode. An example: "1.5 KG" = "90 111 91 555 90 77 74". The "REQ" or "REQUEST" field enables questions and spaces are created with the "SPC" field. The apostrophe (93) can be used as both apostrophe and comma. The "CODE" field is the codebook prefix and is used before each codebook value. The use of spaces before and after codebook words is not necessary."

When using CT-37 table for conversion, we see how our example text "hello world" will look like in digits:

Plain text:     
hello world     
converted:    
7527878594865837872    

## 3. Encryption

TODO: write full text

* first write down id of one time pad (first 5 digit group)
* then split mapped plain text into 5 digit groups (and fill with e.g. "0"s)
   * 75278 78594 86583 7872+0
* then use the generated one time pad and substract the first one time pad 5 digit group (not the ID one) from the first 5 digit group we just created; this is done digit by digit and with modulo?!

* e.g. lets assume we have these 4 groups in our generated one time pad:       
   12345 44444 33222 10024     
   ->     
   75278 78594 86583 78720     
  -12345 44444 33222 10024     
  =     
   63933 34150 53361 68706     
   
* receiver has to have the CT-37 table and the same one time pad and has to add the 5 digit groups and apply modulo 10



