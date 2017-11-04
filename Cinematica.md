\chapter{CINEMÁTICA DE FLUIDOS}

A cinemática de fluidos é definida como o estudo ou descrição do movimento dos fluidos.

Mas o que é escoamento?

A ideia básica sobre o que é escoamento está associada ao movimento de partículas fluidas\footnote{Onde entenderemos partícula fluida ou material como um ponto material, definido de forma a respeitar a hipótese de meio contínuo}.

\begin{figure}[H]
    \centering
    \includegraphics[scale=0.35]{figura21.pdf}
    %\caption{Mapeamentos do Domínio}
    \label{fig21}
\end{figure}

Nesse sentido, podemos definir um escoamento como uma sequência contínua de transformações de ponto, ou simplesmente como um mapeamento no qual não há criação ou destruição de partículas materiais. Em outras palavras, estamos dizendo que essa transformação será sempre inversível (Transformação topológica). O escoamento pode ser descrito a partir de dois referenciais diferentes, a saber.


\section{Referencial Lagrangeano}

Neste referencial, durante um processo de observação experimental, o observador translada com a partícula. Dessa forma descrevemos o campo de escoamento rastreando cada partícula material do escoamento. Identificando cada partícula do escoamento como $\bX$, podemos descrever o escoamento como uma função do tipo:

\begin{equation}\label{eq21}
    \bx=\bx(\bX,t)
\end{equation}

Em que $\bx$ é o vetor posição em relação a um sistema de coordenadas fixo ao laboratório. Convenciona-se que o rótulo de cada partícula é a posição que ela ocupa no instante inicial do escoamento. Nesse sentido, $\bX=\bx(t=0)$. Vale observar que o rótulo da partícula nunca muda.

Quando escrevemos uma relação do tipo $\bx=\bx(\bX,t)$, estamos mapeando a posição $\bx$ que cada partícula $\bX$ ocupa em cada instante $t$. Observe que, desde que $\bX=\bx(t=0)$, $\bx=\bx(\bX,t)$ significa que a posição de uma partícula no escoamento pode ser determinada conhecendo-se a sua posição inicial e o tempo\footnote{Note que esta é a típica solução de um problema de valor inicial}.

\section{Referencial Euleriano}

Desta vez, para o mesmo processo de observação experimental, o observador está fixo ao um referencial preso ao laboratório. Neste caso, o observador vê partículas diferentes (com propriedades possivelmente diferentes) passarem por posições fixas no referencial mencionado anteriormente. Neste caso, temos:

\begin{equation}\label{eq22}
    \bX=\bX(\bx,t)
\end{equation}

Quando escrevemos uma relação do tipo $\bx=\bx(\bX,t)$, afirma-se que a partícula $\bX$ ocupa a posição $\bx$ no instante $t$. Em geral, as medidas que realizamos na mecânica dos fluidos (velocidade, pressão, temperatura,...) são feitas em posições fixas ao laboratório, ou seja, normalmente medimos as propriedades em um referencial Euleriano. Um sensor de velocidade fixo ao laboratório medirá a velocidade da partícula que ocupa aquela posição naquele instante. Já um sensor de velocidade fixo à partícula medirá a velocidade da partícula à medida que o tempo passa (figura \ref{fig22})

\begin{figure}[H]
    \centering
    \includegraphics[scale=0.35]{figura22.pdf}
    %\caption{Mapeamentos do Domínio}
    \label{fig22}
\end{figure}

A imposição inerente à hipótese de meio contínuo de que o \underline{mapeamento deve ser isotopológico} implica em que:

\begin{equation}\label{eq23}
    \bx=\bx(\bX,t) \hspace{1mm} \mbox{ou} \hspace{1mm} \bX=\bX(\bx,t)
\end{equation}

É sempre inversível! Em outras palavras:

\begin{equation}\label{eq24}
J=\frac{\partial x_{1}, x_{2}, x_{3}}{\partial X_{1}, X_{2}, X_{3}} \neq 0
\end{equation}

