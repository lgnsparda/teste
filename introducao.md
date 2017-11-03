# Introdução

## Conceito de Fluido
O que é fluido?

Sob um conceito molecular, líquidos e gases são fluidos e sólidos não o são.

A matéria arranja-se de diversas formas quanto à vinculação e disponibilidade de movimentação relativa entre as moléculas. No estado sólido, o movimento relativo entre as moléculas (sempre presente) é tal que o arranjo topológico não varia. Ou seja, sua vizinhança é invariante. Certamente esse conceito não prevê fenômenos tais como fratura ou fusão do material.

Nos líquidos, as moléculas do material estão livres para se movimentar umas em relação a outras, mesmo que a relação entre vizinhanças seja alterada. Nesse tipo de material as forças de caráter eletromagnético de atração prevalecem sobre as forças relativas ao estado material de agitação térmica (browniano) das moléculas constituintes do líquido em questão. Em geral, os líquidos comportam-se mecanicamente de forma tal que seu volume, sob determinadas condições, será relativamente invariante no sentido que não ocupam completamente o volume do recipiente que contém o material, desde que este recipiente seja maior do que o volume do líquido. Em outras palavras, o volume é uma propriedade do sistema de partículas do fluido.

Para os gases ou vapores, a agitação térmica é capaz de vencer a ação coesiva das forças eletromagnéticas e as moléculas estão livres para se movimentar, descrevendo uma trajetória browniana ilimitada (caso não haja fronteiras) ou limitada apenas pelas paredes do recipiente que contém o fluido. Nesse sentido, o volume que um gás ocupa é igual ao volume do recipiente que abriga o material, seja gás ou vapor.

Do ponto de vista macroscópíco, diversas diferenças entre gases e líquidos podem ser apontadas:


  - Gases são muito mais compressíveis do que os líquidos;
  - Líquidos apresentam, em geral, massa específica muito maior (uma ordem de magnitude) do que a dos gases;
  - Líquidos podem não se misturar (líquido imiscível), gases não;
  - Como consequência do item 3, superfícies envolvendo interfaces do tipo líquido-líquido ou líquido-gás apresentam tensão superficial. Não há interface do tipo gás-gás, logo neste tipo de "mistura" não há possibilidade de haver tensão superficial.


Além do enfoque molecular (Físico ou físico-químico), outras abordagens mais gerais e abrangentes podem ser usadas para definir o que pode ser considerado um material fluido. Nessas abordagens devem ser considerados fatores como escalas de tempo envolvidas e a relação entre tamanho das partículas constituintes do sistema e as escalas de comprimento típicas do escoamento.


## A Hipótese de Meio Contínuo - Número de Knudsen
\vspace{-6mm}

O conceito de contínuo (ou *continuum*) é meramente uma idealização. Como ressaltamos anteriormente a matéria é composta por moléculas, e, portanto, é um sistema discreto em sua escala elementar. Porém, para grande parte das aplicações práticas, e sobretudo para o campo de interesse da mecânica dos fluidos, os líquidos e gases podem ser considerados como materiais contínuos, ou seja, infinitamente divisíveis, de forma que não há vazios no material. Nesse sentido, a mecânica dos fluidos interessa-se pelo comportamento médio de um conjunto muito (mas muito mesmo!) grande de partículas elementares.

**Exemplo:** Um centímetro cúbico de ar em condições atmosféricas padrão contém cerca de $3 \times 10^{16}$ partículas.

Estamos, portanto, interessados no reflexo médio, de significado estatístico bem definido, de um conjunto de partículas (no sentido duplo da palavra) do material, que permita a definição de propriedades mecânicas e termodinâmicas do fluido:

\begin{figure}[H]
    \centering
    \includegraphics[scale=0.5]{figura11.pdf}
    %\caption{Mapeamentos do Domínio}
    \label{fig11}
\end{figure}

Em geral definimos \underline{massa específica média} como:

$$
\overline{\rho}=\frac{m}{v}
$$

