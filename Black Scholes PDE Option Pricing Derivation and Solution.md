# Black-Scholes-Merton Partial Differential Equation Option Pricing

## Part 1. Derivation

### Assumptions:

1. The stock price follow geometric Brownian motion, with expect return $\mu$ and volatility $\sigma$
2. No transaction costs and taxes
3. No arbitrage chances
4. Security prices are continuous 
5. The risk-less interest rate is constant

### Derivation:

The stock return is ![](https://latex.codecogs.com/svg.latex?\frac{dS_t}{S_t}= \mu dt+\sigma dB_t), $B_t$ is a Brownian motion,$\iff dS_t= \mu S_tdt+\sigma S_tdB_t\quad(1)$;

The bond return is $\frac{dP_t}{P_t}=rdt\iff dP_t=rP_tdt \quad(2)$;

Construct a portfolio which value is 0: $V+f_sS+ f_pP = 0$, $f_s$ is the shares of the stock, and  $f_p$ is the shares of the bond, V is the value of the option, by no arbitrage assumption, $dV+f_sdS+f_pdP = 0\quad(3)$;

By Ito's lemma, for $ V = V(t,S)$,
$$
\begin{split}
dV &= \frac{\part V}{\part t}dt+\frac{\part V}{\part S}dS+\frac{1}{2}\frac{\part V^2}{\part^2 S}(dS)^2\\
&=\frac{\part V}{\part t}dt+\frac{\part V}{\part S}(\mu Sdt+\sigma SdB)+\frac{1}{2}\frac{\part V^2}{\part^2 S}(dS)^2\\
&=\frac{\part V}{\part t}dt+\frac{\part V}{\part S}(\mu Sdt+\sigma SdB)+\frac{1}{2}\frac{\part V^2}{\part^2 S}(\sigma SdB)^2 [Ignore\quad dt's\quad 
Infinitesimal]\\
&=(\frac{\part V}{\part t}+\frac{\part V}{\part S}\mu S_t+\frac{1}{2}\frac{\part V^2}{\part^2 S}\sigma^2 S^2）dt+\frac{\part V}{\part S}\sigma SdB[(dB)^2=dt]
\end{split}
$$
Substituting (1)(2) into the equation (3), then
$$
(\frac{\part V}{\part t}+\frac{\part V}{\part S}\mu S_t+\frac{1}{2}\frac{\part V^2}{\part^2 S}\sigma^2 S^2）dt+\frac{\part V}{\part S}\sigma SdB+f_s(\mu Sdt+\sigma SdB)+f_prPdt=0\quad(4)
$$
and $f_p=-\frac{V+f_sS}{P}$, then 
$$
(\frac{\part V}{\part t}+\frac{\part V}{\part S}\mu S_t+\frac{1}{2}\frac{\part V^2}{\part^2 S}\sigma^2 S^2）dt+\frac{\part V}{\part S}\sigma SdB+f_s(\mu Sdt+\sigma SdB)-(V+f_sS)rdt=0\\
\iff\\
(\frac{\part V}{\part t}+\frac{\part V}{\part S}\mu S_t+\frac{1}{2}\frac{\part V^2}{\part^2 S}\sigma^2 S^2 -rV+(\mu S-rS)f_s)dt+(\frac{\part V}{\part S}+f_s)\sigma SdB=0
$$
Because of the Delta hedging, coefficients of $dB$ and $dt$ should be 0, then
$$
f_s = -\frac{\part V}{\part S},\mu = r,\\
\frac{\part V}{\part t}+\frac{\part V}{\part S}\mu S_t+\frac{1}{2}\frac{\part V^2}{\part^2 S}\sigma^2 S^2 =rV
$$
That is the B-S PDE.

## Part 2. Solution

To be continued
