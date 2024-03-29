# Validation

In order to validate SpaceMath v1.0, we apply the coupling modifiers $$\kappa_i$$ defined in eq. 3 to the Two-Higgs Doublet Model of Type I and II (THDM-I, II). In Ref. \[[44](broken-reference)] are reported $$\kappa_b$$ and $$\kappa_V$$ in the context of these models. To reproduce these results via $$\texttt{SpaceMath}$$ v1.0 the only thing we need is to know the model couplings, which are given in Table 9. The commands to evaluate $$\kappa_b$$ and $$\kappa_V$$ are displayed in Table 8.

<table><thead><tr><th width="329">Coupling</th><th width="661">Input to SpaceMath</th><th width="556"> Command \kappa_i</th></tr></thead><tbody><tr><td><span class="math">g_{hbb}^{THDM-I}=\frac{gm_{b}}{2m_{W}}\left(\frac{\cos\alpha}{\sin\beta}\right)</span></td><td><span class="math">\texttt{ghbb[Sa\_,Tb\_,Cb\_]:=g*mb*Sqrt[1-Sa\textasciicircum2]/(2*mW*Tb*Cb)}</span></td><td><span class="math">\texttt{kb[\texttt{ghbb[Sa,Tb,Cos[ArcTan[Tb]]}]]}</span></td></tr><tr><td><span class="math">g_{hbb}^{THDM-II}=\frac{gm_{b}}{2m_{W}}\left(\frac{-\sin\alpha}{\cos\beta}\right)</span></td><td><span class="math">\texttt{ghbb[Sa\_,Tb\_,Sb\_]:=-g*mb*Sa*Tb/(2*mW*Sb) }</span></td><td><span class="math">\texttt{kb[\texttt{ghbb[Sa,Tb,Sin[ArcTan[Tb]]}]]}</span></td></tr><tr><td><span class="math">g_{hVV}^{THDM-I,-II}=g_{V}m_{V}\sin(\beta-\alpha)</span></td><td><span class="math">\textrm{ghVV[Tb\_,Cb\_,Sb\_,Sa\_]:=((Tb*Cb*Sqrt[1-Sa\textasciicircum2])-(Sb/Tb*Sa))*(gv*mV)}</span></td><td><span class="math">\texttt{kV[ghVV[Tb, Cos[ArcTan[Tb]], Sin[ArcTan[Tb]], Sa]]}</span></td></tr></tbody></table>

Notice that $$\texttt{Sa} \equiv \sin(\alpha)$$, $$\texttt{Tb}\equiv\tan(\beta)$$, $$\texttt{Cb}\equiv\cos(\beta)$$, $$\texttt{Sb}\equiv\sin(\beta)$$ are free parameters of THDM-I, -II and $$V=Z, W$$; users can name them as they like; besides $$\tan\beta=\frac{\sin\beta}{\cos\beta}$$, $$\sin(\beta-\alpha)=\sin\beta\cos\alpha-\cos\beta\sin\alpha$$ has been used. The commands $$\texttt{kb}$$ and $$\texttt{kV}$$ can be directly evaluated by introducing values for $$\texttt{Sa, Tb, Cb}$$, or since $$\texttt{SpaceMath}$$ is hosted in $$\texttt{Mathematica}$$, we can use its commands to graph. For this example we use:

* $$\texttt{ContourPlot[kb[\texttt{ghbb[Sa,Tb,Cos[ArcTan[Tb]]}]]\textasciicircum2,\{Sa,-1,1\},\{Tb,0,20\}]},$$
* $$\texttt{ContourPlot[kV[ghVV[Tb,Cos[ArcTan[Tb]],Sin[ArcTan[Tb]],Sa]]\textasciicircum2,\{Sa,-1,1\},\{Tb,0,20\}]},$$

which generate the graphs displayed in Figs. 4, 5 and 6. The codes that generate these graphs can be found in the $$\texttt{"Examples"}$$ directory, whose path is: $$ $\texttt{SpaceMath/Examples/Validation_RX/SPACEMATH_RX-Validation-THDM.nb} $$ or click on the link $$\texttt{"Examples"}$$ once $$\texttt{SpaceMath}$$ was loaded.

<figure><img src="../.gitbook/assets/Figure4.jpg" alt=""><figcaption><p>Fig. 4: Contours of <span class="math">\Gamma(h \to b \bar b) / \Gamma(h_{SM} \to b \bar b)</span> for the SM-like Higgs boson as a function of <span class="math">\sin \alpha</span> and <span class="math">\tan \beta</span> in Type 1 THDM. Left: figure taken from [<a href="broken-reference">44</a>] and Right: figure generated by <span class="math">\texttt{SpaceMath v1.0}</span>.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Figure5.jpg" alt=""><figcaption><p>Fig. 5: Contours of <span class="math">\Gamma(h \to b \bar b) / \Gamma(h_{SM} \to b \bar b)</span> for the SM-like Higgs boson as a function of <span class="math">\sin \alpha</span> and <span class="math">\tan \beta</span> in Type 2 THDM. Left: figure taken from [<a href="broken-reference">44</a>] and Right: figure generated by <span class="math">\texttt{SpaceMath v1.0}</span>.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Figure6.jpg" alt=""><figcaption><p>Fig. 6: Contours of <span class="math">\Gamma(h \to VV^{\star}) / \Gamma(h_{SM} VV^{\star})</span> for the SM-like Higgs boson as a function of <span class="math">\sin \alpha</span> and <span class="math">\tan \beta</span> in any of the THDMs. Left: figure taken from [<a href="broken-reference">44</a>] and Right: figure generated by <span class="math">\texttt{SpaceMath v1.0}</span>.</p></figcaption></figure>

