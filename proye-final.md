# Final de proyectiva.

> **El examen final de la materia** constará de 5 preguntas/demostraciones de los temas dados en clase, específicamente los que se encuentran en las notas del profesor colgadas en el campus de la materia, a saber:
> 1) Notas de clasificación de cuádricas (con la excepción de la demostración de la Ley de inercia de Sylvester).
> 2) Notas de Geometría Proyectiva axiomática (con la excepción de la demostración del Teo fundamental de la geometría proyectiva).
> 3) Notas de Curvas y Superficies (Capítulos 1 al 6 inclusive).

## Cuádricas.

Dada una transformación bilineal entre $k$-espacios vectoriales si pedimos aparte que sea de la pinta,
$$
\beta: V \times V \to W
$$
luego la función de una variable $Q: V \to W$ definida como $Q(v)=\beta(v,v)$ es el <u>operador cuadrático</u> a $\beta$. A su vez notemos que es <u>homogéneo de grado 2</u> donde esto quiere decir que saca escalares de grado 2 para afuera,
$$
Q(\lambda v) = \lambda^2v
$$

### Polarización.

Dada un operador cuadrático $Q$ tenemos ciertas fórmulas que en cierta manera nos 'miden' que tan simétrica es nuestro operador bilineal inicial.
![image-20210412031123866](/home/emi/.config/Typora/typora-user-images/image-20210412031123866.png)

luego podemos ver que $\beta_0$ es simétrica y que aparte $\beta_0 = \beta$ si $\beta$ ya lo era. 

Un corolario simpático de estas identidades es que para $\beta = || - ||$ tenemos la ley del paralelogramo que tan poco simpática es de demostrar.

### Datos importantes.

**Ecuación en el plano afín.** Vale que 
$$
Q(x) = Q(a) + 2\beta_a(x-a) + Q(x-a)
$$
para toda cuadrática $Q$ y su forma bilineal simétrica asociada $\beta$.

### Funciones cuadráticas.

Una función cuadrática es una función del estilo
$$
F(x)=Q(x) + 2\phi(x) + k
$$
donde $Q(x)$ es cuádrica, $\phi(x)$ es un morfismo del dual del espacio vectorial y $k$ es una constante.

Una manera de pensar esta forma cuadrática es que está centrada en un punto $a$ tal que en ese punto se escribe de la siguiente manera,
$$
F(x) = Q(x-a) + \phi_a(x-a) + F(a)
$$
donde $\phi_a(x)=\beta_a(x)+\phi(x)$. Esta escritura es la <u>expresión afín</u> de nuestra cuádrica.

Algunas definiciones importantes,

* Un <u>centro</u> de una cuádrica es un $c \in V$ tal que $\phi_c = 0$.
* Un <u>punto singular</u> es un punto tal que es un centro y aparte $F(c)=0$.
* Los puntos <u>regulares</u> son los no singulares.
* Un <u>vértice</u> es un punto donde $\nabla F(v) \neq 0$ para $v \in C$.
* La simetría al rededor de $c$ es la transformación afín $\sigma_c(x)=-x+2c$.

Algunos datos bastante útiles

* Si tenemos un producto interno entonces nuestra cuádrica tiene la siguiente forma,
  $$
  F(x) = (Tx, x) \ + 2(b,x)  \ + k
  $$
  para alguna t.l autoadjunta $T$, algún vector $b$ de Riesz.

* Vale la sig igualdad, 
  $DF_p = \nabla F(p) = 2(Tp+b)$.

* Si $g$ es una t.l afín luego vale la siguiente igualdad,
  ![image-20210418215715721](/home/emi/.config/Typora/typora-user-images/image-20210418215715721.png)

* Descomponemos al vector $b = a + Tz_0$ y vemos que $a=0$ sii $C$ tiene un centro.

* Un punto $v$ es un centro sii
  ![image-20210418220806047](/home/emi/.config/Typora/typora-user-images/image-20210418220806047.png)

**Teorema.** Son equivalentes las siguientes afirmaciones.

