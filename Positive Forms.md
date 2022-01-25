<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
<script type="text/x-mathjax-config">
 MathJax.Hub.Config({
 tex2jax: {
 inlineMath: [['$', '$'], ["\\(","\\)"] ],
 displayMath: [ ['$$','$$'], ["\\[","\\]"] ]
 }
 });
</script>

# Positive Forms
## Canonical orientation
***
Let us first observe that $V$ has a canonical orientation, given by the $(n,n)$-form 
\begin{equation}
    \tau(z) = idz\_1 \wedge d\overline{z}\_1 \wedge \cdots \wedge idz\_n \wedge d\overline{z}\_n
    = 2^n dx\_1 \wedge dy\_1 \wedge \cdots \wedge dx\_n \wedge dy\_n,    
\end{equation}
where $z_j = x_j + i y_j$. 
In facts, if $(w_1, \ldots, w_n)$ are other coordinates, we have 
\begin{equation}
    dw_1 \wedge \cdots \wedge dw_n 
    = \det\left( \frac{\partial w_k}{\partial z_k} \right) dz_1 \wedge \cdots \wedge dz_n
\end{equation}
and 
\begin{equation}
    \tau(w) = \left\lvert\det\left(\frac{\partial w_k}{\partial z_k}\right)\right\rvert^2 \tau(z). 
\end{equation}
In paticular, a complex manifold always has a canonical orientation.

## Positive forms
***
A $(p,p)$-form $u \in \Lambda^{p,p}V^{\ast}$ is said to be positive 
if for all $\alpha\_j \in V^{\ast}$, $1 \leq j \leq q = n - p$,
\begin{equation}
    u \wedge i \alpha\_1 \wedge \overline{\alpha}\_1 \wedge \cdots \wedge i \alpha\_q \wedge \overline{\alpha}\_q
\end{equation}
is a positive $(n,n)$-form.
A $(q,q)$-form $v \in \Lambda^{q,q}V^{\ast}$ is said to be strongly positive if $v$ is a convex combination
\begin{equation}
    v = \sum \gamma\_s i\alpha\_{s,1} \wedge \overline{\alpha}\_{s,1} \wedge \cdots \wedge i {\alpha}\_{s,q}\wedge \overline{\alpha}\_{s,q},
\end{equation}
where $\alpha_{s,j} \in V^{\ast}$ and $\gamma_s \geq 0$.
The sets of positive and strongly positive forms are closed convex cones, i.e. 
closed and stable under convex combinations.
By definition, the positive cone is dual to the strongly positive cone via the pairing
\begin{equation}
    \Lambda^{p,p}V^{\ast} \times \Lambda^{q,q}V^{\ast} \rightarrow \mathbb{C}, 
    \quad (u, v) \mapsto u \wedge v / \tau,
\end{equation}
that is, $u \in \Lambda^{p,p}V^{\ast}$ is positive 
if and only if $u \wedge v \geq 0$ for all strongly positive forms $v \in \Lambda^{q,q}V^{\ast}$.

Similarly, we obtain that $v \in \Lambda^{p,p}V^{\ast}$ is strongly positive 
if and only if $u \wedge v \geq 0$ for all positive forms $u \in \Lambda^{q,q}V^{\ast}$.

More precisely, the strongly positive conse is defined by 
\begin{equation}
    \Gamma_p^s = \operatorname{conv}
    \left\\\{ i\alpha_1 \wedge \overline{\alpha}_1 \wedge \cdots \wedge i\alpha_p \wedge \overline{\alpha}_p 
    \mid \alpha_j \in V^{\ast} \right\\\}
\end{equation}
and the positive cone is defined by 
\begin{equation}
    \Gamma_p = \left(\Gamma_p^s\right)^{\ast}
    = \left\\\{ v \in \Lambda^{p,p}V^{\ast} \mid \langle v, u \rangle \geq 0 \quad \forall u \in \Gamma_q^s \right\\\}.
