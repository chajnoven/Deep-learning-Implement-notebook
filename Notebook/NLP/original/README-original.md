# LSTM
---
For example:

![image-20191211103148384](imgs/image-20191211103148384.png)

## Step1

The output of the **Learn Gate** is $N_{t} i_{t}$ here:
$$
\begin{aligned} 
N_{t}&=\tanh \left(W_{n}\left[S T M_{t-1}, E_{t}\right]+b_{n}\right) \\
i_{t}&=\sigma\left(W_{i}\left[S T M_{t-1}, E_{t}\right]+b_{i}\right)\\ 
\end{aligned}
$$

$$
\text{Equation }1
$$

Description:
$$
\begin{aligned} 
&STM_{t-1} \rightarrow tanh  \rightarrow N_{t}=\tanh \left(W_{n}\left[S T M_{t-1}, E_{t}\right]+b_{n}\right) \rightarrow[*] \rightarrow N_{t} \cdot i_{t}\\
&[*]\rightarrow i_{t}=\sigma\left(W_{i}\left[S T M_{t-1}, E_{t}\right]+b_{i}\right)\\
&\sigma\rightarrow ignore(sigmoid)
\end{aligned}
$$

## Step2

The output of the **Forget Gate** is $L T M_{t-1} f_{t}$ where:
$$
\begin{aligned} 
&f_{t}=\sigma\left(W_{f}\left[S T M_{t-1}, E_{t}\right]+b_{f}\right)\\
&LTM_{t-1} \rightarrow [*]\rightarrow LTM_{t-1}\cdot f_t\\
&[*] \rightarrow f_t
\end{aligned}
$$
$$
\text { Equation } 2
$$

## Step3

**Remember Gate**
$$
\begin{align}
LTM_t&=Forget\;Gate\ + Learn\;Gate\\
&=LTM_{t-1}*f_t\ + N_t*i_t
\end{align}
$$

$$
\text { Equation } 3
$$



## Step4

**Use Gate**

The output of the Use Gate is $U_{t} V_{t}$ where:
$$
\begin{aligned} U_{t} &=\tanh \left(W_{u} L T M_{t-1} f_{t}+b_{u}\right) \\ V_{t} &=\sigma\left(W_{v}\left[S T M_{t-1}, E_{t}\right]+b_{v}\right)\\
S T M_{t}&=U_{t} \cdot V_{t}
\end{aligned}
$$

$$
\text { Equation } 4
$$

## Finally

![image-20191211113032257](imgs/image-20191211113032257.png)

## Reference

[Links](https://classroom.udacity.com/nanodegrees/nd188-bert/parts/a58738e5-e865-4f64-82e9-cbe7a41b272e/modules/67b445a1-38bc-4128-9d8b-58129e849573/lessons/a8fc0724-37ed-40d9-a226-57175b8bb8cc/concepts/f9f95dcb-bb0e-43d3-841c-9277c54207cb)