1.  La cuádrica $C$ está contenida adentro de una variedad afín propia.
2.  Todos los puntos son singulares.
3.  Para cada punto $p \in C$ podemos escribir $C = \ker \beta + p$.
   *Demo.*
   * 1 $\rightarrow$ 2.  Supongamos que $v$ no es singular. La idea es llegar a una contradicción. Miramos la cuádrica centrada en $v$. Sea $z \notin C_Q  \cup S \ \cup \ker \phi_v $ que existe porque son subespacios propios y porque supusimos que v no es centro. Vemos que para $\lambda=\frac{-2\phi_v(z)}{Q(z)}$ vale que $F(v+\lambda z)=0.$ Contradicción.
   * 2 $\rightarrow$ 3. Ver las dos contenciones.
     * $(\subseteq)$ Para cada $v \in C$ vale que $\beta_{v-p} = 0$.
     * $(\supseteq)$ Miramos la cuádrica centrada en $p$ y hacemos la cuenta qué queremos ver.
   * 3 $\rightarrow$ 1. Esto es evidente dado que  $\ker \beta = V$ por la definición de la cuádrica que nos pide que $Q \neq 0$. De esta manera es una variedad afín propia.

**Teorema.** Un punto $c \in C$ es centro sii $\sigma_c(C)=C$.
*Demo.*

* Ida. Hacer la cuenta.
* Vuelta. El caso que está contenido en una variedad afín propia es por el teorema anterior. En el otro caso igualando $F(x)=F(\sigma_c(x))=0$ nos queda que 
  $\phi_c(c-x)=0$
   para todo los $x \in C$. Supongamos que no es así para todo el espacio! Entonces debe haber una base $\{v_i\}$ tal que vale lo de arriba caso contrario $C$ estaría contenido en una variedad afín sobre los primeros que no se anula.

**Teorema.** Una cuádrica $C$ tiene centro sii no tiene vértice.
*Demo.* La idea es usar el sistema de ecuaciones que definen $a,b$ y usar la equivalencia de $a \neq 0$ para ver si tiene un centro.

* La ida es mirar (d1).
* La vuelta es mirar ambas ecuaciones. Dado que $a \neq 0$ luego resulta que ambas ecuaciones definen soluciones. Si no tuvieran intersección como variedades afines quiere decir que como subespacios lineales el hiperplano contiene al otro subespacio. Como $a$ cumple la ec homogenea de (d1) entonces llegamos a un absurdo con (d2).

### Clasificación normal euclídea de cuádricas sobre los reales.

Toda cuádrica es equivalente a alguna de estas dos flias de cuádricas para distintos autovalores.

1. ![image-20210418222449012](/home/emi/.config/Typora/typora-user-images/image-20210418222449012.png)
   Para una cuádrica con centro. Donde $\mu=0$ si es singular o $\mu=1$ si es regular. Es equivalente por el isomorfismo ortogonal afín $g(x)=Ux + c$ para $c$ un centro.

2. ![image-20210418222458683](/home/emi/.config/Typora/typora-user-images/image-20210418222458683.png)

   Para una cuádrica sin centros. La cuádrica es equiv por un isomorfismo ortogonal afín dado por $g(x)=Ux + v$ para $v$ un vértice.

   *Demo.*

   1. Si tiene centro entonces la llevamos a la escritura $F(x) = Q(x-c) + \mu$. Consideremos una base $\{ v_i \}$ que diagonaliza a $T$ y sea $U$ la t.l ortogonal que lleva la base canónica a la base de autovectores. Esta nos sirve.
   2. Si no tiene centro entonces tiene un vértice $v$. El espacio $\{ \nabla F(v) \}^\perp$ es dejado fijo por $T$ luego tiene una base de autovalores que completamos con $\nabla F(v)$. La $U$ nos la armamos para que mande la base canónica en esta nueva base que nos construimos.

### Clasificación afín.

Toda cuádrica con centro es equivalente por un isomorfismo afín a la cuádrica dada por 
![image-20210418223938320](/home/emi/.config/Typora/typora-user-images/image-20210418223938320.png)
con $p+n \le \dim (V)$.

*Demo.*

* La idea es tomar la clasificiación del teo anterior y ahora componer con la t.l afín $M$ que mande cada autovector a $ \sqrt{\pm \lambda_i}$ dependiendo si es negativa o no el autovalor y para los nulos que los fije. De esta manera obtuvimos una escritura tal como queríamos.

  ## 					Geometría axiomática.

### Plano proyectivo axiomático.

Un plano proyectivo axiomático es un plano que cumple tres axiomas.

1. Dados 4 puntos distintos no hay 3 puntos colineales.
2. Dos rectas se intersecan en un único punto.
3. Dos puntos cualesquiera definen una única recta.

### Anillos ternarios planares.

Es una manera de definirnos un anillo por medio de 5 axiomas.

![image-20210428100903860](/home/emi/.config/Typora/typora-user-images/image-20210428100903860.png)