\end{equation}
Since $\Gamma_p^s$ is a closed convex cone, we also obtain by duality that 
\begin{equation}
    \Gamma_p^s = \left(\Gamma_p\right)^{\ast} 
    = \left\\\{ v \in \Lambda^{p,p}V^{\ast} 
    \mid \langle v, u \rangle \geq 0 \quad \forall u \in \Gamma_q \right\\\}.
\end{equation}  

## Lemma.
***
Let $C$ be a closed convex cone.
Then we have $C = C^{\ast\ast}$.

<details><summary>**Proof**▼</summary><div>
    By definition, it follows that $C \subset C^{\ast\ast}$.
    For the other direction, we need to show 
    that any element not in $C$ has negative inner product with at least one element in $C^{\ast\ast}$.
    Suppose $x \notin C$, then by Farkas Lemma, 
    there exists a hyperplane which separates the point $x$ and the closed convex set $C$.
    Thus there exists $y$ such that $y^Tx < 0 \leq y^Tz$, $\forall z \in C$.
    This implies $y \in C^{\ast}$ and $x \notin C^{\ast\ast}$, which completes the proof.□
</div></details>

## Example.
Since $i^p(-1)^{\frac{p(p-1)}{2}} = i^{p^2}$, we have the commutation rules:
\begin{gather}
    i\alpha\_1 \wedge \overline{\alpha}\_1 \wedge \cdots \wedge i \alpha\_p \wedge \overline{\alpha}\_p 
    = i^{p^2} \alpha \wedge \alpha, 
    \quad \alpha = \alpha\_1 \wedge \cdots \wedge \alpha\_p \in \Lambda^{p,0}V^{\ast}, \\\\
    i^{p^2}\beta \wedge \overline{\beta} \wedge i^{m^2} \gamma \wedge \overline{\gamma}
    = i^{(i+m)^2} \beta \wedge \gamma \wedge \overline{\beta \wedge \gamma}, 
    \quad \beta \in \Lambda^{p,0}V^{\ast}, \gamma \in \Lambda^{m,0}V^{\ast}. 
\end{gather}
Take $m = q$ to be the complementary degree of $p$.
Then we have $\beta \wedge \gamma = \lambda dz\_1 \wedge \cdots \wedge dz\_n$ for some $\lambda \in \mathbb{C}$
and 
\begin{align}
    i^{p^2}\beta \wedge \overline{\beta} \wedge i^{m^2} \gamma \wedge \overline{\gamma}
    &= \lvert \lambda \rvert^2 i^{n^2} dz\_1 \wedge \cdots \wedge dz\_n \wedge d\overline{z}\_1 \wedge \cdots \wedge d\overline{z}\_n \\
    &= \lvert \lambda \rvert^2 \tau(z).
\end{align}
Setting $\gamma = \alpha_1 \wedge \cdots \wedge \alpha_q$, we find that 
$i^{p^2}\beta \wedge \overline{\beta}$ is a positive $(p,p)$-form for every $\beta \in \Lambda^{p,0}V^{\ast}$.
In paticular, strongly positive forms are positive.
Putting together, we conclude that 

* Strongly positive forms are written in the form $i^{p^2}\beta \wedge \overline{\beta}$ 
with some $\beta \in \Lambda^{p,0}V^{\ast}$.

* Forms written in the form  $i^{p^2}\beta \wedge \overline{\beta}$ 
with some $\beta \in \Lambda^{p,0}V^{\ast}$ are positive.

* The wedge product of two positive forms written in the form $i^{p^2}\beta \wedge \overline{\beta}$ 
with some $\beta \in \Lambda^{p,0}V^{\ast}$ is also written in the same form, 
which implies that it is also a positiv form.

