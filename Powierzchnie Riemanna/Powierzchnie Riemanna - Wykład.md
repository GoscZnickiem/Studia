AGCo jest dziedziną funkcji holomorficznej?

# Definicje Powierzchni Riemanna

## Topologiczne klejenie dziedzin

Dziedzina $\sqrt{z}$:
"dwuwartościowa funkcja holomorficzna na $\mathbb C ^ \times = \mathbb C \setminus \{0\}$"

Można ją opisać przy pomocy dwóch kopii $\mathbb C ^ \times$:

 > [!todo] rysunek

Aby uniknąć sprzeczności rozcinamy je wzdłuż osi $\mathbb R_-$:

 > [!todo] rysunek

Po sklejeniu odpowiednich części otrzymujemy $\Sigma$ - powierzchnia Riemanna funkcji $\sqrt z$, dwukrotnie pokrywającą $\mathbb C ^ \times$.
Na $\Sigma$ funkcja $\sqrt z$ jest jednoznaczną funkcją holomorficzną.

 > [!fakt] 
 > Niech $p : \mathbb C^2 \to \mathbb C$ będzie holomorficzna.
 > Niech $\Sigma = \lbrace (x,y) \in \mathbb C^2 \vert p(x,y) = 0 \rbrace$.
 > 
 > Załóżmy, że $\forall (x_0, y_0) \in \Sigma$:
 > $$p_x(x_0, y_0) = \frac{\partial p}{\partial x} (x_0, y_0) \neq 0$$ lub
 > $$p_y(x_0, y_0) = \frac{\partial p}{\partial y} (x_0, y_0) \neq 0$$
 > 
 > Wtedy w otoczeniu $D_1 \times D_2$ każdego $(x_0, y_0) \in \Sigma$ powierzchnia $\Sigma$ jest wykresem funkcji holomorficznej.
 > $$\Sigma \cap (D_1 \times D_2) = 
 > \lbrace (x, f(x)) \vert x \in D_1 \rbrace, \ f : D_1 \to D_2 \ \mathrm{holo}$$
 > lub
 > $$\Sigma \cap (D_1 \times D_2) = 
 > \lbrace (g(y), y) \vert y \in D_2 \rbrace, \ g : D_2 \to D_1 \ \mathrm{holo}$$
 > > [!dowód]
 > > Zał. $p_x(x_0, y_0) \neq 0$. 
 > > Wybieramy mały dysk $D_2$ wokół $y_0$, tak aby $(x_0, y_0)$ był jedynym miejscem zerowym $p$ w $\{x\} \times D_2$.
 > > Wtedy
 > > $$ \frac{1}{2\pi i}
 > > \oint_{\partial D_2} \frac{p_y(x_0,y)}{p(x_0,y)} dy
 > > = 1 $$
 > > Bo powyższe wyrażenie zlicza liczbę miejsc zerowych wewnątrz $D_2$. 
 > > Z holomorficzności $p$ wiemy, że powyższa całka jest sparametryzowana w sposób ciągły przez $x_0$ na jego małym otoczeniu $D_1$.
 > > Funkcja ciągła przyjmująca wartości całkowite musi być stała więc na całym obszarze $D_1 \times D_2$ powyższe wyrażenie przyjmuje wartość 1.
 > > Stąd:
 > > $$ \forall x \in D_1 \quad \frac{1}{2\pi i}
 > > \oint_{\partial D_2} \frac{p_y(x,y)}{p(x_0,y)} dy
 > > = 1 $$
 > > tzn. w $\{x\} \times D_2$ funkcja $p$ ma jedno zero dane wzorem:
 > > $$ f(x) = \frac{1}{2\pi i}
 > > \oint_{\partial D_2} \frac{yp_y(x,y)}{p(x_0,y)} dy $$
 > > Co kończy dowód.

W sytuacji z powyższego faktu: kiedy uznamy $F : \Sigma \to \mathbb C$ za holomorficzną?
$F$ jest holomorficzna w otoczeniu $(x_0, y_0) \in \Sigma$ jeśli $x \xmapsto{F_1} F(x,f(x))$ lub $y \xmapsto{F_2} F(g(y),y)$
jest holomorficzna w otoczeniu $x_0$ lub odpowiednio $y_0$.
Jeśli obie pochodne są różne od zera to obie funkcje są koniecznie holomorficzne:

 > [!todo] dowód przez rysunek

$$F_1 = F_2 \circ f, \quad F_2 = F_1 \circ g$$

 > [!def] Powierchnia Riemanna
 > **Powierzchnią Riemanna** nazywamy topologiczną przestrzeń Hausdorffa $\Sigma$
 > wyposażoną w rodzinę map $(U_\alpha, \varphi_\alpha)$ taką, że:
 >  - $\bigcup U_\alpha = \Sigma$
 >  - $U_\alpha otwarty w \Sigma$
 >  - $\varphi_\alpha : U_\alpha \to V_\alpha$ - homeomorfizm na pewnym otwartym $V_\alpha \subseteq \mathbb C$
 >  - $\varphi_\alpha \circ \varphi_\beta^{-1}$ są holomorficzne na swoich dziedzinach

