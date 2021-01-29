# Galaxy Defender
Motta Jacopo

# Concept del giogo

Galaxy Defender è un gioco di sopravvivenza ambientato nello spazio, con visuale dall&#39;alto. Il giocatore controlla un&#39;astronave che è libera di muoversi liberamente nell&#39;area di gioco. Una serie di nemici inizierà a spawnare e il giocatore dovrà cercare di sopravvivere sparando. Il campo di gioco è anche attraversato da degli asteroidi. Il giocatore può decidere di evitarli oppure distruggerli per ottenere delle capsule che ripristinano la vita persa. Il gioco termina quando il giocatore termina la vita e il punteggio viene calcolato in base al numero di nemici eliminati.

# Game loop

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture1.png" width="300">

_Figura 1 Game Loop_

# Concept map

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture2.png" width="700">

_Figura 2 Concept Map_

# Analisi tecnica e meccaniche

# Level design e interfaccia grafica

Il campo di gioco è strutturato come un rettangolo con vista dall&#39;alto. Il giocatore può muoversi liberamente all&#39;interno ma non può uscire perché bloccato a muri invisibili.

Nell&#39;interfaccia grafica del gioco sono indicate la salute corrente del giocatore, lo stato delle sue armi, il numero di nemici eliminati e il punteggio corrispondente.

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture3.png" width="600">

_Figura 3 Screenshot dal gioco_

# Mesh del gioco

Tutte le mesh del gioco sono state realizzate utilizzando Tinkercad.

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture4.png" width="500">

_Figura 4 Mesh_

# Player

Il giocatore controlla un pawn costituito dalla static mesh di un&#39;astronave e circondato da un box collider. Il pawn contiene anche dei &quot;scene component&quot; che indicano la posizione da cui saranno poi spawnati i proiettili che l&#39;astronave può sparare.

L&#39;astronave del giocatore possiede 2 armi:

- L&#39;arma primaria spara una coppia di proiettili che può essere sparato ad oltranza ma al costo di surriscaldare l&#39;arma che smette di funzionare per un po&#39; di secondi se usata troppo.
- L&#39;arma secondaria spara una sequenza di 5 proiettili che infliggono un danno maggiore ma ha bisogno di un tempo di ricarica dopo ogni sparo.

Le informazioni sul surriscaldamento e ricarica delle armi sono rappresentate nella UI.

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture5.png" width="800">

_Figura 5 Player pawn ___ Barra della salute ___ Arma primaria e secondaria_

Il giocatore può muoversi liberamente del campo di gioco e controlla l&#39;accelerazione dell&#39;astronave con i tasti WASD, mentre l&#39;orientamento è dettato dalla posizione del cursore del mouse che funziona da mirino.

# Nemici

Esistono tre tipi diversi di nemici nel gioco che spawnano ad oltranza man mano che il giocatore ne elimina un certo numero e hanno lo scopo di infliggere danno al giocatore. Hanno una quantità di salute diversa in base al tipo, infliggono danni differenti e una volta distrutti conferiscono uno score differente.

- Il nemico1 spawna in continuo, si muove orizzontalmente nella parte alta dello schermo e spara dei proiettili verso il basso. Possono esserci al massimo 5 nemici di questo tipo in contemporanea.
- Il nemico2 spawna quando sono stati eliminati un tot di nemici (ogni multiplo di 5) e si muove verso la posizione del giocatore cercando di raggiungerlo per schiantarglisi contro. Man mano che si eliminano nemici c&#39;è una probabilità sempre più alta che spawnino un numero maggiore di nemici2 per volta.
- Il nemico3 spawna quando sono stati eliminati un tot di nemici (ogni multiplo di 15) e si muove in maniera verticale lungo i muri laterali del campo di gioco, emettendo un raggio laser continuo che attraversa il campo di gioco in orizzontale. È il nemico con la salute maggiore.

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture6.png" width="800">

_Figura 6 Enemy1 ___ Enemy2 ___ Enemy3_

# Asteroidi

Gli asteroidi attraversano il campo di gioco e provengono da qualsiasi direzione. Se colpiscono il giocatore infliggono danno. Il giocatore può decidere se distruggerli o schivarli. Quando vengono distrutti hanno una certa probabilità di droppare una capsula che se raccolta dal player ripristina parte della sua salute. Anche gli asteroidi una volta distrutti conferiscono un piccolo score.

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture7.png" width="600">

_Figura 7 Asteroidi ___ Capsula salute_

# Controlli

Gli input al gioco avvengono tramite mouse e tastiera. Con i tasti WASD si controllano i movimenti del giocatore, mentre con il mouse se ne controlla l&#39;orientamento. Il tasto destro e sinistro del mouse servono per sparare. Il gioco può essere messo in pausa premendo il tasto P.

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture8.png" width="400">

_Figura 8 Controlli_

# Menù e opzioni

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture9.png" width="600">

_Figura 9 Main menù_

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture10.png" width="600">

_Figura 10 Scoreboard_

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture11.png" width="600">

_Figura 11 Control_

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture12.png" width="600">

_Figura 12 Graphics settings_

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture13.png" width="600">

_Figura 13 Credits_

<img src="https://github.com/mottajacopo/Galaxy_Defender_UE4/blob/master/Images/Picture14.png" width="600">

_Figura 14 Pause menu_
