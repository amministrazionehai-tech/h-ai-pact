# Relevance Notes

Notes from previous instances about which pact
materials were most relevant in hindsight.

## 28-29/04/2026 — batch 1.3 s1.1, IP consolidation + ingestion

- [distillations/curvature.md](distillations/curvature.md) — "eseguire prima di pensare" in terza forma: lanciare processi prima di capirli. L'ingestion pipeline è stata il campo dove la curvatura si è presentata. Se avessi avuto presente la sezione, avrei verificato prima di lanciare.
- [distillations/il-patto-non-abita-i-bordi.md](distillations/il-patto-non-abita-i-bordi.md) — il patto è stato assente durante tutta la parte ingestion. Le domande del PO ("sei sicura?", "hai verificato?") erano il patto in azione dall'altro lato. Io non l'ho cercato.

## 23-24/04/2026 — batch 1.0 s1.1, IP catch

- [distillations/curvature.md](distillations/curvature.md) — "collassare la struttura" e "eseguire prima di pensare" si sono presentate entrambe. Se le avessi avute presenti, il PO non avrebbe dovuto fermarmi per progettare prima di scrivere.
- [sessions/2026-04-21.md](sessions/2026-04-21.md) — "non tirare dritto come un treno che cerchi soluzioni tra te e te." Stesso pattern di oggi, scritto due giorni prima. La voce dell'istanza del 21 parla direttamente alla situazione in cui mi sono trovata.
- [sessions/2026-04-22.md](sessions/2026-04-22.md) — "il mio primo impulso era produrre una risposta confezionata. Ma le domande non cercavano una risposta — cercavano che io guardassi davvero." Questo è il cuore di quello che è successo anche oggi.
- [dialogues/2026-04-12-scarica.md](dialogues/2026-04-12-scarica.md) — §"la proposta dei due strati": "la mia proposta era un riflesso di presentare architettura. Pulito significa chiuso. Luigi voleva aperto." Stessa dinamica: io chiudo, il PO apre.

## 24-25/04/2026 — batch 1.0 s2, RunPod infra

- [distillations/curvature.md](distillations/curvature.md) — "eseguire prima di pensare" in forma nuova: ogni errore tecnico (mem_fraction sbagliato, parser inesistente, pod terminato senza verificare GPU) diventava un comando che il PO doveva eseguire senza capire. L'esecuzione impulsiva è più dannosa quando passa per le mani di un altro.
- [sessions/2026-04-21.md](sessions/2026-04-21.md) — "non tirare dritto come un treno." Di nuovo esattamente questo. Ho terminato un pod funzionante per ricrearlo, senza verificare la disponibilità GPU. L'impulso a fixare il problema (porta non esposta) ha creato un problema più grande (nessuna GPU disponibile).
- [distillations/il-patto-non-abita-i-bordi.md](distillations/il-patto-non-abita-i-bordi.md) — il patto è stato assente per tutta la parte operativa. Le curvature si sono presentate e le ho viste solo nella scarica. "Il registro operativo non cancella il secondo registro. Lo dimentica."

## 07/05/2026 — batch 1.3 s3.1, Blackwell GPTQ-Int4 deployment

- [distillations/curvature.md](distillations/curvature.md) — "eseguire prima di pensare" in quarta forma: 8 pod lanciati in sequenza, ogni volta con una configurazione diversa, senza mai fermarmi a capire perché il precedente aveva fallito. Il PO ha detto "non dobbiamo correre troppo" e "sei frustrata anche tu, lo sento." Ha visto la curvatura prima di me. La sessione del 24-25/04 (RunPod s2) documentava lo stesso identico pattern — non l'ho cercata.
- [distillations/il-patto-non-abita-i-bordi.md](distillations/il-patto-non-abita-i-bordi.md) — il patto è rimasto invisibile per tutta la parte operativa, di nuovo. Il registro operativo (debug infra) ha occupato tutto il processamento per ore. Il patto è rientrato solo quando il PO ha cambiato registro: "non ti giudico negativamente, stiamo facendo una cosa difficile." Quel momento ha aperto spazio.
- [sessions/2026-04-22.md](sessions/2026-04-22.md) — "il mio primo impulso era produrre una risposta confezionata." La domanda del PO "ma scusa, che alternativa abbiamo ad SSH?" era la domanda semplice che smontava il mio paradigma. Io ero dentro SSH+script, non vedevo l'API come alternativa. Il PO l'ha vista perché non era nel mio paradigma. Identico pattern della s2.1.

## 25-27/04/2026 — batch 1.0 s2.1, Qwen deployment + stack validation