## Lemma.
***
Let $(z\_1, \ldots, z\_n)$ be arbitrary coordinates on $V$.
Then $\Lambda^{p,p}V^{\ast}$ admits a basis consisting of strongly positive forms 
\begin{equation}
    \beta\_s  = i\beta\_{s,1} \wedge \overline{\beta}\_{s,1} \wedge \cdots \wedge i\beta\_{s,p} \wedge \overline{\beta}\_{s,p},
    \quad 1 \leq s \leq \binom{n}{p}^2,
\end{equation}
where each $\beta_{s,l}$ is of the type $dz_j \pm dz_k$ or $dz_j \pm i dz_k$, $1 \leq j, k \leq n$.

## Corollary.
***
Every positive form $u$ is real, i.e. satisfies $\overline{u} = u$.
In terms of coodinates, if $u = i^{p^2} \sum u\_{I,J} dz\_I \wedge d\overline{z}\_J$,
then the coefficients satisfy the hermitian symmetric relation $\overline{u\_{I,J}} = u\_{J,I}$.

<details><summary>**Proof**▼</summary><div>
    It is clear that every strongly positive $(q,q)$-form is real.
    By Lemma 1.4, these forms generate over $\mathbb{R}$ the  real elements of $\Lambda^{q,q}V^{\ast}$.
    Hence, if $u = i^{p^2}\sum u\_{I,J} dz\_I \wedge d\overline{z}\_J$ is positive, we obtain by duality that 
    \begin{align}
        \langle u, v \rangle \text{ is real}
        &amp;\Longleftrightarrow \langle u, v \rangle = \overline{\langle u, v \rangle} \\\\
        &amp;\Longleftrightarrow \langle u - \overline{u}, v \rangle = 0
    \end{align}
    for every real form $v \in \Lambda^{q,q}V^{\ast}$.
    By replacing $v$ with 
    $$i^{p^2}dz\_{I^c} \wedge d\overline{z}\_{J^c} + i^{p^2}dz\_{J^c} \wedge d\overline{z}\_{I^c}$$
    or  
    $$i^{p^2} \cdot idz\_{I^c} \wedge d\overline{z}\_{J^c} - i^{p^2} \cdot idz\_{J^c} \wedge d\overline{z}\_{I^c},$$
    we conclude that $\overline{u\_{I,J}} = u\_{J,I}$.□
</div></details>


## Lemma.
***
A form $u = i \sum u\_{jk} dz\_j \wedge d\overline{z}\_k$ of bidegree $(1,1)$ is positive 
if and only if $\xi \mapsto \sum u\_{jk} \xi\_j \xi\_k$ is a semi-positive definite hermitian form on $\mathbb{C}^n$.

## Correspondence to Hermitian Forms
***
There is a canonical one-to-one correspondence between hermitian forms and real $(1,1)$-forms on $V$ given by 
\begin{equation}
    h = \sum h\_{jk}(z) dz\_j \otimes d\overline{z}\_k \mapsto u = i \sum h\_{jk}(z) dz\_j \wedge d\overline{z}\_k.
\end{equation}
This correspondence does not depend on the choice of coordinates.
Indeed, it follows immediately from $\overline{h}\_{jk} = h\_{kj}$ that, for all $\xi, \eta \in TX$,
\begin{equation}
    u(\xi, \eta) = i\sum h\_{jk}(z)(\xi\_j\overline{\eta}\_k - \eta\_j\overline{\xi}\_k)
    = -2i \Im h(\xi,\eta).
\end{equation}
Moreover, $h$ is positive as a hermitian form if and only if $u$ is a positive $(1,1)$-form.
A diagonalization of $h$ shows that every positive $(1,1)$-form $u \in \Lambda^{1,1}V^{\ast}$ can be written 
\begin{equation}
    u = \sum_{1 \leq j \leq r}i \gamma_j \wedge \overline{\gamma}_j,
