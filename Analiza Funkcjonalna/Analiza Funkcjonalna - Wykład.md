# Zbiory wypukłe

## Podstawowe oznaczenia

 - $\mathbb{K}$ - ciało (domyślnie $\mathbb{R}$ lub $\mathbb{C}$)
 - $\mathcal{X, Y, Z}$ - Przestrzenie liniowe nad $\mathbb{K}$
 - $a, b, c, \alpha, \beta, \gamma \in \mathbb{K}$
 - $x, y, z \in \mathcal{X}$

 > [!def] Odcinek
 > **Odcinek** o końcach $x, y$ to zbiór:
 > $$
 >     [x,y] := \lbrace \lambda x + (1 - \lambda) y \ : \ 0 \leq \lambda \leq 1 \rbrace
 > $$

 > [!def] Zbiór wypukły
 > Zbiór $K \subset X$ jest **wypukły** gdy:
 > $$
 >     \left( \forall x,y \in K \right) \left( [x,y] \subset K \right)
 > $$
 > Czyli gdy odcinek między każdymi dwoma punktami zbioru jest zawarty w tym zbiorze.
 > > [!note]
 > > Przekrój $\bigcap_\alpha K_\alpha$ rodziny zbiorów wypukłych jest zbiorem wypukłym.

 > [!def] Otoczka wypukła
 > **Otoczką wypukłą** zbioru $A$ nazywamy przekrój wszystkich zbiorów wypukłych zawierających $A$. Oznaczamy ją $\mathrm{conv} A$.
 > > [!note] 
 > > $\mathrm{conv} A$ jest najmniejszym zbiorem wypukłym zawierającym $A$.
 >
 > > [!note]
 > > $$
 > > \mathrm{conv} A = \lbrace 
 > >     \sum_{j=1}^m \lambda_j x_j \ : \
 > >     \sum_{j=1}^m \lambda_j = 1,
 > >     \lambda_j \geq 0,
 > >     x_j \in A, 
 > >     m \in \mathbb{N}
 > > \rbrace
 > > $$

 > [!def] Kombinacja wypukła
 > **Kombinacja wypukła** $x_1, x_2, \dots, x_m$ to zbiór:
 > $$
 > \lbrace 
 >     \sum_{j=1}^m \lambda_j x_j \ : \
 >     \sum_{j=1}^m \lambda_j = 1,
 >     \lambda_j \geq 0,
 > \rbrace
 > $$

 > [!def] Funkcjonał Minkowskiego
 > Funkcję $p : X \to [0, \infty]$ nazywamy **funkcjonałem Minkowskiego** gdy dla każdego $x \in X$:
 >  1. $0 \leq p(x) < \infty$
 >  2. $p(x+y) \leq p(x) + p(y)$
 >  3. $\left(\forall \lambda > 0\right) \left( p(\lambda x) = \lambda p(x) \right)$
 > > [!note]
 > > $p(0) = 0$

 > [!def] Zbiór pochłaniający
 > Zbiór $K \subset X$ nazywamy **pochłaniającym** gdy:
 > $$
 > \left( \forall x \in X \right) 
 > \left( \exists \lambda > 0 \right)
 > \left( \lambda x \in K \right)
 > $$
 > *Note*: jeśli $K$ jest pochłaniający to $0 \in K$.

 > [!tw] Twierdzenie
 > Niech $K \subset X$ będzie wypukły i pochłaniający. Wówczas funkcja
 > $$
 >  p_K(x) = \inf 
 >  \lbrace
 >      \lambda > 0, x \in \lambda K
 >  \rbrace
 > $$
 > jest funkcjonałem Minkowskiego. Ponadto:
 >  1. $x \in K \implies p_K(x) \leq 1$
 >  2. $p_K(x) < 1 \implies x \in K$

 > [!tw] Twierdzenie
 > Niech $p(x)$ będzie funkcjonałem Minkowskiego. Wówczas
 > $$ K = \lbrace x \in X \ : \ p(x) \leq 1 \rbrace $$
 > jest zbiorem wypukłym i pochłaniającym. Ponadto $p(x) = p_K(x)$.