In addition, we also show in Fig. 7 the THDM-I, -II, Lepton Specific and Flipped parameter spaces in the $$\cos(\beta-\alpha)-\tan\beta$$ plane. Again, couplings are shown in Table 9. We compare our results with the ones reported by authors of Ref. \[[45](broken-reference)]. In these graphs we perform a $$\chi^2$$ test define as follows:

$$
\chi^2=\sum_{i=1}^n\left(\frac{O_i-E_i}{\sigma_i}\right)^2,
$$

where $$O_i$$ and $$E_i$$ are the observed and expected values, respectively, and $$\sigma_i$$ indicates uncertainty. The command for plot these figures is:

{% tabs %}
{% tab title="95 %" %}
```mathematica
Chi2Rx95[ghtt[-ArcCos[Cab] + ArcTan[tb], tb],ghbb[-ArcCos[Cab] + ArcTan[tb], tb], ghtautau[-ArcCos[Cab] + ArcTan[tb], tb], ghZZ[Sqrt[1 - Cab^2]],ghWW[Sqrt[1 - Cab^2]], 0, 2000, Cab, tb]
```
{% endtab %}

{% tab title="68 %" %}
```wolfram
Chi2Rx68[ghtt[-ArcCos[Cab] + ArcTan[tb], tb],ghbb[-ArcCos[Cab] + ArcTan[tb], tb], ghtautau[-ArcCos[Cab] + ArcTan[tb], tb],ghZZ[Sqrt[1 - Cab^2]],ghWW[Sqrt[1 - Cab^2]], 0, 2000, Cab, tb]
```
{% endtab %}
{% endtabs %}

Complete instructions can be found at:  $$ $\texttt{SpaceMath/Examples/Validation_RX/SPACEMATH_RX-Validation-THDM-Chi2Rx.nb} $$

| Coupling              | THDM-I                   | THDM-II                   | THDM-Lepton Specific      | THDM-Flipped              |
| --------------------- | ------------------------ | ------------------------- | ------------------------- | ------------------------- |
| $$hVV$$               | $$\sin(\beta-\alpha)$$   | $$\sin(\beta-\alpha)$$    | $$\sin(\beta-\alpha)$$    | $$\sin(\beta-\alpha)$$    |
| $$hu_{i}u_{i}$$       | $$\cos\alpha/\sin\beta$$ | $$\cos\alpha/\sin\beta$$  | $$\cos\alpha/\sin\beta$$  | $$\cos\alpha/\sin\beta$$  |
| $$hd_{i}d_{i}$$       | $$\cos\alpha/\sin\beta$$ | $$-\sin\alpha/\cos\beta$$ | $$\cos\alpha/\sin\beta$$  | $$-\sin\alpha/\cos\beta$$ |
| $$h\ell_{i}\ell_{i}$$ | $$\cos\alpha/\sin\beta$$ | $$-\sin\alpha/\cos\beta$$ | $$-\sin\alpha/\cos\beta$$ | $$\cos\alpha/\sin\beta$$  |

<figure><img src="../.gitbook/assets/Figure7.png" alt=""><figcaption><p>Fig. 7: Plane <span class="math">\cos(\beta-\alpha)-\tan\beta</span> for different versions of THDM's: (a) Type I, (b) Type II, (c) Lepton Specific, (d) Flipped. The plots were generated in <span class="math">\texttt{SpaceMath v1.0}</span>.</p></figcaption></figure>

We can observe slight differences between the graphs generated via $$\texttt{SpaceMath v1.0}$$ and those of the $$\texttt{Gfitter}$$ group, this is due to two sources: 1) The experimental data that $$\texttt{SpaceMath}$$ considers are the most recent and 2) the $$\texttt{Gfitter}$$ team includes all production modes of the Higgs boson. Here, it is worth mentioning that even though $$\texttt{SpaceMath v1.0}$$ only has gluon fusion production implemented, our results are highly similar, this may be because it is the dominant channel for the production of the higgs boson.

Besides the $$\chi^2$$ test, $$\texttt{SpaceMath v1.0}$$ also generates the region consistent with all individual observables; Fig. 8 shows the graph generated by $$\texttt{SpaceMath v1.0}$$.