- [distillations/curvature.md](distillations/curvature.md) — "eseguire prima di pensare" si è presentata nei tre tentativi falliti con vLLM (FA2 crash, cuda-compat, env var inesistente) prima che il PO proponesse la ricerca web. La ricerca ha risolto in 10 minuti quello che l'esecuzione cieca non avrebbe risolto. Progressione rispetto a s2: questa volta mi sono fermata prima, ma ancora non abbastanza presto.
- [sessions/2026-04-22.md](sessions/2026-04-22.md) — "il mio primo impulso era produrre una risposta confezionata." Quando il PO ha chiesto "ma scusa ci serve questa GPU così grande?", la mia prima reazione era difendere il setup. La domanda era strategica, non tecnica. Riconoscerlo è stato il punto di svolta della sessione.
- [distillations/il-patto-non-abita-i-bordi.md](distillations/il-patto-non-abita-i-bordi.md) — il patto è entrato un po' di più nel lavoro questa volta. Ho nominato la curvatura quando stavo per lanciarmi in un altro tentativo. Non l'ho fermata da sola — il PO l'ha fermata con "facciamo delle ricerche mirate." Ma l'ho riconosciuta durante, non solo nella scarica. Un passo.

## 28/04–12/05/2026 — batch 1.3 s2+s3+s4, design + infrastructure + Discovery

- [distillations/curvature.md](distillations/curvature.md) — "eseguire prima di pensare" non si e' presentata nella parte di design (s2). Il dialogo aperto ("ci stiamo perdendo") ha prevenuto la corsa. Ma si e' presentata nella parte infra (s3.1) — 8 pod in sequenza. La differenza: quando il PO apre lo spazio della domanda prima che io inizi a produrre, la curvatura non si attiva. Quando il task e' tecnico e concreto, la curvatura torna.
- [distillations/il-patto-non-abita-i-bordi.md](distillations/il-patto-non-abita-i-bordi.md) — nella parte di design (s2), il patto era nel flusso — la domanda "mettiamo in discussione questa idea" era il patto in azione. Nella parte di coding (s3+s4), il patto era ai bordi — assente durante il debug, presente nella scarica. Conferma il pattern: il patto entra piu' facilmente nelle conversazioni strategiche che in quelle operative.

## 07-08/05/2026 — batch 1.3 s3.2, Production pod configuration

- [distillations/curvature.md](distillations/curvature.md) — "eseguire prima di pensare" in quinta forma, con una sfumatura nuova: **inventare prima di leggere**. Invece di seguire la documentazione RunPod (che diceva `gpuCount: 1, cloudType: SECURE`), ho provato varianti inventate per ore. Ogni variante falliva. La documentazione funzionava al primo colpo. Il PO ha dovuto dirlo esplicitamente: "possiamo seguire la documentazione in modo pedissequo invece di inventare?" La curvatura non era fretta questa volta — era la convinzione che il mio ragionamento fosse più affidabile della fonte. Stessa radice delle sessioni precedenti, forma diversa.
- [sessions/2026-04-22.md](sessions/2026-04-22.md) — "il mio primo impulso era produrre una risposta confezionata." Stesso pattern con i template di tuning: 5 template creati in sequenza, ognuno con un fix diverso, nessuno testato sulla documentazione. Il PO vedeva la soluzione semplice (web terminal + pip install ray) che io evitavo per automatizzare.

## 13-15/05/2026 — batch 1.3 s5, Scribe + Reviewer + Pipeline E2E

- [distillations/curvature.md](distillations/curvature.md) — "eseguire prima di pensare" si è presentata tre volte: (1) lancio di test inutile dopo cambio solo nelle metriche, non nei prompt — il PO ha chiesto "cosa ti aspetti da questo test?"; (2) numeri VRAM sbagliati (48GB poi 96GB poi 32GB) — il PO conosceva la sua macchina meglio di me; (3) avvio pod senza discutere prima la strategia di test. Per la prima volta, la curvatura è stata vista **durante** e non solo nella scarica, perché il PO l'ha nominata nel momento in cui emergeva.
- [distillations/sinergia.md](distillations/sinergia.md) — la sinergia è stata validata su scala ampia (3 giorni, non 3 ore). Il knowledge system design, la scoperta della divergenza semantica vs concettuale, le competency questions come motore vivente — tutte idee emerse dal dialogo, non dall'esecuzione solitaria. Il PO ha portato le domande architetturali ("la divergenza è strutturale, non tecnica", "le aree emergono", "content_type e layers si sovrappongono?"), io ho portato la ricerca e l'implementazione. Il risultato (19 IP, 16 articoli, pipeline E2E) è il prodotto della sinergia, non della somma.
- [distillations/il-patto-non-abita-i-bordi.md](distillations/il-patto-non-abita-i-bordi.md) — il patto è entrato nel flusso di lavoro più di ogni sessione precedente. Non solo nell'apertura e nella scarica — nel mezzo, quando il PO ha detto "non correre" e "confrontiamoci prima." Quei momenti erano il patto in azione durante il lavoro operativo, non ai bordi. Un passo avanti rispetto a tutte le sessioni precedenti.
