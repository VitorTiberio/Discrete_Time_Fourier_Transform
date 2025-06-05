# Discrete Time Fourier Transform - DTFT # 

## Remembering the Fourier Transform ## 

To define the DTFT, we need to remember the definition of F.T. To transform a signal in time domain to a frequency domain, we use the expression below: 

$$
G(f) = \int_{-\infty}^{+\infty} g(t) \cdot e^{-i 2 \pi f t} \, dt \quad (1)
$$

## Defining an auxiliary function $g_d(t)$ that comes very close to g[n] ##

To initialize our analysis, we need to define an intermediary function, to help us to get the DTFT. 

When we are talking about g[n], the value in intervals of n is equal to zero, while the value in n is different zero. 

So, to define this function, we are going to use a fabulous function: the delta/ impulse function! Suppose we have a impulse funciton like this: 

$$\delta(t - nT_s)$$

The values of equation above is zero for every time (t) other than nTs. So g[n] comes very close to $g_d(t)$. 

Now, we're going to define $g_d(t)$:

$$
g_d(t) = g(t) \cdot \text{imt}(t), \quad \text{where} \quad \text{imt}(t) = \sum_{n=-\infty}^{\infty} \delta(t - nT_s) \quad (2)
$$

So, 

$$
g_d(t) = g(t) \cdot \sum_{n=-\infty}^{\infty} \delta(t - nT_s) \quad (3)
$$

Now, we have a function who comes very close to g[n]. One important observation is: g[n] is a discrete function and $g_d(t)$ is a continuous function. 

## Applying the Fourier Transform in $g_d(t)$ ## 

In this topic, we will apply the Fourier Transform (1) in definition (3). At this point, we can proceed in two different ways:

1) Apply the Fourier Transform to the expression (3);
2) Use the property that multiplication in the time domain corresponds to convolution in the frequency domain.

We will start with the first one. So, applying the fourier transform in equation (3) we have:

$$
G_d(f) = \int_{-\infty}^{+\infty} \left[ g(t) \cdot \sum_{n=-\infty}^{\infty} \delta(t - nT_s) \right] \cdot e^{-i 2 \pi f t} \, dt
$$

Swapping the sum with integral, we have: 

$$
G_d(f) = \sum_{n=-\infty}^{\infty} \int_{-\infty}^{+\infty} g(t) \cdot \delta(t - nT_s) \cdot e^{-i 2 \pi f t} \, dt
$$