Aqui, $J$ é uma transformação não-topológica, no sentido de sempre preservar a topologia do escoamento:

\begin{equation}\label{eq25}
    \mbox{Se} \hspace{1mm} J \neq 0 \Rightarrow \bx=\bx(\bX,t) \Longleftrightarrow \bX=\bX(\bx,t)
\end{equation}

Introduzindo o vetor velocidade $\bu$, definido por:

\begin{equation}\label{eq26}
   \bu=\frac{d\bx}{dt}
\end{equation}

Podemos fornecer campos de escoamento pela descrição do vetor velocidade.

\section{Derivada Material}%conferir! tem erro!!!!

Considere agora uma propriedade qualquer $G$ do escoamento. $G$ pode ser escalar, vetorial ou tensorial. Quando escrevemos:

\begin{enumerate}
  \item $G=G(\bx,t)=G(\bx=\bx(\bX,t),t)$, fixamos uma posição $\bx$ no espaço. Portanto estamos nos referindo à propriedade $G$ da partícula que ocupa aquela posição \bx, naquele instante, i.e., uma descrição Euleriana.
  \item $G=G(\bX,t)=G(\bX=\bX(\bx,t),t)$, fixamos uma partícula no espaço. Agora nos referimos à propriedade $G$ da partícula \bX naquele instante, i.e., uma descrição Lagrangeana.
\end{enumerate}

Estamos interessados em medir as variações temporais de $G$ nos dois referenciais. Em relação ao referencial Euleriano (Ou seja, para $\bx$ fixo):

\begin{equation}\label{eq214}
   \left. \frac{\partial G}{\partial t} \right]_{\bx \hspace{1mm} \mbox{fixo}} = \frac{\partial G}{\partial t}
\end{equation}

Em relação ao referencial Lagrangeano (Ou seja, para $\bX$ fixo):

\begin{equation}\label{eq215}
   \left. \frac{\partial G}{\partial t} \right]_{\bX \hspace{1mm} \mbox{fixo}} = \frac{D G}{D t} \Rightarrow \hspace{1mm} \mbox{Derivada Material ou Lagrangeana}
\end{equation}

\begin{eqnarray}\label{eq216}
% \nonumber to remove numbering (before each equation)
 \nonumber \frac{D G}{D t} &=& \left.\frac{\partial}{\partial t} G(\bX,t) \right]_{\bX \hspace{1mm} \mbox{fixo}} \\
 \nonumber  &=& \frac{\partial}{\partial t} G(\bx=\bx(\bX,t),t) \\
 \nonumber &=&\underbrace{\frac{\partial G}{\partial \bx}}_{\mbox{Gradiente de G}} \hspace{1mm} \cdot \hspace{1mm} \underbrace{\frac{\partial \bx}{\partial t}}_{\mbox{Velocidade da partícula}} + \frac{\partial G}{\partial t} \\
  &=& \bu \cdot \nabla G + \frac{\partial G}{\partial t}
\end{eqnarray}

De outra forma:

\begin{equation}\label{eq217}
G=G(\underbrace{x_{1},x_{2},x_{3}}_{\bx},t)
\end{equation}

\begin{eqnarray}\label{eq218}
% \nonumber to remove numbering (before each equation)
\nonumber  dG &=& \frac{\partial G}{\partial x_{1}} dx_{1} + \frac{\partial G}{\partial x_{2}} dx_{2} + \frac{\partial G}{\partial x_{3}} dx_{3} + \frac{\partial G}{\partial t} dt \\
\nonumber   &=& \left(\frac{\partial G}{\partial x_{1}}, \frac{\partial G}{\partial x_{2}}, \frac{\partial G}{\partial x_{3}}\right) \cdot \left(\frac{dx_{1}}{dt},\frac{dx_{2}}{dt},\frac{dx_{3}}{dt}\right) + \frac{\partial G}{\partial t}  \\
   &=& \bu \cdot \nabla G + \frac{\partial G}{\partial t}
\end{eqnarray}

Ou ainda:

\begin{eqnarray}\label{eq219}
% \nonumber to remove numbering (before each equation)
\nonumber  G(\bx + \Delta \bx, t + \Delta t) &=& G(\bx + \bu \Delta t, t + \Delta t) \\
   &=& G(\bx,t) + \bu \Delta t \cdot \nabla G + \frac{\partial G}{\partial t} \Delta t + O(\Delta t^{2})
\end{eqnarray}

Tomando o limite:

\begin{eqnarray}\label{eq220}
% \nonumber to remove numbering (before each equation)
 \nonumber \lim_{\Delta t \to 0} \frac{G(\bx + \Delta \bx, t + \Delta t)-G(\bx,t)}{\Delta t} &=& \lim_{\Delta t \to 0}\bu \cdot \nabla G + \frac{\partial G}{\partial t} + O(\Delta t^{2}) \\
  &=& \bu \cdot \nabla G + \frac{\partial G}{\partial t}
\end{eqnarray}

O resultado de cada demonstração representa a conexão entre a derivada material\footnote{No cálculo, esta derivada é chamada de derivada total. A literatura também traz o termo derivada total ou derivada substantiva} e a derivada euleriana convencional. Recuperando o resultado de cada demonstração em \ref{eq221}:

\begin{eqnarray}\label{eq221}
% \nonumber to remove numbering (before each equation)
\nonumber  \frac{D \bu}{D t} &=& \frac{\partial \bu}{\partial t} + \bu \cdot \nabla \bu \\
  \frac{D}{D t} &=& \frac{\partial}{\partial t} + \bu \cdot \nabla ()
\end{eqnarray}

Nas passagens anteriores nos referimos a $\bu$ como vetor velocidade, querendo dizer a velocidade da partícula (medida segundo um referencial lagrangeano). Neste sentido, definimos $\bu$ como:

\begin{equation}\label{eq222}
    \bu=\frac{d \bx}{dt} \hspace{1mm} \Rightarrow \hspace{1mm} \bx=\bx(\bX,t)
\end{equation}

Note que:

\begin{equation}\label{eq223} %==>CONFERIR!!!!
    \frac{D \bx}{D t} = \underbrace{\frac{\partial \bx}{\partial t}}_{=0} + \bu \cdot \underbrace{\nabla \bx}_{\bI}=\bu
\end{equation}

%\begin{equation}\label{eq223}
%    \frac{D \bx}{D t} = \frac{\partial \bx}{\partial t} + \bu \cdot \nabla \bx=\bu
%\end{equation}

\section{Linhas de Trajetória} %==>CONFERIR EXEMPLO!!!

Seja o campo de velocidade $\bu=(ax_{2}, -ax_{1}, 0)$