#### De anillos a planos.

 Consideramos el siguiente conjunto,
![image-20210428132502121](/home/emi/.config/Typora/typora-user-images/image-20210428132502121.png)
notemos que agregamos el punto en el infinito. Por otro lado las rectas son subconjuntos de alguna de las siguientes flias,
![image-20210428132555441](/home/emi/.config/Typora/typora-user-images/image-20210428132555441.png)

![image-20210428132605787](/home/emi/.config/Typora/typora-user-images/image-20210428132605787.png)

donde tenemos las rectas dadas por la operación $T$, las pendientes posibles y finalmente las rectas con 'pendiente $\infty$'. 

#### De planos a anillos.

La construcción más grosa es la que nos permite pasar de un plano axiomático $P$ a un anillo ternario $R$. Para eso necesitamos 4 puntos en el plano y vamos a identificar a las rectas de este plano con elementos del anillo. 
![image-20210428100219148](/home/emi/.config/Typora/typora-user-images/image-20210428100219148.png)

* **Elementos de R.** Son todas las rectas que pasan por A menos la recta AB.
* **El 0**. Es la recta AO.
* **El 1.** Es la recta AE.
* **Identificación.** Toda recta que pasa por B y corta a OE en algún punto C la identificamos con la recta AC.
* **Un punto cualesquiera.** Dado $M \notin AB$ cualesquiera consideramos las rectas AM, BM. Estas inducen elementos por las construcciones previas porque AM es un elemento y de BM obtenemos AC que es otro elemento. De esta manera obtenemos un elemento $(r,s) \in R \times R$.
* **Los puntos $m$.** Se corresponden con los puntos en AB. Por lo de antes lo estamos identificando con el par $(1,m)$.
* **Infinito.** Al punto $A$ lo consideramos el punto $\infty$.
* **Operación T.** Dados $x,m,b \in R$.
  * Al punto $b$ lo pensamos como un par $(0,b)$. O sea es una recta que pasa por B.
  * Miramos al punto $(m)$ en la recta AB.
  * Al punto $x$ como es la primer coordenada es una recta que pasa por A.  
  * **Obtenemos y.** Finalmente unimos la recta $(0,b)$ con $(m)$ y nos fijamos donde corta a la recta $x$. Lo corta en el punto $y=T(x,m,b)$. Nos quedamos con este punto que es la recta que pasa por $B$. 

#### Desargues.

#### Pappus.

### Morfismos y funciones que preservan rectas.

Una <u>colineación</u> es una función biyectiva entre planos proyectivos que manda puntos alineados en puntos alineados.

**Lema.** Toda colineción $F$ entre planos proyectivos de dimensión al menos 2 es tal que manda una recta en otra recta de manera biyectiva.

*Demo*.

* Pedimos dimensión 2 para que no estén contenidos en una única recta $\ell $.
* **Idea.** Suponemos que no entonces debe existir un punto $P'$ tal que no está en la recta pero su preimagen sí lo está. Consideramos otro punto $Q$ que no esté en la recta. Hacemos las intersecciones de rectas y nos debería quedar que para todo punto arbitrario está contenido en esta recta. Absurdo.

  ## 							Curvas.



## 							Superficies.

En general vamos a estar pensando siempre en superficies regulares. Esto es que las funciones derivadas con respecto a las dos variables sean continuas y de manera tal que su producto vectorial sea nunca nulo. Esta idea geométrica tiene sentido para poder pensar en planos tangentes puesto que sino las derivadas serían colineales y no tendríamos plano. Es *fundamental* tener el plano tangente en todo lo que sigue.

#### Propiedades útiles de superficies regulares.

* Toda <u>superficie regular</u> se puede pensar como el gráfico de una función de clase $C^1$.
  
* **Demo.** Al ser regular algún menor de $D\phi$ es no nulo. Supongamos que el de $(x(u,v),y(u,v))$. Mapeamos al abierto en $\R ^2$ dado por estas dos coordenadas. Es un difeomorfismo entonces tomamos la nueva parametrización componiendo con la inversa.
  
* **Qué dice.** Las parametrizaciones regulares son funciones abiertas. ![image-20210527200205351](/home/emi/.config/Typora/typora-user-images/image-20210527200205351.png)

  * **Demo.** Es el gráfico de una función de clase $C^1$ entonces dada una bola $B \subset U$ podemos tomar al abierto $W = \pi^{-1}(B \times \{0\})$.