Onde $m$ é a massa total do sistema e $v$ é o volume total do sistema. Deseja-se definir a massa específica como propriedade local. Seria natural lançar mão do conceito de derivada, de forma que:

$$
\rho(\textbf{x})=\lim_{\Delta v \to 0}\frac{\Delta m}{\Delta v}
$$

Em que $\Delta v$ é um volume arbitrário que contém a coordenada $\textbf{x}$ e $\Delta m$ a massa de fluido contida nesse volume. Aqui nos deparamos com um problema: Se o volume for tão pequeno que o trânsito material de moléculas através de suas fronteiras se fizer perceptível ao processo de média estatística, então não faz mais sentido definir massa específica.

\begin{figure}[H]
    \centering
    \includegraphics[scale=0.5]{figura12.pdf}
    %\caption{Mapeamentos do Domínio}
    \label{fig12}
\end{figure}

Em nosso processo de fazer $\Delta v \to 0$, em geral, será possível detectar um tamanho de volume cúbico $\Delta v$ tal que se $\Delta v > \Delta v'$, então as variações afins ao movimento molecular não afetam o valor da razão $\Delta m/\Delta v$. Se essa escala for, por outro lado, muito menor do que a menor escala relevante do problema, i.e., $\Delta v << V$ de maneira que seja possível considerar $\Delta v'$ como "arbitrariamente pequeno", então podemos admitir que o material em estudo é um meio contínuo.

Em outras palavras se a razão entre uma escala típica de movimento microscópico (Para líquidos ou gases, o livre caminho médio) e uma escala típica do problema que desejamos abordar for muito pequeno, então uma abordagem contínua pode ser empregada. À esta razão dá-se o nome de Número de Knudsen, tal que:

$$
Kn=\frac{\lambda}{L}
$$

Se $Kn<<1$ então o meio é contínuo.

**Exemplo:** Escoamento de ar através de um rotor de ventilador doméstico:

  - $L=$ Diâmetro do rotor, cerca de 30 cm.
  - $\lambda=$ Livre caminho médio. Para um gás perfeito, temos da teoria cinética dos gases que:


$$
\lambda=\frac{K_{B} T}{\sqrt{2} \pi \sigma^{2} P}, \hspace{2mm} onde:
$$


  - $K_{B}$: Constante de Boltzmann: $1,38 \times 10^{-23} \hspace{1mm} J/K $
  - $\sigma$: Diâmetro da Partícula: ($N_{2} \sim 3,7$Â, $O_{2} \sim 3,0$Â onde $1$Â= $10^{-10}m$)
  - $P$: Pressão Absoluta;

$$
\lambda \sim \frac{1,4 \times 10^{-23} \cdot 300}{1,14 \times 3,14 \times 9 \times 10^{-20} \cdot 10^{5}} \sim 10^{-7}
$$

Suponhamos $L=30 \hspace{1mm} cm$ ($0,3 \hspace{1mm} m$):

$$
Kn=\frac{10^{-7}}{0,3} \sim 3 \times 10^{-7} \hspace{0.5mm} << 1
$$

De forma que uma abordagem contínua é perfeitamente viável.

## Fluido, Escoamento e Escalas de Tempo: O Número de Deborah


A definição de escoamento está ligada intrinsecamente às escalas de tempo envolvidas. Do ponto de vista mecânico, consideramos que um fluido newtoniano é um material que oferece resistência à _taxa de deformação_, diferentemente de um sólido, que oferece resistência à _deformação_. Em geral estamos habituados a classificar de maneira muito objetiva materiais que escoam e que não escoam (fluidos e não-fluidos). No entanto, é preciso estar atento às escalas de tempo associadas à deformação do material, e as alterações das condições dinâmicas a que se sujeita o material. Outra forma de descrever este conceito seria a seguinte: Quando se aplica uma tensão cisalhante em um sólido, este se deforma em uma quantidade fixa, e quando a aplicação da tensão é interrompida, o sólido interrompe sua deformação. Aplicando a mesma tensão em um fluido, este se deforma a uma taxa, e quando a aplicação da tensão é interrompida, o fluido continua a se deformar segundo esta taxa de deformação, caracterizando um escoamento.

