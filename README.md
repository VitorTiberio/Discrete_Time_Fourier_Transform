# Discrete Time Fourier Transfomr - DTFT # 

To initialize our analysis, we need to define a intermediary function, to help us to get the DTFT. 

When we are talking about g[n], the value in intervals of n is equal to zero, while the value in n is different zero. 

So, to define this function, we are going to use a fabulous function: the delta/ impulse function! Suppose we have a impulse funciton like this: 

$$\delta(t - nT_s)$$

The values of equation above is zero for every time (t) other than nTs. So g[n] comes very close to $g_d(t)$. 

Now, we're going to define $g_d(t)$:

$$
g_d(t) = g(t) \cdot \text{imt}(t), \quad \text{where} \quad \text{imt}(t) = \sum_{n=-\infty}^{\infty} \delta(t - nT_s)
$$

So, 

$$
g_d(t) = g(t) \cdot \sum_{n=-\infty}^{\infty} \delta(t - nT_s)
$$

Now, we have a function who comes very close to g[n]. One important observation is: g[n] is a discrete function and %g_d(t)% is a continuous function. 