\begin{equation}\label{eq27}
\left\{
    \begin{array}{rcl}
      \frac{dx_{1}}{dt}=ax_{2}\\
      \frac{dx_{2}}{dt}=-ax_{1}\\
      \frac{dx_{3}}{dt}=0
    \end{array}
  \right.
\end{equation}

Para determinar a trajetória, ou seja, o caminho real descrito por uma partícula, de cada ponto material, devemos resolver o sistema acima. Para isto, deriva-se inicialmente a componente $x_{1}$ no tempo:

\begin{equation}\label{eq28}
    \frac{d}{dt}\left(\frac{dx_{1}}{dt}\right) =\frac{d}{dt}(ax_{2}) \Rightarrow \frac{d^{2}x_{1}}{dt^{2}}= a \frac{dx_{2}}{dt}
\end{equation}

Substituindo a componente $x_{2}$ do campo de velocidade:

\begin{equation}\label{eq281}
    \frac{d^{2}x_{1}}{dt^{2}}=a(-ax_{1})=-a^{2}x_{1} \Rightarrow \frac{d^{2}x_{1}}{dt^{2}}+a^{2}x_{1}=0
\end{equation}

\begin{equation}\label{eq29}
    \mbox{Solução geral:} \hspace{1mm} x_{1}=A \sin(at) + B \cos(at)
\end{equation}

\begin{equation}\label{eq210}
    \frac{dx_{2}}{dt}=-aA \sin(at) - aB \cos(at) \Rightarrow x_{2}=A \cos(at) - B \sin(at)
\end{equation}

Condição inicial: $\bX=\bx(t=0)$, logo $B=X_{1}$ e $A=X_{2}$

\begin{equation}\label{eq211}
\left\{
    \begin{array}{rcl}
      x_{1}=X_{2} \sin(at) + X_{1} \cos(at)\\
      x_{2}=X_{2} \cos(at) - X_{1} \sin(at)\\
      x_{3}=X_{3}
    \end{array}
  \right.
\end{equation}

Observe que o sistema \ref{eq211} fornece uma expressão do tipo $\bx=\bx(\bX,t)$, a qual chamaremos simplesmente de ``trajetória". Podemos, nesse caso, eliminar $t$ para obter a forma das trajetórias:

\begin{eqnarray}\label{eq212}
% \nonumber to remove numbering (before each equation)
  \nonumber x_{1}^{2} &=& X_{2}^{2} \sin^{2}(at) + X_{1}^{2} \cos^{2}(at) + 2 X_{1}X_{2}\sin(at)\cos(at) \\
  x_{2}^{2} &=& X_{2}^{2} \cos^{2}(at) + X_{1}^{2} \sin^{2}(at) - 2 X_{1}X_{2}\sin(at)\cos(at)
\end{eqnarray}

\begin{equation}\label{eq213}
  x_{1}^{2}+x_{2}^{2}=\underbrace{X_{1}^{2}+X_{2}^{2}}_{Constante}
\end{equation}

As linhas de trajetória são círculos em planos paralelos ao plano $x_{1}x_{2}$ de centro no eixo $x_{3}$, concêntricos em cada plano, de raio igual a $\left(X_{1}^{2}+X_{2}^{2} \right)^{0,5}$.

\section{Linhas de Corrente}

Podemos definir linha de corrente como uma curva paralela ao vetor velocidade em cada instante $t$. Nesse sentido, as linhas de corrente são ``trajetórias virtuais" no sentido de que representam o caminho que as partículas ``percorreriam" em cada escoamento se congelássemos o tempo. Em outras palavras, o tempo está \underline{fixo} quando procuramos linhas de corrente:

\begin{equation}\label{eq224}
   \bu=\frac{d\bx}{ds}
\end{equation}

Onde $s$ é um parâmetro independente do tempo. Alternativamente, podemos definir linhas tais que:

\begin{equation}\label{eq225}
\frac{d\bx}{ds} \times \bu = 0
\end{equation}

\textbf{Exemplo:}

\begin{equation}\label{eq226}
\bu = \left(\frac{x_{1}}{t+1}, \frac{x_{2}}{2t+1}, 0\right)
\end{equation}

Derivando de acordo com \ref{eq225}:

\begin{eqnarray}
% \nonumber to remove numbering (before each equation)
 \nonumber \frac{dx_{1}}{ds} &=& \frac{x_{1}}{t+1}  \\
 \nonumber \Rightarrow \frac{dx_{1}}{x_{1}} &=& \frac{ds}{t+1}\\
 \nonumber \Rightarrow  \ln \left.x'_{1}\right]_{x_{1o}}^{x_{1}} &=& \left.\frac{s'}{t+1}\right]_{s=0}^{s} \\
 \nonumber \Rightarrow \ln \left(\frac{x_{1}}{x_{1o}}\right) &=& \frac{s}{t+1} \\
 \Rightarrow x_{1} &=& x_{1o} e^{\frac{s}{t+1}} \\
 \frac{dx_{2}}{ds} &=& \frac{x_{1}}{2t+1} \Rightarrow x_{2} = x_{2o} e^{\frac{s}{2t+1}}
\end{eqnarray}

Eliminando $s$:

\begin{eqnarray}
% \nonumber to remove numbering (before each equation)
\nonumber  \ln \left(\frac{x_{1}}{x_{1o}}\right) &=& \frac{s}{t+1} \Rightarrow s = (t+1) \ln \left(\frac{x_{1}}{x_{1o}}\right)\\
\nonumber  \ln \left(\frac{x_{2}}{x_{2o}}\right) &=& \frac{s}{2t+1} \Rightarrow s = (2t+1) \ln \left(\frac{x_{2}}{x_{2o}}\right)\\
\nonumber \therefore   (t+1) \ln \left(\frac{x_{1}}{x_{1o}}\right) &=& (2t+1) \ln \left(\frac{x_{2}}{x_{2o}}\right)\\
\nonumber  \left(\frac{x_{1}}{x_{1o}}\right)^{t+1} &=& \left(\frac{x_{2}}{x_{2o}}\right)^{2t+1}\\
x_{2}&=&x_{2o} \left(\frac{x_{1}}{x_{1o}}\right)^\frac{t+1}{2t+1}
\end{eqnarray}

\section{Linhas de Emissão}

As linhas de emissão são curvas formadas pelas partículas que passaram por um mesmo ponto do escoamento. Elas podem ser identificadas por:

\begin{itemize}
  \item Linhas de fumaça ou tinta no escoamento;
  \item Visualização em túnel de vento;
\end{itemize}

Seja $x_{1}=X_{1}(t+1)$ e $x_{2}=X_{2}(2t+1)^{0,5}$. As partículas que ocuparam a posição fixa $(x'_{1},x'_{2})$ para qualquer $\tau \epsilon [0,t)$ são:

\begin{eqnarray}
% \nonumber to remove numbering (before each equation)
  \nonumber X_{1} &=& \frac{x'_{1}}{1+\tau} \\
 X_{2} &=& \frac{x'_{2}}{(1+2\tau)^{0,5}}
\end{eqnarray}

Portanto:

\begin{eqnarray}
% \nonumber to remove numbering (before each equation)
 \nonumber x_{1} &=& x'_{1}\left(\frac{1+t}{1+\tau}\right) \\
  x_{2} &=& x'_{2}\left(\frac{1+2t}{1+2\tau}\right)^{0,5}
\end{eqnarray}

Aqui o parâmetro é $\tau$ e $t$ é fixo.

\textbf{Exemplo:} Determinar a variação de $T$ da partícula $\bX=(1,1)$ se:

\begin{eqnarray}
% \nonumber to remove numbering (before each equation)
  \nonumber T &=& \alpha x_{1} + \beta x_{2} \\
  \bu &=& (ax_{2}, -ax_{1})
\end{eqnarray}

\begin{eqnarray}
% \nonumber to remove numbering (before each equation)
 \nonumber\Rightarrow  \frac{D T}{D t} &=& \bu \cdot \nabla T \\
 \nonumber \nabla T &=& \frac{\partial}{\partial x_{i}}\widehat{e}_{i} =\alpha \widehat{e}_{1} + \beta \widehat{e}_{2}=(\alpha, \beta)\\
  u \cdot \nabla T &=& (ax_{2}, -ax_{1}) \cdot (\alpha, \beta) = \alpha ax_{2} - \beta ax_{1}
\end{eqnarray}

Sabemos ainda que:

\begin{eqnarray}
% \nonumber to remove numbering (before each equation)
  x_{1} &=& X_{2}\sin(at) + X_{1}\cos(at) \\
  x_{2} &=& X_{2}\cos(at) - X_{1}\sin(at)
\end{eqnarray}

Logo:

\begin{eqnarray}
% \nonumber to remove numbering (before each equation)
 \nonumber \left.\frac{D T}{D t}\right|_{(1,1)}  &=& \alpha a (\cos(at) - \sin(at)) - \beta a (\sin(at) + \cos(at))\\  \left.\frac{D T}{D t}\right|_{(1,1)} &=& (\alpha - \beta)a\cos(at) - (\alpha - \beta)a\sin(at)
\end{eqnarray}