<figure><img src="../.gitbook/assets/Figure8.png" alt=""><figcaption><p>Fig. 8: Intersection of all channels in the <span class="math">\cos(\beta-\alpha)-\tan\beta</span> plane for different versions of THDM’s: a) Type I, b) Type II, c) Lepton Specific, d) Flipped. The plots were generated in <span class="math">\texttt{SpaceMath v1.0}</span>.</p></figcaption></figure>

Finally, we shown in Table 10 a comparison between our numerical evaluations and those made via $$\texttt{HDecay}$$ package \[23], which the branching ratios of the Higgs boson decaying to pair of particles ($$b\bar{b}$$, $$s\bar{s}$$, $$c\bar{c}$$, $$t\bar{t}$$, $$\tau^+\tau^-$$, $$\mu^+\mu^-$$, $$gg$$, $$\gamma\gamma$$, $$Z\gamma$$, $$W^+W^-$$, $$ZZ$$) in the theoretical framework of the THDM-I are shown. Again, the Feynman rules needed for evaluations are shown in Table 9, where it can be seen that only two parameters are introduced. We take the same inputs for these free THDM-I parameters as in Ref. \[23], namely,

* $$\tan\beta$$= 1.29775,
* $$\alpha$$=-0.684653,

and we also consider a Higgs boson mass of $$m_{h}$$=125.09 GeV.

<table data-header-hidden><thead><tr><th width="178"></th><th width="163"></th><th width="203"></th><th width="188"></th><th width="201"></th><th width="139"></th></tr></thead><tbody><tr><td><span class="math">\mathcal{BR}(h\rightarrow b\bar{b})</span></td><td><span class="math">\mathcal{BR}(h\rightarrow\tau\tau)</span></td><td><span class="math">\mathcal{BR}(h\rightarrow\mu\mu)</span></td><td><span class="math">\mathcal{BR}(h\rightarrow s\bar{s})</span></td><td><span class="math">\mathcal{BR}(h\rightarrow c\bar{c})</span></td><td><span class="math">\mathcal{BR}(h\rightarrow t\bar{t})</span></td></tr><tr><td><p>0.6080 </p><p>(<span class="math">\textit{0.6080}</span>)</p></td><td><p>0.6542 </p><p>(<span class="math">\textit{0.6542}</span>)<span class="math">\times10^{-1}</span></p></td><td><p>0.2316</p><p>(<span class="math">\textit{0.2316}</span>)<span class="math">\times10^{-3}</span></p></td><td><p>0.2294 </p><p>(<span class="math">\textit{0.2294}</span>)<span class="math">\times10^{-3}</span></p></td><td><p>0.2653</p><p>(<span class="math">\textit{0.2653}</span>)<span class="math">\times10^{-1}</span></p></td><td>0 (<span class="math">\textit{0}</span>)</td></tr><tr><td><span class="math">\mathcal{BR}(h\rightarrow gg)</span></td><td><span class="math">\mathcal{BR}(h\rightarrow\gamma\gamma)</span></td><td><span class="math">\mathcal{BR}(h\rightarrow Z\gamma)</span></td><td><span class="math">\mathcal{BR}(h\rightarrow WW)</span></td><td><span class="math">\mathcal{BR}(h\rightarrow ZZ)</span></td><td></td></tr><tr><td><p>0.7041</p><p>(<span class="math">\textit{0.7041}</span>)<span class="math">\times10^{-1}</span></p></td><td><p>0.2126 </p><p>(<span class="math">\textit{0.2126}</span>)<span class="math">\times10^{-2}</span></p></td><td><p>0.1458 </p><p>(<span class="math">\textit{0.1458}</span>)<span class="math">\times10^{-2}</span></p></td><td>0.2005 (<span class="math">\textit{0.2005}</span>)</td><td><p>0.2507 </p><p>(<span class="math">\textit{0.2507}</span>)<span class="math">\times10^{-1}</span></p></td><td></td></tr><tr><td><span class="math">\mathcal{BR}(h\rightarrow AA)</span></td><td><span class="math">\mathcal{BR}(h\rightarrow AZ)</span></td><td><span class="math">\mathcal{BR}(h\rightarrow W\pm h\mp)</span></td><td><span class="math">\mathcal{BR}(h\rightarrow h+h-)</span></td><td><span class="math">\Gamma_{h}^{\textrm{tot}}</span></td><td></td></tr><tr><td><span class="math">0 (\textit{0})</span></td><td><span class="math">0 (\textit{0})</span></td><td><span class="math">0 (\textit{0})</span></td><td><span class="math">0 (\textit{0})</span></td><td><p>0.4248 </p><p>(<span class="math">\textit{0.4248}</span>)<span class="math">\times10^{-2}</span> GeV</p></td><td></td></tr></tbody></table>

In Table \[10], the quantities in brackets are the results generated via $$\texttt{SpaceMath}$$. We observe that our results are identical to those $$\texttt{HDecay}$$, which is to be expected since we actually reproduced the relevant expressions of the decay widths of the Higgs boson reported in Ref. \[[46](broken-reference)].
