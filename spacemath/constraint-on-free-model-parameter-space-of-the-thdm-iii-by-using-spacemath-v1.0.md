# Constraint on free model parameter space of the THDM-III by using SpaceMath v1.0

We now turn to constrain the free model parameter space of the THDM-III focusing on the Yukawa interactions. As previously we mentioned, in SpaceMath v1.0 only the Higgs boson data are enabled. Then, we use signal strengths to find allowed regions which are in accordance with the most up-to-date experimental reports. We give, step by step, instructions on how SpaceMath v1.0 works. For enthusiastic users go to the Sec. **THDM-III in** $$\texttt{SpaceMath v1.0}$$.

We first present an overview of the THDM-III focusing only on the details relevant of the Yukawa Lagrangian. For a detailed account of this model and the study of its phenomenology we refer the readers to Refs. \[[28](broken-reference)-[39](broken-reference)].

The most general $$SU(2)_L\times U(1)_Y$$ invariant scalar potential is given by \[[40](broken-reference), [41](broken-reference)]:

$$
V(\Phi_{1},\Phi_{2})=\mu_{1}^{2}(\Phi_{1}^{\dagger}\Phi_{1})+\mu_{2}^{2}(\Phi_{2}^{\dagger}\Phi_{2})-\left(\mu_{12}^{2}(\Phi_{1}^{\dagger}\Phi_{2})+H.c.\right)+\frac{1}{2}\lambda_{1}(\Phi_{1}^{\dagger}\Phi_{1})^{2}
$$

$$
+\frac{1}{2}\lambda_{2}(\Phi_{2}^{\dagger}\Phi_{2})^{2}+\lambda_{3}(\Phi_{1}^{\dagger}\Phi_{1})(\Phi_{2}^{\dagger}\Phi_{2})+\lambda_{4}(\Phi_{1}^{\dagger}\Phi_{2})(\Phi_{2}^{\dagger}\Phi_{1})
$$

$$
+\left(\frac{1}{2}\lambda_{5}(\Phi_{1}^{\dagger}\Phi_{2})^{2}+\left(\lambda_{6}(\Phi_{1}^{\dagger}\Phi_{1})+\lambda_{7}(\Phi_{2}^{\dagger}\Phi_{2})\right)(\Phi_{1}^{\dagger}\Phi_{2})+H.c.\right),
$$

where $$\mu_{1, 2}$$, $$\lambda_{1, 2, 3 ,4}$$ are real parameters while $$\mu_{12}$$, $$\lambda_{5, 6, 7}$$ can be complex in general. The doublets are written as $$\Phi_{a}^T=\left( \phi_{a}^{+}, \phi_{a}^0\right)$$ for $$a=1, 2$$. After the Spontaneous Symmetry Breaking (SSB) the two Higgs doublets acquire non-zero expectation values. The Vacuum Expectation Values (VEV) are selected as

$$
\langle\Phi_{a}\rangle=\frac{1}{\sqrt{2}}\left(\begin{array}{c}
0\\
\upsilon_{a}
\end{array}\right),\,a=1,\,2
$$

where $$\upsilon_1$$ and $$\upsilon_2$$ satisfy $$\upsilon_1^2 + \upsilon_2^2 = \upsilon^2$$ for $$\upsilon=246$$ GeV.

In the most general case both doublets can participate in the interactions with the fermion fields. The Yukawa Lagrangian is written as

$$
\mathcal{L}_{Y}=Y_{1}^{u}\bar{Q}_{L}^{'}\tilde{\Phi}_{1}u_{R}^{'}+Y_{2}^{u}\bar{Q}_{L}^{'}\tilde{\Phi}_{2}u_{R}^{'}+Y_{1}^{d}\bar{Q}_{L}^{'}\Phi_{1}d_{R}^{'}
$$

$$
+Y_{2}^{d}\bar{Q}_{L}^{'}\Phi_{2}d_{R}^{'}+Y_{1}^{\ell}\bar{L}_{L}^{'}\Phi_{1}\ell_{R}^{'}+Y_{2}^{\ell}\bar{L}_{L}^{'}\Phi_{2}\ell_{R}^{'}+H.c.,
$$

Because we are interested in neutral interactions we only present the neutral part of the Yukawa Lagrangian of Eq. 6 which reads \[[31](broken-reference)]:

$$
\mathcal{L}_{Y}^{N}=Y_{1}^{u}\bar{Q}_{L}^{0}\tilde{\Phi}_{1}u_{R}^{0}+Y_{2}^{u}\bar{Q}_{L}^{0}\tilde{\Phi}_{2}u_{R}^{0}+Y_{1}^{d}\bar{Q}_{L}^{0}\Phi_{1}d_{R}^{0}
$$

$$
+Y_{2}^{d}\bar{Q}_{L}^{0}\Phi_{2}d_{R}^{0}+Y_{1}^{\ell}\bar{L}_{L}^{0}\Phi_{1}\ell_{R}^{0}+Y_{2}^{\ell}\bar{L}_{L}^{0}\Phi_{2}\ell_{R}^{0}+h.c.
$$