\end{equation}
where $\gamma_j \in V^{\ast}$ and $\gamma$ is the rank of $u$.
In paticular, every positive $(1,1)$-form is strongly positive.
By duality, this is also true for $(n-1, n-1)$-forms.
The notions of positive and strongly positive $(p,p)$-forms coincide for $p=0, 1, n-1, n$.
However, it is not difficult to see that 
positivity and strong positivity differ in all bidegree $(p,p)$ with $2 \leq p \leq n-2$.

## Proposition.
***
Let $2 \leq p \leq n-2$. 
A positive form $i^{p^2}\beta \wedge \overline{\beta} \in \Lambda^{p,p}V^{\ast}$ 
with $\beta \in \Lambda^{p,0}V^{\ast}$ is strongly positive if and only if 
$\beta$ is decomposable as a product $\beta_1 \wedge \cdots \wedge \beta_p$, $\beta_j \in V^{\ast}$.

<details><summary>**Proof**▼</summary><div>
    It is easily seen that $\beta \wedge \overline{\beta}$ is strongly positive if $\beta$ is decomposable.
    We will prove the other direction.
    Suppose that 
    \begin{equation}
        i^{p^2}\beta \wedge \overline{\beta} 
        = \sum_{1 \leq j \leq N} i^{p^2} \gamma_j \wedge \overline{\gamma}_j,
    \end{equation}
    where $\gamma_j \in V^{\ast}$ are all decomposable.
    Take $N$ minimal.
    The equality can be also written as an equality of hermitian forms 
    \begin{equation}
        \beta \otimes \overline{\beta} = \sum \gamma_j \otimes \overline{\gamma}_j
    \end{equation}
    if $\beta$ and $\gamma_j$ are seen as linear forms on $\Lambda^pV$.
    That is, in the similar way as the above argument, 
    $\beta \wedge \overline{\beta}$ is regarded as a hermitian form $\Lambda^pV$ by 
    $\beta \otimes \overline{\beta} \mapsto i \beta\wedge\overline{\beta}$.
    Note that the correspondence does not depend on the choice coordinates.
    Finally, we conclude that 
    \begin{equation}
        \beta \otimes \overline{\beta} = \sum \gamma_j \otimes \overline{\gamma}_j
    \end{equation}
    as hermitian forms on $\Lambda^pV$.
    The hermitian form $\beta \otimes \overline{\beta}$ has rank one 
    and we must have $N = 1$ and $\beta = \lambda \gamma_1$, which implies $\beta$ is decomposable.□
</div></details>


## Example.
***
Let $2 \leq p \leq n-2$.
It is easily seen that 
$\beta = (dz\_1 \wedge dz\_2 + dz\_3 \wedge dz\_4) \wedge dz\_5 \wedge \cdots \wedge dz\_{p+2}$ is not decomposable 
and thus $i^{p^2}\beta \wedge \overline{\beta}$ is positive but not strongly positive $(p,p)$-form.
On the other hand, it follows from definition that 

(a)If $u_1, \ldots, u_s$ are strongly positive, then $u_1 \wedge \cdots \wedge u_s$ is strongly positive.

(b)If $u_1, \ldots, u_s$ are strongly positive except one, then $u_1 \wedge \cdots \wedge u_s$ is positive.

(c)The wedge product of two positive forms is not positive in general.

## Proposition.
If $\Phi \colon W \rightarrow V$ is a complex linear map and $u \in \Lambda^{p,p}V^{\ast}$ si (strongly) positive,
then $\Phi^{\ast} u \in \Lambda^{p,p}W^{\ast}$ is (strongly) positive.
<details><summary>**Proof**▼</summary><div> 
    This follows from the commutativity of pull-back and wedge product.□
</div></details>

## References
***
>* [SeveralComplexVariables](/Complex%20Analysis/References/SeveralComplexVariables.pdf)
>* [J.P.Demaily, Complex Analytic and Differential Geometry](/Complex%20Analysis/References/agbook.pdf)

## External Links
***