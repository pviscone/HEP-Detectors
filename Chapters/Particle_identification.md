[TOC]

# Rivelatori Cherenkov

## Radiazione Cherenkov 

L'effetto Cherenkov si ha quando una particella attraversa un mezzo con velocità superiore a quella della luce nel mezzo stesso ($c_n=c_0/n$).

La radiazione Cherenkov è causata dalla polarizzazione asimmetrica del mezzo al passaggio della particella che, rilassandosi e tornando all'equilibrio, genera una radiazione di dipolo (questo succede per ogni sezione infinitesima della traccia della particella)

| <img src="images/Particle_identification/image-20220316192558631.png" alt="image-20220316192558631" style="zoom:50%;" /> |
| :----------------------------------------------------------: |
| A: Una particella a bassa velocità polarizza il mezzo in modo simmetrico |
| B: A velocità superiori a quella della luce nel mezzo la polarizzazione diventa fortemente asimmetrica |

Ogni punto della traccia genera un'onda e se la particella ha $v>c_n$ (con $c_n$ velocità di fase della luce nel mezzo) queste onde interferiscono in modo costruttivo

| <img src="images/Particle_identification/image-20220316193152123.png" alt="image-20220316193152123" style="zoom:50%;" /> |
| :----------------------------------------------------------: |
| Da questa figura si può ricavare facilmente l'angolo Cherenkov |

L'emissione Cherenkov avviene ad un angolo fissato che aumenta con la velocità della particella
$$
\cos(\theta_C)=\frac{1}{\beta n}
$$

> **NB** Il rinculo causato dall'emissione del fotone è trascurata ma calcoli in QM mostrano che questa approssimazione è valida nella maggior parte dei casi

Questo angolo se misurato può subire uno smearing dovuto alla relazione di dispersione del mezzo che non è costante nella frequenza

**Recap:** La radiazione Cherenkov avviene se:

- La particella ha velocità maggiore alla velocità di fase nel mezzo alla data frequenza di emissione (poichè per relazione di dispersione $n=n(\omega)$)
- Il mezzo è trasparente nell'ottico e ha dimensioni superiori alla linghezza d'onda della radiazione (necessario per permettere l'interferenza costruttiva)

Inoltre, a una distanza sufficiente dalla traccia della particella, le onde hanno polarizzazione trasversa: sono polarizzate linearmente in un piano contenente la direzione di propagazione dell'onda e la traccia della particella

## Cherenkov Threshold

La **velocità minima** per cui si ha emissione Cherenkov si ottiene ponendo $\cos(\theta_C)=1$ (Ovvero emissione in avanti a $0°$)
$$
\beta_\text{th}=\frac{1}{n}
$$
All'aumentare di $\beta$ cresce sia l'angolo che l'intensità dell'emissione.

L'**angolo massimo** invece si ottiene per $\beta=1$
$$
\cos(\theta_\text{max})=\frac{1}{n}
\\
\sin\theta_\text{max}=\sqrt{1-\cos(\theta_\text{max})^2}=\sqrt{1-\frac{1}{n^2}}=\frac{1}{\gamma_\text{th}}
$$

| <img src="images/Particle_identification/image-20220317114142322.png" alt="image-20220317114142322" style="zoom:67%;" /> |
| :----------------------------------------------------------: |
| Facendo il plot dell'angolo cherenkov normalizzato in funzione del $\gamma$ (normalizzato) si nota come il range di sensibilità di un rivelatore cherenkov è molto stretto dato che oltre una certa velocità la variazione dell'angolo di emissione è quasi nulla.<br />Già a $\gamma=2 \gamma_\text{th}$ l'angolo cherenkov ha raggiunto l'87% del suo valore asintotico $\theta_\text{max}$ |

Con semplici conti è possibile esprimere il seno dell'angolo in funzione di gamma
$$
\sin^2(\theta_C)=\sin^2(\theta_\text{max})\frac{\gamma^2-\gamma_\text{th}^2}{\gamma^2-1} \implies
\\
\implies \lim_{\gamma \to \infty} \frac{\theta_c}{\theta_\text{max}} \simeq \frac{R_c}{R_\text{max}} \simeq \sqrt{1-\frac{\gamma_\text{th}^2}{\gamma^2}}
$$
dove $R_c$ ed $R_\text{max}$ sono i raggi dei rispettivi anelli cherenkov

## Spettro di emissione

| ![image-20220317120219225](images/Particle_identification/image-20220317120219225.png) |
| :----------------------------------------------------------: |
| Spettro di emissione Cherenkov (Formula di Frank-Tamm).<br />Ricordiamo che si ha radiazione Cherenkov solo per $\beta^2 n^2(\omega)>1$ |



# Transition radiation detectors



# PID Methods