Quando uma porção de água é servida em um copo, é preciso cerca de $10^{-13}$ segundos para que as moléculas do material organizem-se e se acomodem à nova vinculação geométrica. Esse tempo, associado exclusivamente às características do material, é chamado de \underline{tempo de relaxação} do fluido. Quando a água escoa para o copo, o tempo associado do escoamento\footnote{Na verdade estamos nos referindo a um tempo relacionado à mudança das condições de contorno que envolvem o material (No caso, o movimento da jarra que contém a água).} da água é da ordem de milissegundos ($10^{-3}$ segundos) ou mais.

A relação entre esses dois tempos característicos é tal que o ``fluido", ou material, tem muito tempo para se acomodar às novas condições de contorno. Dessa forma, podemos dizer que a razão entre o tempo característico de relaxação do material $t_{relax}$ e o tempo característico de variação das condições de contorno $t_{esc}$ para a água sendo servida em um copo é muito pequena. Define-se assim o número de Deborah como:

\begin{equation}\label{eq17}
De=\frac{t_{relax}}{t_{esc}}
\end{equation}

A origem do número de Deborah, dada pelo professor Markus Reiner, remete à passagem bíblica cantada pela profetisa Débora no livro dos Juízes. Esta passagem encontra-se no capítulo 5, versículo 5:

\textsf{``Os montes escoaram diante do Senhor, e até Sinai, diante do Senhor Deus de Israel."}

Podemos fazer algumas observações sobre a relação entre o número de Deborah e o comportamento do material:

\begin{itemize}
  \item $De \longrightarrow 0$: O material comporta-se como um fluido e, muito provavelmente, como um fluido linear (newtoniano ou newtoniano generalizado);
  \item $De << 1$: O material comporta-se como um fluido;
  \item $De \sim 1$: O material escoa, mas efeitos não-lineares começam a ser importantes, ou já o são! Estes efeitos são associados principalmente a efeitos elásticos no fluido. Ou seja, o material não é puramente fluido ou sólido;
  \item $De \longrightarrow \infty$: O material \underline{pode} se comportar como um fluido. De toda forma, o material fica indiferente às mudanças nas condições de contorno.
\end{itemize}

\section{Notação Indicial}
\vspace{-6mm}

A notação indicial ou notação de Einstein é um método muito útil para a representação de grandezas vetoriais.

Um dado vetor no $\mathbb{R}^3$ é representado na seguinte forma:

\begin{equation}\label{eq18}
\mathbf{v}=(v_{1}, v_{2}, v_{3})=v_{1}\widehat{e}_{1}+v_{2}\widehat{e}_{2}+v_{3}\widehat{e}_{3}
\end{equation}

Onde os vetores base são:

\begin{eqnarray}\label{eq19}
% \nonumber to remove numbering (before each equation)
  \nonumber \widehat{e}_{1} &=& (1,0,0) \\
  \widehat{e}_{2} &=& (0,1,0) \\
  \nonumber \widehat{e}_{3} &=& (0,0,1)
\end{eqnarray}

As propriedades fundamentais dos vetores de base são descritas como:

\begin{description}
  \item[I - Ortogonalidade Mútua:] $\widehat{e}_{1} \cdot \widehat{e}_{2}=\widehat{e}_{2} \cdot \widehat{e}_{3}=\widehat{e}_{3} \cdot \widehat{e}_{1}=0$, onde ``$\cdot$" representa o produto escalar (Que entre vetores, é comutativo);
  \item[II - Base Normal:] $\|\widehat{e}_{1}\|=(\widehat{e}_{1} \cdot \widehat{e}_{1})^{0.5}=1$, valendo o mesmo para $\widehat{e}_{2}$ e $\widehat{e}_{3}$;
  \item[III - Base destrógira:] Segue a regra da mão direita:
  \begin{eqnarray}\label{eq110}
  % \nonumber to remove numbering (before each equation)
    \nonumber \widehat{e}_{1} \times \widehat{e}_{2} &=& \widehat{e}_{3} \\
    \widehat{e}_{2} \times \widehat{e}_{3} &=& \widehat{e}_{1} \\
    \nonumber \widehat{e}_{3} \times \widehat{e}_{1} &=& \widehat{e}_{2}
  \end{eqnarray}
\end{description}

%\setlength{\unitlength}{0.70mm}
%\begin{picture}(1,1)(0,0)
%\thicklines
%\put(50,30){\vector(1,0){20}}
%\put(50,30){\vector(0,1){20}}
%\put(50,30){\vector(-1,-1){10}}
%\put(45,20){$\widehat{e}_{1}$}
%\put(71,26){$\widehat{e}_{2}$}
%\put(53,47){$\widehat{e}_{3}$}
%%\thinlines
%%\put(140,55){\line(1,0){5}}
%%\put(145,50){\line(0,1){5}}
%%\put(140,55){\line(-1,-1){5}}
%%\put(135,50){\line(0,-1){5}}
%%\put(145,50){\line(-1,-1){5}}
%%\put(135,45){\line(1,0){5}}
%\end{picture}

%\pagebreak

Segundo a notação indicial, o vetor $v$ pode ser representado como:

\begin{equation}\label{eq111}
\mathbf{v}=v_{i}\widehat{e}_{i}=\sum_{i=1}^{3}v_{i}\widehat{e}_{i}
\end{equation}

Escreve-se agora as seguintes convenções:

\begin{description}
  \item[Convenção I:] Todos os sufixos variam em uma mesma faixa, de 1 a $n$. No $\mathbb{R}^3$, $n=3$;
  \item[Convenção II:] ``Convenção Soma": Índices repetidos ou mudos indicam um somatório;
\end{description}

\textbf{Exemplos:}
\begin{enumerate}
  \item Representação de um vetor:
  \begin{equation}\label{eq112}
    \mathbf{v}=v_{1}\widehat{e}_{1}+v_{2}\widehat{e}_{2}+v_{3}\widehat{e}_{3}=v_{i}\widehat{e}_{i}\hspace{1mm} ou \hspace{1mm} v_{p}\widehat{e}_{p}
  \end{equation}
  \item Representação de um sistema linear:

  $\left\{
    \begin{array}{ccccccc}
      a_{11}x_{1}&+&a_{12}x_{2}&+&a_{13}x_{3}&=&b_{1} \\
      a_{21}x_{1}&+&a_{22}x_{2}&+&a_{23}x_{3}&=&b_{2} \\
      a_{31}x_{1}&+&a_{32}x_{2}&+&a_{33}x_{3}&=&b_{3}
    \end{array}
  \right.$
  $\longrightarrow$ $a_{ij}x_{j}=b_{i}$\\

  Onde:
  \begin{itemize}
    \item $i$ é o índice livre, que representa a direção (ou equação para este caso);
    \item $j$ é o índice mudo ou repetido, que representa a soma;
    \item \textbf{Regra Básica:} Em um mesmo termo de uma expressão, um índice \textbf{não pode aparecer mais do que duas vezes}.
    \item \textbf{Exemplo:} $a_{ij}b_{j}c_{j}$ não representa uma expressão em notação indicial.
  \end{itemize}

\end{enumerate}

\subsection{O Delta de Kronecker}

\begin{equation}\label{eq113}
\delta_{ij}=\left\{
    \begin{array}{rcl}
      1 , &\mbox{se}&  i=j\\
      0 , &\mbox{se}&  i \neq j\\
    \end{array}
  \right.
\end{equation}

Seu conceito remete a Leopold Kronecker (1823-1891). Duas formas notáveis do delta de Kronecker são dadas por:
\begin{itemize}
  \item Como os vetores de base $\widehat{e}_{1}$, $\widehat{e}_{2}$ e $\widehat{e}_{3}$ são ortonormais, o produto escalar entre eles resultará no próprio delta:
      \begin{equation}\label{eq114}
      \widehat{e}_{i} \cdot \widehat{e}_{j}=\delta_{ij}
      \end{equation}
  \item Considerando que as direções ordenadas $x_{1}$, $x_{2}$ e $x_{3}$ são independentes, tem-se:
      \begin{equation}\label{eq115}
      \frac{\partial x_{i}}{\partial x_{j}}=\delta_{ij}
      \end{equation}
\end{itemize}

Uma propriedade importante do delta de Kronecker é a de contração de índices. Considerando \ref{eq113}, temos que:

\begin{equation}\label{eq116}
a_{ij}\delta_{1j}=a_{i1}\delta_{11}+a_{i2}\delta_{12}+a_{i3}\delta_{13}=a_{i1}
\end{equation}

Observe que o índice $j$ é mudo, pois se repete e denota uma soma. Se este índice se repete com o delta, este sumirá da expressão, e todo índice $j$ é substituído por 1. Desta forma, pode-se escrever de forma análoga:

\begin{eqnarray}\label{eq117}
% \nonumber to remove numbering (before each equation)
  \nonumber a_{ij}\delta_{jp} &=& a_{ip} \\
  \delta_{im}\delta_{mj} &=& \delta_{ij} \\
 \nonumber \delta_{im}\delta_{mj}\delta_{jp} &=& \delta_{ip}
\end{eqnarray}

Com estes resultados, podemos escrever o produto escalar entre vetores:

\begin{equation}\label{eq118}
\mathbf{a} \cdot \mathbf{b}=a_{i}\widehat{e}_{i} \cdot b_{j}\widehat{e}_{j}=a_{i}b_{j}\underbrace{\widehat{e}_{i} \cdot \widehat{e}_{j}}_{\delta_{ij}}=a_{i}b_{j}\delta_{ij}=a_{i}b_{i}=a_{1}b_{1}+a_{2}b_{2}+a_{3}b_{3}
\end{equation}

Aconselha-se a utilização de letras diferentes na inclusão de novos termos. O delta fará todo o resto ao contrair os índices convenientes.

As componentes de um vetor podem ser escritas através do produto escalar com os vetores de base. Logo, seja $\mathbf{u}$ um vetor. Este pode ser escrito como:

\begin{equation}\label{eq119}
\mathbf{u}=\mathbf{u} \cdot \widehat{e}_{1}=u_{i}\widehat{e}_{i} \cdot \widehat{e}_{1}=u_{i}\delta_{i1}=u_{1}
\end{equation}

Utilizando os conceitos apresentados até aqui, podemos representar um sistema linear na forma matricial como:

\begin{equation}\label{eq120}
\mathbf{A} \cdot \mathbf{x} = \mathbf{b} \longrightarrow A_{ij}x_{j}=b_{i}
\end{equation}

Onde $\mathbf{x}$ e $\mathbf{b}$ são vetores. Mas podemos afirmar que $\mathbf{A}$ é um tensor?
Para responder esta pergunta, representaremos a quantidade $\mathbf{A}$ na forma $A_{pq}\widehat{e}_{p}\widehat{e}_{q}$. Note que não há um produto entre $\widehat{e}_{p}$ e $\widehat{e}_{q}$:

\begin{eqnarray}\label{eq121}
% \nonumber to remove numbering (before each equation)
 \nonumber \widehat{e}_{p}\widehat{e}_{q} \longrightarrow \widehat{e}_{1}\widehat{e}_{1}&=&\left[
                                                                      \begin{array}{ccc}
                                                                        1 & 0 & 0 \\
                                                                        0 & 0 & 0 \\
                                                                        0 & 0 & 0 \\
                                                                      \end{array}
                                                                    \right]\\
  \widehat{e}_{1}\widehat{e}_{2}&=&\left[
                                                                      \begin{array}{ccc}
                                                                        0 & 1 & 0 \\
                                                                        0 & 0 & 0 \\
                                                                        0 & 0 & 0 \\
                                                                      \end{array}
                                                                    \right]\\
 \nonumber \widehat{e}_{2}\widehat{e}_{3}&=&\left[
                                                                      \begin{array}{ccc}
                                                                        0 & 0 & 0 \\
                                                                        0 & 0 & 1 \\
                                                                        0 & 0 & 0 \\
                                                                      \end{array}
                                                                    \right]...
\end{eqnarray}

Nesse sentido, observe os índices que representam soma em $A_{pq}\widehat{e}_{p}\widehat{e}_{q}$. Logo:

\begin{equation}\label{eq122}
A_{pq}\widehat{e}_{p}\widehat{e}_{q}=A_{11}\widehat{e}_{1}\widehat{e}_{1}+A_{12}\widehat{e}_{1}\widehat{e}_{2}+A_{13}\widehat{e}_{1}\widehat{e}_{3}
+A_{21}\widehat{e}_{2}\widehat{e}_{1}+...=\left[
                                           \begin{array}{ccc}
                                             A_{11} & A_{12} & A_{13} \\
                                             A_{21} & A_{22} & A_{23} \\
                                             A_{31} & A_{32} & A_{33} \\
                                           \end{array}
                                         \right]
\end{equation}

De fato, $\widehat{e}_{p}\widehat{e}_{q}$ representa uma possível base de um espaço de matrizes de segunda ordem. Para que $\mathbf{A}=A_{pq}\widehat{e}_{p}\widehat{e}_{q}$ seja um tensor de fato é preciso que uma certa regra de transformação ortogonal seja obedecida. Esta regra não será abordada neste texto. No entanto, para nossos propósitos podemos utilizar as regras estabelecidas anteriormente para qualquer quantidade $A_{ij}\widehat{e}_{i}\widehat{e}_{j}$, sendo ela tensorial ou não! Por exemplo, o tensor identidade pode ser escrito como $\mathbf{I}=\delta_{ij}\widehat{e}_{i}\widehat{e}_{j}$. Retornando ao sistema linear (equação \ref{eq120}), temos:

\begin{equation}\label{eq123}
 \underbrace{A_{pq}\widehat{e}_{p}\widehat{e}_{q}}_{\mathbf{A}} \cdot \underbrace{x_{i}\widehat{e}_{i}}_{\mathbf{x}}=\underbrace{b_{j}\widehat{e}_{j}}_{\mathbf{b}}
\end{equation}

\begin{eqnarray}\label{eq124}
% \nonumber to remove numbering (before each equation)
 \nonumber A_{pq}x_{i}\widehat{e}_{p}\underbrace{\widehat{e}_{q} \cdot \widehat{e}_{i}}_{\delta_{qi}} &=& b_{j}\widehat{e}_{j} \\
 \nonumber A_{pq}x_{i}\delta_{qi}\widehat{e}_{p} &=& b_{j}\widehat{e}_{j} \\
 \nonumber A_{pq}\underbrace{x_{i}\delta_{qi}}_{x_{q}}\widehat{e}_{p} &=& b_{j}\widehat{e}_{j} \\
  A_{pq}x_{q}\widehat{e}_{p} &=& b_{j}\widehat{e}_{j}
\end{eqnarray}

Para recuperarmos as equações do sistema original, basta tomar as componentes da equação \ref{eq120} em uma direção unitária $\widehat{e}_{i}$, ou seja:

\begin{eqnarray}\label{eq125}
% \nonumber to remove numbering (before each equation)
  \nonumber A_{pq}x_{q}\widehat{e}_{p} \cdot \widehat{e}_{i} &=& b_{j}\widehat{e}_{j} \cdot \widehat{e}_{i} \\
  A_{pq}x_{q}\delta_{pi} &=& b_{j}\delta_{ji} \\
  \nonumber A_{iq}x_{q} &=& b_{i}
\end{eqnarray}



\subsection{O Permutador de Levi-Civita}

\begin{equation}\label{eq126}
\varepsilon_{ijk}=\left\{
    \begin{array}{rcl}
      1 , &\mbox{para}&  \varepsilon_{123}, \varepsilon_{231}, \varepsilon_{312}\\
      -1 , &\mbox{para}&  \varepsilon_{132}, \varepsilon_{321}, \varepsilon_{213}\\
      0 , &\mbox{para os demais}&
    \end{array}
  \right.
\end{equation}

O permutador de Levi-Civita representa as componentes de um tensor de terceira ordem. Seu conceito remete a Tulio Levi-Civita (1873-1948). Um mecanismo muito prático para a determinação do sinal de $\varepsilon$ é descrito abaixo, onde definimos uma convenção para o sentido de permutação:

\begin{displaymath}
    \xymatrix{
        1 \ar[d]_+ \\
    2 \ar[r]_+ & 3 \ar[lu]_+}
\end{displaymath}

Logo:

\begin{itemize}
  \item No sentido positivo: $\varepsilon_{ijk}=1$;
  \item No sentido negativo: $\varepsilon_{ijk}=-1$;
  \item Para índices repetidos: $\varepsilon_{ijk}=0$;
\end{itemize}

Outra forma:

\begin{equation}\label{eq127}
\varepsilon_{ijk}=\frac{1}{2}(i-j)(j-k)(k-i)
\end{equation}

Utilizando o permutador, podemos escrever o produto vetorial como:

\begin{equation}\label{eq128}
\mathbf{u} \times \mathbf{v}=\left|
                               \begin{array}{ccc}
                                 \widehat{e}_{1} & \widehat{e}_{2} & \widehat{e}_{3} \\
                                 u_{1} & u_{2} & u_{3} \\
                                 v_{1} & v_{2} & v_{3} \\
                               \end{array}
                             \right|=u_{i}\widehat{e}_{i} \times v_{j}\widehat{e}_{j}=u_{i}v_{j}\underbrace{\widehat{e}_{i} \times \widehat{e}_{j}}_{\varepsilon_{ijk}\widehat{e}_{k}}=u_{i}v_{j}\varepsilon_{ijk}\widehat{e}_{k}
\end{equation}

\textbf{Propriedades:}

\begin{enumerate}
  \item $\mathbf{u} \times \mathbf{v}=\mathbf{w}$;\\
  $\mathbf{w}$ é perpendicular a $\mathbf{u}$ e $\mathbf{v}$ simultaneamente;
\setlength{\unitlength}{0.70mm}
\begin{picture}(1,1)(0,0)
\thicklines
\put(10,0){\vector(1,0){20}}
\put(10,0){\vector(0,1){20}}
\put(10,0){\vector(-1,-1){10}}
\put(5,-10){$\mathbf{u}$}
\put(31,-4){$\mathbf{v}$}
\put(13,17){$\mathbf{w}$}
\end{picture}
  \item $\mathbf{u} \times \mathbf{v}=-\mathbf{v} \times \mathbf{u}$\\
Prova:
\begin{equation}\label{eq129}
\nonumber \mathbf{u} \times \mathbf{v}=u_{i}\widehat{e}_{i} \times v_{j}\widehat{e}_{j}=u_{i}v_{j}\varepsilon_{ijk}\widehat{e}_{k}=v_{j}u_{i}\varepsilon_{ijk}\widehat{e}_{k}\underbrace{=}_{\varepsilon_{ijk}=-\varepsilon_{jik}}
-v_{j}u_{i}\underbrace{\varepsilon_{jik}\widehat{e}_{k}}_{\widehat{e}_{j} \times \widehat{e}_{i}}=-\mathbf{v} \times \mathbf{u}
\end{equation}
  \item $\mathbf{u} \times \mathbf{u}=0$\\
Prova: Do item 2, temos que:
\begin{equation}\label{eq130}
\underbrace{\mathbf{u} \times \mathbf{u}}_{\mathbf{a}}=-\underbrace{\mathbf{u} \times \mathbf{u}}_{\mathbf{a}} \Longleftrightarrow \mathbf{a}=0
\end{equation}
\end{enumerate}

Com os conceitos apresentados, podemos definir o operador nabla ($\nabla$) em notação indicial:

\begin{equation}\label{eq131}
\nabla = \left(\frac{\partial}{\partial x_{1}}, \frac{\partial}{\partial x_{2}}, \frac{\partial}{\partial x_{3}} \right)=
\frac{\partial}{\partial x_{i}}\widehat{e}_{i}
\end{equation}

Assim sendo, definem-se:

\begin{itemize}
  \item Gradiente de um escalar:
  \begin{equation}\label{eq132}
 \nonumber   \nabla \phi = \frac{\partial}{\partial x_{i}}\widehat{e}_{i} (\phi) = \frac{\partial \phi}{\partial x_{i}}\widehat{e}_{i}
  \end{equation}
  \item Gradiente de um vetor:
  \begin{equation}\label{eq133}
 \nonumber   \nabla \mathbf{v} = \frac{\partial}{\partial x_{i}}\widehat{e}_{i} (\mathbf{v}) = \frac{\partial}{\partial x_{i}}\widehat{e}_{i}(v_{j}\widehat{e}_{j}) = \frac{\partial v_{j}}{\partial x_{i}}\widehat{e}_{i}\widehat{e}_{j}
  \end{equation}
  \item Divergente de um vetor:
  \begin{equation}\label{eq134}
 \nonumber   \nabla \cdot \mathbf{v} = \frac{\partial}{\partial x_{i}}\widehat{e}_{i} \cdot (v_{j}\widehat{e}_{j}) = \frac{\partial v_{j}}{\partial x_{i}}\widehat{e}_{i} \cdot \widehat{e}_{j} = \frac{\partial v_{j}}{\partial x_{i}} \delta_{ij} = \frac{\partial v_{i}}{\partial x_{i}}=\frac{\partial v_{1}}{\partial x_{1}}+\frac{\partial v_{2}}{\partial x_{2}}+\frac{\partial v_{3}}{\partial x_{3}}
  \end{equation}
  \item Rotacional de um vetor:
  \begin{equation}\label{eq135}
 \nonumber   \nabla \times \mathbf{v} = \frac{\partial}{\partial x_{i}}\widehat{e}_{i} \times (v_{j}\widehat{e}_{j}) = \frac{\partial v_{j}}{\partial x_{i}}\widehat{e}_{i} \times \widehat{e}_{j} = \frac{\partial v_{j}}{\partial x_{i}} \varepsilon_{ijk}\widehat{e}_{k}
  \end{equation}
  \item Laplaciano de um vetor:
  \begin{equation}\label{eq136}
 \nonumber  \nabla^{2} \mathbf{v} =\nabla \cdot (\nabla \mathbf{v}) = \frac{\partial}{\partial x_{i}}\widehat{e}_{i} \left[\frac{\partial}{\partial x_{j}}\widehat{e}_{j}(v_{k}\widehat{e}_{k})\right]=\frac{\partial v_{k}}{\partial x_{i} \partial x_{j}}(\widehat{e}_{i} \cdot \widehat{e}_{j})\widehat{e}_{k}=\frac{\partial^{2} v_{k}}{\partial x_{i}^{2}}\widehat{e}_{k}=\left(\frac{\partial^{2} v_{1}}{\partial x_{1}^{2}},\frac{\partial^{2} v_{2}}{\partial x_{2}^{2}},\frac{\partial^{2} v_{3}}{\partial x_{3}^{2}}\right)
  \end{equation}
\end{itemize}


