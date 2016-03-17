% Numerical Simulations Assignment 2 presentation
% Teun Hoppenbrouwers ANR:751611
% UVT

Introduction
============
- This will be the presentation version of Assignment 2, where I transcribed part of a Game theory 2 Assignment in Latex.

Question 
--------------------------------------
Firm A (the "Acquirer") is considering taking over firm T (the "Target"). It does not know firm T's value $x$; it believes that this value, when firm T is controlled by its own management, is drawn from the cumulative distribution function $F(x)=x(2-x)$ on the support [0,1]. Firm T knows it own value. Firm T will be worth twice as much under firm A´s management than it is under its own management. Suppose that firm A bids $y$ to take over firm T. Then if T accepts A´s offer, A´s payoff is $2x-y$ and T's payoff is $y$; if T rejects A's offer, A's payoff is $0$ and T's payoff is $x$.



A
--------------------------------
Model this situation as a Bayesian game in which firm A chooses how much to offer and firm T decides the lowest offer to accept. Make sure to properly define the type spaces, action spaces, beliefs, strategies and payoff functions of the players.

A
-------------------------------------
- A has 1 type. Types of T are different firm values ($x$) distributed over interval [0,1]. Action A: bids $y$ to take over T, $y$ distributed over  $[ 0,\infty )$- 
- Action T: Reject or accept $y$, T will only accept if $y\geq x$ 
- A beliefs $x$ is drawn from CDF $F(x)=x(2-x)$, T knows own $x$.
- Strategy A $\rightarrow$ bid $y$  $[ 0,\infty ) $ 
- Strategy T $\rightarrow$ accept or reject $y$ ( Only accept $y$ if $y\geq x$ ) 

B
---------------------------------
- What is the (unconditional) expected value of Firm T (under its own management)

- $E(x)=\int^{+\infty}_{-\infty} x*f(x)dx$ 
- $F(x)=x(2-x)=x^2+2x$ 
- $f(x)=F'(x)=-2x+2$ 
- $E(x)=\int_{0}^{1} x*(-2x+2)=\int_{0}^{1} -2x^2+2x$ 
- $-2/3*1^3+1^2=1/3$ 

C
----------------------------------
Find the Bayesian Nash equilibrium (equilibria?) of this game [Hint: $E(x\mid x\leq y)=(\int_{0}^{y}xf(x)dx)/F(y)$, where $f(x)=F'(x)$ is the probability density function of $x$.]

C
------------------------------------
-firm value $x$ is distributed over [0,1] T will only accept $y$ if $y \geq x$. 
- A can bid under or above 1. If bid is higher or equal than 1 firm T will always accept (1 is max possible firm value) 
- $E(x\mid x\leq y)$ is expected $x$ of firm that accept $y$ 
- $E(x\mid x\leq y)=(\int_{0}^{y}xf(x)dx)/F(y)$ 
- $f(x)=-2x+2$ 
- $\int_{0}^{y}x*(-2x+2)=\int_{0}^{y}-2x^2+2x$ 
- $-(2/3)y^3+y^2$ 
- $F(y)=y(2-y)$ 
- $E(x\mid x\leq y)= (-(2/3)y^3+y^2)/(-y^2+2y)$ 
- the value above is the expected value of a firm if it accepts $y$ when $y \leq 1$, if $y > 1$ all types will accept. Expected value of all types is 1/3 (see Question B) 
- payoff A if $y \leq 1$ \\ $2x-y=2*(-(2/3)y^3+y^2)/(-y^2+2y)-y$ 
$2*(-(2/3)y^3+y^2)/(-y^2+2y)-y \leq 0$ on interval [0,1] 
- payoff A if $y>1$ 
- $2*(1/3)-y<0$ 
- Nash equilibrium is for A to bid 0.