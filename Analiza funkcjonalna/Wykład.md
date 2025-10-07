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
 > *Note*: jeśli $K$ jest pochłaniający to $0 \in K$

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
 > jest zbiorem wypukłym i pochłaniającym. Ponadto $p(x) = p_K(x)$

# Twierdzenie Hahna-Banacha 

 > [!def] Funkcjonał liniowy
 > **Funkcjonałem liniowym** nazywamy odwzorowanie liniowe $\phi : X \to \mathbb K$

 > [!tw] Twierdzenie Hahna-Banacha (wersja rzeczywista)
 > Niech $p : X \to [0, \infty]$ będzie funkcjonałem Minkowskiego oraz $X_0 \subset X$.
 > Załóżmy, że $\phi : X_0 \to \mathbb R$ jest funkcjonałem liniowym takim, że 
 > $$ (\forall x \in X_0) (\phi(x) \leq p(x)) $$
 > Istnieje wówczas funkcjonał liniowy $\psi : X \to \mathbb R$ taki, że:
 >  1. $(\forall x \in X_0) (\psi(x) = \phi(x))$
 >  2. $(\forall x \in X) (\psi(x) \leq p(x))$
 >
 > Czyli funkcjonał $\phi$ można przedłużyć na całą przestrzeń, z zachowaniem kontroli przez $p(x)$.