with

$$
Q_{L}^{0}=\left(\begin{array}{c}
u_{L}\\
d_{L}
\end{array}\right),\;L^{0}=\left(\begin{array}{c}
\nu_{L}\\
e_{L}
\end{array}\right),\Phi_{1}=\left(\begin{array}{c}
\phi_{1}^{+}\\
\phi_{1}^{0}
\end{array}\right),\;\Phi_{2}=\left(\begin{array}{c}
\phi_{2}^{+}\\
\phi_{2}^{0}
\end{array}\right),\tilde{\Phi}_{j}=i\sigma_{2}\Phi_{j}^{*}.
$$

Here $$\Phi_i$$ $$(i=1, 2)$$ denotes the Higgs doublets and $$Y_i^f$$ stand for $$3\times3$$ Yukawa matrices. After SSB and algebraic manipulations, the Yukawa Lagrangian in term of physical states is given as follows:

$$
\mathcal{L}_{Y}=\frac{g}{2}\left(\frac{m_{d}}{m_{W}}\right)\bar{d}_{i}\left[\frac{\cos\alpha}{\cos\beta}\delta_{ij}+\frac{\sqrt{2}\sin(\alpha-\beta)}{g\cos\beta}\left(\frac{m_{W}}{m_{d}}\right)\left(\tilde{Y}_{2}^{d}\right)_{ij}\right]d_{j}H
$$

$$
+\frac{g}{2}\left(\frac{m_{d}}{m_{W}}\right)\bar{d}_{i}\left[-\frac{\sin\alpha}{\cos\beta}\delta_{ij}+\frac{\sqrt{2}\cos(\alpha-\beta)}{g\cos\beta}\left(\frac{m_{W}}{m_{d}}\right)\left(\tilde{Y}_{2}^{d}\right)_{ij}\right]d_{j}h
$$

$$
+i\frac{g}{2}\left(\frac{m_{d}}{m_{W}}\right)\bar{d}_{i}\left[-\tan\beta\delta_{ij}+\frac{\sqrt{2}}{g\cos\beta}\left(\frac{m_{W}}{m_{d}}\right)\left(\tilde{Y}_{2}^{d}\right)_{ij}\right]\gamma^{5}d_{j}A
$$

$$
+\frac{g}{2}\left(\frac{m_{u}}{m_{W}}\right)\bar{u}_{i}\left[\frac{\sin\alpha}{\sin\beta}\delta_{ij}-\frac{\sqrt{2}\sin(\alpha-\beta)}{g\sin\beta}\left(\frac{m_{W}}{m_{u}}\right)\left(\tilde{Y}_{2}^{u}\right)_{ij}\right]u_{j}H
$$

$$
+\frac{g}{2}\left(\frac{m_{u}}{m_{W}}\right)\bar{u}_{i}\left[\frac{\cos\alpha}{\sin\beta}\delta_{ij}-\frac{\sqrt{2}\cos(\alpha-\beta)}{g\sin\beta}\left(\frac{m_{W}}{m_{u}}\right)\left(\tilde{Y}_{2}^{u}\right)_{ij}\right]u_{j}h
$$

$$
+i\frac{g}{2}\left(\frac{m_{u}}{m_{W}}\right)\bar{u}_{i}\left[-\cot\beta\delta_{ij}+\frac{\sqrt{2}}{g\sin\beta}\left(\frac{m_{W}}{m_{u}}\right)\left(\tilde{Y}_{2}^{u}\right)_{ij}\right]\gamma^{5}u_{j}A,
$$

where $$i$$ and $$j$$ stand for the fermion flavors, with $$i\neq j$$, in general. As far as the lepton interactions, it is similar to type-down quarks part with the exchange $$d\to\ell$$ and $$m_d\to m_{\ell}$$. The physical particles $$h, H, A$$ were obtained through a rotation depending on mixing angles $$\alpha$$ and $$\beta$$ as follows:

$$
\left(\begin{array}{c}
H\\
h
\end{array}\right)=\left(\begin{array}{cc}
\cos\alpha & \sin\alpha\\
-\sin\alpha & \cos\alpha
\end{array}\right)\left(\begin{array}{c}
Re\Phi_{1}\\
Re\Phi_{2}
\end{array}\right),
$$

$$
\left(\begin{array}{c}
G\\
A
\end{array}\right)=\left(\begin{array}{cc}
\cos\beta & \sin\beta\\
-\sin\beta & \cos\beta
\end{array}\right)\left(\begin{array}{c}
Im\Phi_{1}\\
Im\Phi_{2}
\end{array}\right),
$$

$$
\left(\begin{array}{c}
G^{\pm}\\
H^{\pm}
\end{array}\right)=\left(\begin{array}{cc}
\cos\beta & \sin\beta\\
-\sin\beta & \cos\beta
\end{array}\right)\left(\begin{array}{c}
\Phi_{1}^{\pm}\\
\Phi_{2}^{\pm}
\end{array}\right),
$$

with the angle $$\beta$$ given by:

$$
\tan\beta=\frac{v_2}{v_1}.
$$