* El espacio tangente son velocidades de curvas.
  ![image-20210527205311672](/home/emi/.config/Typora/typora-user-images/image-20210527205311672.png)

  * **Demo.** Sea $v$ vector del tangente que queremos ver que es la velocidad de una curva. Como está en el rango del diferencial existe un $w$ en la preimagen. Tomamos la curva en $U$ dada por $X + tw$ para $t$ def donde podemos.

* Propiedades útiles.
  ![image-20210527232628106](/home/emi/.config/Typora/typora-user-images/image-20210527232628106.png)

  ![image-20210527232645910](/home/emi/.config/Typora/typora-user-images/image-20210527232645910.png)

  * **Sol.** Usamos la def!

  ![image-20210527234817841](/home/emi/.config/Typora/typora-user-images/image-20210527234817841.png)

  * **Sol.** Por el ítem anterior tenemos que solo depende de la curva en $S$ y como el espacio tangente queda definido por las curvas tenemos la igualdad.

  ![image-20210528000927411](/home/emi/.config/Typora/typora-user-images/image-20210528000927411.png)
  * **Ida.** Usamos el teorema de la función inversa componiendo con las parametrizaciones regulares. En definitiva nos dice que esta composición es localmente inversible y que es de clase $C^1$.
  * **Vuelta.** Similarmente usamos el teorema de la función inversa y en este caso nos queda que la composición tiene diferencial inversible por lo que  $f^{-1}$ lo tiene también.

  ![image-20210528001305887](/home/emi/.config/Typora/typora-user-images/image-20210528001305887.png)

  * **Sol.** Localmente es un difeomorfismo por lo que en particular es una parametrización regular pre-componiendo con $\varphi$.

#### Integrales de superficies.

Acá tenemos los mismos resultados que teníamos para análisis 2. El resultado obvio es que no dependemos de la parametrización elegida.

![image-20210605023924622](/home/emi/.config/Typora/typora-user-images/image-20210605023924622.png)

* **Demo.** Tenemos un difeomorfismo entre los dominios de las dos parametrizaciones. Por el teorema del cambio de variables obtenemos las dos integrales con dominios distintos. La idea es considerar la función
  ![image-20210605024156797](/home/emi/.config/Typora/typora-user-images/image-20210605024156797.png)
  Ahora usando la fórmula del cambio de variables obtenemos que la primer parte nos queda lo que queríamos mientras que la parte del producto vectorial la hacemos aparecer calculando las diferenciales y multiplicando por sus traspuestas para después tomar el determinante. Después acomodamos lo que nos queda.



## Geodésicas y función exponencial.

![image-20210611013400262](/home/emi/.config/Typora/typora-user-images/image-20210611013400262.png)

* **Demo.** 
  1. Miramos la función $f(t)= || \alpha^. (t)||$ y vemos que su derivada es cero.
  2. Vemos que ambas cumplen la condición inicial para las geodésicas. 
  3. Ver que la diferencial en $0$ es un isomorfismo luego por el teorema de la función inversa se sigue.

![image-20210611014235102](/home/emi/.config/Typora/typora-user-images/image-20210611014235102.png)

* **Demo.** Como está parametrizada por longitud de arco tenemos que $\alpha^{..} \perp \alpha^.$ luego dar una base del plano $\Pi$ y de ahí obtenemos que es una geodésica. La vuelta sale de que $\alpha$ es un multiplo de la normal.



**Ejercicio.**

![image-20210611014321118](/home/emi/.config/Typora/typora-user-images/image-20210611014321118.png)

* **Solución.** La idea es mirar la parametrización en estos casos y notar que lo que esos planos nos dicen los podemos dar en forma general para todos estos casos. 

![image-20210611014352811](/home/emi/.config/Typora/typora-user-images/image-20210611014352811.png)

* **Demo.** Una desigualdad la tenemos siempre porque toda curva es menor que una linea recta. Para encontrar la constante usamos que tomando una bola más chica si es necesario podemos ver que la clausura al ser un compacto tiene una cota en la norma del gradiente. Miramos la curva que une estos dos puntos y calculamos su longitud y de ahí obtenemos la cota.
  * $||\nabla f|| < K$ está acotado en un compacto. La idea es medio usar el teo del valor medio para que controlar la derivada y después integrando nos queda regio.

![image-20210611014414960](/home/emi/.config/Typora/typora-user-images/image-20210611014414960.png)

