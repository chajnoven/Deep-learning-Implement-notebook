# NLP
---
## Content

- [RNN](#rnn)

- [LSTM](#lstm)
    - [LSTM ipyb](https://github.com/udacity/deep-learning-v2-pytorch/blob/master/recurrent-neural-networks/char-rnn/Character_Level_RNN_Solution.ipynb)



## RNN

![image-20191213193647166](imgs/image-20191213193647166.png)

For Pictures, In NLP, It needs to consider to the length.

reference
[udacity](https://github.com/udacity/deep-learning-v2-pytorch/blob/master/recurrent-neural-networks/char-rnn/Character_Level_RNN_Solution.ipynb)

## LSTM

---
For example:

![image-20191211103148384](imgs/image-20191211103148384.png)

### Step1

The output of the **Learn Gate** is ![image-20191211115822313](imgs/image-20191211115822313.png) here:

![image-20191211115920070](imgs/image-20191211115920070.png)

Description:

![image-20191211115934456](imgs/image-20191211115934456.png)

### Step2

The output of the **Forget Gate** is ![image-20191211120002116](imgs/image-20191211120002116.png) where:

![image-20191211120024952](imgs/image-20191211120024952.png)

### Step3

**Remember Gate**

![image-20191211120045139](imgs/image-20191211120045139.png)

### Step4

**Use Gate**

The output of the Use Gate is ![image-20191211120122026](imgs/image-20191211120122026.png) where:

![image-20191211120143130](imgs/image-20191211120143130.png)

### Finally

![image-20191211113032257](imgs/image-20191211113032257.png)

### Reference

[Links](https://classroom.udacity.com/nanodegrees/nd188-bert/parts/a58738e5-e865-4f64-82e9-cbe7a41b272e/modules/67b445a1-38bc-4128-9d8b-58129e849573/lessons/a8fc0724-37ed-40d9-a226-57175b8bb8cc/concepts/f9f95dcb-bb0e-43d3-841c-9277c54207cb)



### Warning

Because github doesn't support latex, so I have made a original, which is latex math.

[reference](https://github.com/udacity/deep-learning-v2-pytorch/tree/master/recurrent-neural-networks/char-rnn)
[original](https://github.com/chajnoven/Deep-learning-Implement-notebook/blob/master/Notebook/NLP/original/README-original.md)


