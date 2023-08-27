# LHC Higgs boson data

### Signal strength modifiers $$\mathcal{R}_X$$

For a production process $$\sigma(pp\to H_i)$$ and a decay $$H_i\to X$$, the signal strength is defined as follows:

$$
\mathcal{R}_{X}=\frac{\sigma(pp\to h)\cdot\mathcal{BR}(h\to X)}{\sigma(pp\to h^{\text{SM}})\cdot\mathcal{BR}(h^{\text{SM}}\to X)},
$$

where $$\sigma(pp\to H_i)$$ is the production cross section of $$H_i$$, with $$H_i=h,h^{\text{SM}}$$; here $$h$$ is the SM-like Higgs boson coming from an extension of the SM and $$h^{\text{SM}}$$ is the SM Higgs boson; $$\mathcal{BR}(H_i\to X)$$ is the branching ratio of the decay $$H_i\to X$$, with $$X=b\bar{b}, \tau^-\tau^+,\mu^-\mu^+,WW^*,ZZ^*,\gamma\gamma$$. In SpaceMath v1.0, we only consider the Higgs boson production cross section via the gluon fusion mechanism and we use the narrow width approximation:

$$
\mathcal{R}_{X}\approx\frac{\Gamma(h\to gg)\cdot\mathcal{BR}(h\to X)}{\Gamma(h^{\text{SM}}\to gg)\cdot\mathcal{BR}(h^{\text{SM}}\to X)}.
$$

### Higgs boson coupling modifiers $$\kappa_i$$

The coupling modifiers $$\kappa_i$$ are introduced to quantify the deviations of the SM-like Higgs boson to other particles. The coupling modifiers $$\kappa_i$$ for a production cross section or a decay mode, are defined as follows:

$$
\kappa_{pp}^2=\frac{\sigma(pp\to h)}{\sigma(pp\to h^{\text{SM}})}\;\text{or}\;\kappa_X^2=\frac{\Gamma(h\to X)}{\Gamma({h^\text{SM}}\to X)}.
$$

We consider tree-level Higgs boson couplings to different particles, i.e., $$g_{hZZ^*}$$_,_ $$g_{hWW^*}$$, $$g_{h\tau^-\tau^+}$$, $$g_{h\mu^-\mu^+}$$, $$g_{hb\bar{b}}$$, as well as effective coupling modifiers $$g_{hgg}$$ and $$g_{h\gamma\gamma}$$ which describe gluon fusion production $$\texttt{ggh}$$ and the $$h\to\gamma\gamma$$ decay, respectively.

The organization of our work is as follows. In Sec. **Installation** we present, in a concise way, how SpaceMath v1.0 can be installed. Sec. **First steps** is devoted to show as SpaceMath v1.0 works, giving a detailed example. Sec. **Validation** is focused on the validation of SpaceMath v1.0 by reproducing several results shown in the literature.&#x20;