* **Demo.**  Nos construímos la variación tal que en cada punto $\alpha(t)$ tenga velocidad $\mu(t)$. Elegimos $s$ para que tenga sentido usando la compacidad de la curva. Después hacemos la cuenta. En particular si los extremos están fijos por la construcción tenemos que $\alpha_1(t), \alpha_0(t)$ son la geodésica constante.

![image-20210611014431679](/home/emi/.config/Typora/typora-user-images/image-20210611014431679.png)

* **Demo.** Hacemos la cuenta de la derivada metiendo adentro de la integral la derivada con respecto a $s$. Luego usamos los datos que tenemos e integración por partes para pasar la derivada a $\alpha$. Es importante notar que es por extremos fijos entonces el campo vale $0$ en los extremos! Para ver la ultima cuenta metemos el proyector en el lado derecho y usamos sus propiedades.

![image-20210611014451122](/home/emi/.config/Typora/typora-user-images/image-20210611014451122.png)

* **Demo.** Es una consecuencia de la formula de la primer variación. Notemos que ser minimizante es que $f'(0)=0$ porque justamente minimiza. Haciendo esta cuenta llegamos a lo que queríamos.
  * Un detalle importante es primero considerar el campo de aceleraciones de nuestra curva con extremos fijos para luego tomar la variación de este campo. Recordemos que tenemos *libertad* de elegir nuestro campo en este caso.

![image-20210611014509206](/home/emi/.config/Typora/typora-user-images/image-20210611014509206.png)

* **Demo.** Consideramos una variación medio loca loca pero después es hacer cuentas y darse cuenta que todo está bien :) 
  * La variación que tomamos es justamente la exponencial en p evaluada en $t(v+sw)$ pidiendo de antemano que lo que multiplicamos por $t$ esté dentro del dominio. 
  * Calculamos la derivada de $\alpha_s$ definida anteriormente. Como es una geodésica es constante por lo que nos da lo mismo que en $t=0$. En tal caso nos queda $||v+sw||^2$ y **usando pitágoras hacemos aparecer** $\langle v, w \rangle$. 
  * Derivamos la identidad recién obtenida pero ahora con respecto a $s$ *hojaldre* e intercambiamos las derivadas con respecto a las dos variables y llegamos  a que $\langle \mu^{.}, \gamma^{.} \rangle = \langle v,w \rangle$.
  * Como en las otras demos queremos pasar la derivada para el otro lado. Consideramos $f(t) = \langle \mu(t), \dot\gamma(t) \rangle$  tal que su derivada nos da $\langle v, w \rangle$ y concluimos que es lineal y que vale exactamente $f(t)=t \langle v, w \rangle.$ Evaluamos en $1$ e interpretamos lo que realmente es $f$ en términos de la diferencial de la exponencial y estamos.

![image-20210611014531227](/home/emi/.config/Typora/typora-user-images/image-20210611014531227.png)

* **Demo.** Cuentita pero usamos la definición de la param polar y de la derivada de $\gamma$ acá. Nos quedan dos términos positivos usando pitagoras porque el producto interno se muere. De los dos términos nos quedamos con el que está multiplicado por $|\dot r|$. Luego vemos que la diferencial que lo acompaña justamente tiene norma 1. 

![image-20210611014545510](/home/emi/.config/Typora/typora-user-images/image-20210611014545510.png)

* **Demo.** 
  1. Si se sale tomamos el intervalo donde queda dentro del abierto normal. Tomamos una sucesión que se va yendo luego usando el lema anterior podemos acotar la diferencia de $r$ en estos puntos menos $r$ en $a + \delta$. De esto obtenemos la cota porque por medio de $r$ hacemos aparecer a $R$ y por el lema anterior la integral de $||\dot \alpha||$.
     1. Consideramos $a + \delta$ para que nos quede bien el radio :) porque $r(a+\delta) \to 0$.
  2. Como la geodésica tiene norma la velocidad que está en el dominio usando lo anterior tenemos la desigualdad que queríamos. 
  3. **Estuve un tiempo trabado con esto pero es una boludez al final igual debo prestar mucha atención**. La idea es volver al lema anterior y usar la cota que teníamos antes para el radio suponiendo que $||\dot \gamma|| = ||\dot \alpha||$ . En el caso anterior separamos en dos partes después de usar pitagoras. Ahora nos quedó que la desigualdad es una igualdad por lo que el otro término vale $0$. Esto nos dice que $\dot u(t) = 0$ luego nos queda que la curva $\alpha(t)$ es una reparametrización de la geodésica que pasa por los dos puntos porque en definitiva la curva en el dominio es una recta del estilo $r(t)u_0$. 