# Twierdzenie Hahna-Banacha 

 > [!def] Funkcjonał liniowy
 > **Funkcjonałem liniowym** nazywamy odwzorowanie liniowe $\phi : X \to \mathbb K$

 > [!tw] Twierdzenie Hahna-Banacha (wersja rzeczywista)
 >
 > Niech $p : X \to [0, \infty]$ będzie funkcjonałem Minkowskiego oraz $X_0 \subset X$.
 > Załóżmy, że $\phi : X_0 \to \mathbb R$ jest funkcjonałem liniowym takim, że 
 > $$ (\forall x \in X_0) (\phi(x) \leq p(x)) $$
 > Istnieje wówczas funkcjonał liniowy $\psi : X \to \mathbb R$ taki, że:
 >  1. $(\forall x \in X_0) (\psi(x) = \phi(x))$
 >  2. $(\forall x \in X) (\psi(x) \leq p(x))$
 >
 > Czyli funkcjonał $\phi$ można przedłużyć na całą przestrzeń, z zachowaniem kontroli przez $p(x)$.
 > 
 > > [!dowód]-
 > > Dowód opiera się na lemacie:
 > > > [!lemat]
 > > > $X_0 < X$ i $z \in X \setminus X_0$ i $\widetilde{X} = \mathrm{lin} \lbrace X_0, \lbrace z \rbrace \rbrace$
 > > > 
 > > > to $\phi$ można rozszerzyć do $\widetilde{X}$ z zachowaniem kontroli przez $p(x)$.
 > >
 > > $\mathcal A$ zbiór par $(\widetilde X, \widetilde \phi)$, gdzie $X_0 < \widetilde X < X$,
 > > $\widetilde \phi$ - f. rzeczywisty na $\widetilde X$ taki, że $\widetilde \phi = \phi$ na $X_0$ i $\widetilde \phi (x) \leq p(x)$ na $\widetilde X$.
 > >
 > > $\mathcal A$ ma częściowy porządek (zawieranie podprzestrzeni i funkcjonału) o własności, że każdy łańuch ma ograniczenie górne.
 > > Z L-K-Z mamy, że $\mathcal A$ ma element maksymalny. Dowodzimy że przestrzeń tego elementu jest równa $X$.

 > [!def] Półnorma
 > Funkcjonał Minkowskiego $p : X \to [0, \infty]$ nazywamy **półnormą** gdy
 > $p(\alpha x) = |\alpha| \ p(x), \ \alpha \in \mathbb K, \ x \in X$

 > [!def] Zbiór zbalansowany
 > $K$ jest zbalansowany gdy dla każdego $\alpha \in \mathbb K, |\alpha| = 1$:
 >
 > $\alpha K \subset K$ lub równoważnie $\alpha K = K$
 > > [!note] 
 > > $p_K$ jest półnormą. Odwrotnie, jeśli $p$ - półnorma to $K = \lbrace x : p(x) \leq 1 \rbrace$ spełnia powyższy warunek.

 > [!tw] Twierdzenie Hahna-Banacha
 >
 > Niech $p : X \to [0, \infty]$ będzie półnormą oraz $X_0 \subset X$.
 > Załóżmy, że $\phi : X_0 \to \mathbb R$ jest funkcjonałem liniowym takim, że 
 > $$ |\phi(x)| \leq p(x) $$
 > Istnieje wówczas funkcjonał liniowy $\psi : X \to \mathbb R$ taki, że:
 >  1. $\psi(x) = \phi(x)$ w $X_0$
 >  2. $\psi(x) \leq p(x)$ w $X$
 >
 > Czyli funkcjonał $\phi$ można przedłużyć na całą przestrzeń, z zachowaniem kontroli przez $p(x)$.
 >
 > > [!dowód]-
 > > 
 > > > [!lemat]
 > > > $\phi$ funkcjonał zespolony. Niech $\phi_1 = \mathrm{Re} \ \phi$ i $\phi_2 = \mathrm{Im} \ \phi$.
 > > > Wówczas $\phi_1$ i $\phi_2$ są funkcjonałami rzeczywistymi i $\phi_1(ix) = - \phi_2(x)$.
 > > 
 > > $$ \phi(x) = \phi_1(x) + i\phi_2(x) $$
 > > $$ \phi_1(x) \leq |\phi(x)| \leq p(x) $$
 > > Z tw. H-B (wersja rzeczywista) - istnieje $\Phi_1$ rozszerzenie rzeczywiste $\phi_1$ takie, że $\Phi_1(x) \leq p(x)$.
 > > Niech $\Phi_2(x) = - \Phi_1(ix)$. $\Phi_2$ też jest funkcjonałem rzeczywistym i z lematu:
 > > $\Phi(x) = \Phi_1(x) + i\Phi_2(x)$ jest funkcjonałem zespolonym.
 > >
 > > Niech $x \in X$. Istnieje $\alpha \in \mathbb C, |\alpha| = 1$, że 
 > > $\alpha \Phi(x) \in \mathbb R^+$:
 > > 
 > > $$0 \leq \alpha \Phi(x) = \Phi(\alpha x) = $$
 > > $$ = \Phi_1(\alpha x) + i \Phi_2(\alpha x) = $$
 > > $$ = \Phi_1(\alpha x) \leq p(\alpha x)$$
 > > 
 > > Więc $\forall x \exists \alpha, |\alpha| = 1 \ |\alpha \Phi(x)| = \alpha \Phi(x) \leq p(x)$.
 > > Ale $|\alpha||\Phi(x)| = |\Phi(x)|$ co kończy dowód kontroli przez $p(x)$.