$\Sigma$ z wcześniejszego faktu jest powierzchnią Riemanna.

 > [!def] Funkcja holomorficzna na powierzchni Riemanna
 > - $\Sigma$ - powierzchnia Riemanna,
 > $U \subseteq \Sigma$ otwarty.
 > Niech $f : U \to \mathbb C$.
 > Mówimy, że f jest **holomorficzna** ($f \in \mathcal O (U)$) jeśli $f \circ \varphi_\alpha^{-1}$ jest holomorficzna.
 > - $\Sigma_1, \Sigma_2$ - powierzchnie Riemanna,
 > $U \subseteq \Sigma_1$ otwarty.
 > Niech $f : U \to \mathbb C$.
 > Mówimy, że f jest **holomorficzna** ($f \in \mathcal O (U)$) jeśli 
 > $\forall \mathrm{mapy} (W_\beta, \varphi_\beta) na $\Sigma_2$
 > funkcja $\varphi_\beta \circ f$ jest holomorficzna.
 > (tzn. $\varphi_\beta \circ f \circ \varphi_\alpha$ jest holomorficzna)

Przykłady:
 - $\Sigma = Z(y^2 - x) = \lbrace (x,y) \in \mathbb C^2 \ \vert \ y^2 - x = 0 \rbrace$
 - $\Sigma = Z(y^2 - p(x))$ gdzie $p(x)$ jest wielomianem o pojedynczych pierwiastkach. (Powierzchnia hipereliptycza)

## Ilorazy

$\mathbb C / \mathbb Z [i] \quad$ ($z \sim w \iff z - w \in \mathbb Z[i]$)
Jest torusem jako przestrzeń topologiczna.
 > [!todo] obrazek
$\mathbb C \ni z = x + iy \longmapsto (e^{2\pi i x}, e^{2\pi i y}) \in S_1 \times S_1$

Podobnie: Jeśli $z_1, z_2 \in \mathbb C$ są lnz nad $\mathbb R$ to definiujemy kratę $\Lambda = \mathbb Z z_1 \times \mathbb Z z_2$.
$\mathbb C / \Lambda$ też ma strukturę powierzchni Riemanna i też jest topologicznie torusem.

## Kiełki i kontynuacja analityczna

 > [!def] Kiełek
 > Niech $z_0 \in \mathbb C$. Na parach $(U, f)$,
 > gdzie $z_o \ni U \subseteq \mathbb C$ otwarty,
 > $f \in \mathcal O (U)$ wprowadzamy relację równoważności $\sim_{z_0}$:
 > $$ (U,f) \sim_{z_0} (V, g) \iff
 > \exists \mathrm{otw.} W \subseteq U \cap V,
 > z_0 \in W, f \vert_W = g \vert_W$$
 > Czyli w klasach abstrakcji tej relacji znajdują się pary, które w pewnym otoczeniu $z_0$ mają zgodne wartości funkcji.
 > **Kiełkami** nazywamy klasy abstrakcji tejże relacji i oznaczamy je $\underline{f}_{z_0}$.

 > [!def] Przestrzeń Kiełków funkcji holomorficznych
 > Oznaczamy $\mathcal O _ \mathbb C$.
 > 
 > Dla $(U,f)$ określamy podzbiór $\mathcal O_ \mathbb C$:
 > $$O(U, f) = \lbrace \underline{f}_{z} \vert z \in U \rbrace$$
 > Zbiory te określają bazę topologii na $\mathcal O _ \mathbb C$ która jest Hausdorffa.
 > 
 > Rzut $\mathcal O _ \mathbb C \ni \underline f_z \longmapsto z \in \mathbb C$ jest lokalnym homeomorfizmem.

 > [!def] Powierzchnia Riemanna
 > Składową spójną $\mathcal O _ \mathbb C$ zawierającą $O(U, f)$ to **powierzchnia Riemanna** funkcji f.

# $\mathbb C P^2$

Wiemy, że $\underset{wielomian}{p(x,y)} = 0 \rightarrow Z(p) = \Sigma \subseteq \mathbb C^2$

 > [!def] $\mathbb C P^2$
 > **$\mathbb C P^2$** nazywamy przestrzeń prostych:
 > $$ \mathbb C^2 \subset \mathbb CP^2 = 
 > \lbrace l \ \vert \ l < \mathbb C^3, dim_\mathbb C l = 1 \rbrace =
 > \lbrace [x:y:z] \ \vert \ x,y,z \in \mathbb C, \text{nie wszystkie} = 0 \rbrace $$
 > gdzie $[x:y:z]$ to klasa równoważności trójki $(x,y,z)$ względem relacji proporcjonalności.

W $\mathbb CP^2$ są 3 standardowe kopie $\mathbb C^2$:
 - $[x:y:1]$
 - $[x:1:z]$
 - $[1:y:z]$

$p(x,y) = \sum a_{ij}x^iy^j$
$$ Z(p) = \lbrace (x,y) \in \mathbb C^2 \ \vert \ \sum a_{ij}x^iy^j = 0 \rbrace = $$
$$ = \lbrace [x:y:1] \in \mathbb CP^2 \ \vert \ \sum a_{ij}x^iy^j = 0 \rbrace \subset $$
$$ \subset \lbrace [x:y:z] \in \mathbb CP^2 \ \vert \ \sum a_{ij}x^iy^jz^{d-i-j} = 0, \text{gdzie } d = \deg{p} \rbrace$$