# Przestrzenie unormowane

 > [!def] Norma
 > Półnorma $p$ nazywamy **normą** na $X$ gdy $p(x) = 0 \iff x = 0$.
 > 
 > Normę oznaczamy przez $x \to ||x||$.

 > [!def] Przestrzeń unormowana
 > $(X, ||\centerdot||)$ nazywamy **przestrzenią unormowaną**.
 > 
 > > [!note] 
 > > $d(x, y) = ||x - y||$ jest metryką na $X$

Mamy własności topologiczne wyrażone przez normę:
 - $B(x,r) = \lbrace y \in X : ||x - y|| < r \rbrace$
 - $U$ - otwarty $\iff (\forall x \in U) (\exists r > 0) ( B(x,r) \subset U )$
 - $x \in \mathrm{Int} \ U \iff (\exists r > 0) ( B(x,r) \subset U )$
 - $U$ - domknięty $\iff X \setminus U$ - otwarty
itd...

 > [!def] Zbieżność w normie
 > $x_n \in X$ zbiega do $x \in X$ gdy: 
 > $$\lim_{n\to\infty} ||x_n - x|| = 0$$
 > Ozn. $x_n \to x$
 > 
 > > [!note]
 > > $x_n \to x \implies ||x_n|| \to ||x||$

 > [!def] Przestrzeń Banacha 
 > Przestrzeń unormowana nazywa się **przestrzenią Banacha** gdy jest zupełna, czyli każdy ciąg Cauchy'ego jest zbieżny:
 > $$ \lbrace x_n \rbrace _{n \in \mathbb N} - \mathrm{cauchy'ego} \implies (\exists x \in X) (x_n \to x)$$

Przykłady przestrzeni Banacha:
 - $\mathbb K^n$ z normą $||x|| = \sqrt{(\sum_{j=1}^\infty |x_j|^2}$
 - $l^1 = l^1(\mathbb N)$ - przestrzeń ciągów $\{x_n\}$ takich, że $\sum_{j=1}^\infty |x_j| < \infty$ z normą $||x|| = \sum_{j=1}^\infty |x_j|$
 - $l^\infty$ - przestrzeń ciągów ograniczonych z normą $||x|| = \sup_j |x_j|$
 - $c_0$ - przestrzeń ciągów o granicy 0 z normą $||x|| = \sup_j |x_j|$
 - $c_\infty$ - przestrzeń ciągów zbieżnych z normą $||x|| = \sup_j |x_j|$
 - $C([0,1])$ z normą supremum (zbieżności jednostajnej) $||f|| = \sup_{x \in [0,1]} |f(x)|$

 > [!tw] Twierdzenie
 > Każdą przestrzeń unormowaną można uzupełnić do przestrzeni Banacha.
 >
 > Jeśli $(X, ||\centerdot||)$ - p. unormowana to istnieje jedyne (z dokładnością do izomorfizmu) $(\mathbb X, ||\centerdot||_{\mathbb X})$ takie, że 
 > $X \subset \mathbb X, ||x|| = ||x||_\mathbb X$ dla $x \in X$, $X$ jest gęsty w $\mathbb X$.

Przykład przestrzeni unormowanej, niezupełnej:
$C([0,1])$ z normą $||f|| = \int_0^1 |f(x)|dx$
