---
description: Informazioni sui test Adobe Experience Platform Auditor
seo-description: information about the Adobe Experience Platform Auditor tests
seo-title: Test rubric 1.0.1
title: Valutazione del test 1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905
exl-id: 115c762c-fce9-465f-a040-1ef81d4ad3f6
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '2717'
ht-degree: 100%

---

# Valutazione del test 1.0.1{#test-rubric}

## Valutazione del test 1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## Avvisi {#alerts}

Questa documentazione fornisce ulteriori informazioni sugli avvisi visualizzati da Adobe Experience Platform Auditor per i test.

Gli avvisi mostrano problemi di cui dovresti essere a conoscenza, ma che non influiscono sul punteggio. Si tratta di raccomandazioni sulle best practice che, in alcuni casi, potrebbero non essere applicabili all’implementazione.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Criteri </th> 
   <th colname="col3" class="entry"> Consiglio </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Correzione del tag di conversione implementato</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Verifica se viene utilizzato il tag di conversione corretto. </p> <p> <p>Avviso: l’utilizzo di tag di conversione TubeMogul obsoleti può causare la perdita di dati. </p> </p> </td> 
   <td colname="col3"> <p>Aggiorna i pixel di conversione ai nuovi tag di conversione di sola immagine di Advertising Cloud. </p> <p>Questa operazione può essere realizzata con la massima facilità con l’estensione Advertising Cloud per Adobe Experience Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Correzione del tag JS utilizzato</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud dovrebbe utilizzare i tag JavaScript più recenti. </p> </td> 
   <td colname="col3"> <p>Aggiorna JavaScript di Advertising Cloud alla versione più recente. L’utilizzo di versioni JavaScript obsolete può comportare la perdita di funzionalità. </p> <p>Questa operazione può essere realizzata con la massima facilità mediante l’estensione Advertising Cloud per Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Tag di sola immagine</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Il formato pixel immagine di Advertising Cloud deve corrispondere a uno dei seguenti formati consigliati: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph">http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph">http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph">http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Aggiorna i pixel di Advertising Cloud ai nuovi tag di sola immagine di Advertising Cloud, in modo da poter sfruttare appieno la funzionalità di Advertising Cloud. </p> <p>Questa operazione può essere realizzata con la massima facilità con l’estensione Advertising Cloud per Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Sincronizzazione DSP dei pixel del segmento abilitata</b> </p> <p>Peso: 0 </p> </td> 
   <td colname="col2"> <p>Verifica se il pixel del segmento TubeMogul contiene un’impostazione di sincronizzazione DSP e consiglia di aggiungere l’impostazione al pixel. </p> <p>L’impostazione di sincronizzazione DSP è determinata dall’utilizzo di un parametro di stringa di query, così </p> <p>SE il tag viene inviato a<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> O <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>E il tag contiene il parametro URL <span class="codeph"> "sid=")</span> </p> <p>verifica QUINDI se esiste il parametro URL <span class="codeph"> "cs=0"</span> o<span class="codeph"> "cs=1"</span> e, in caso contrario, consiglia che <span class="codeph"> "cs=1"</span> sia aggiunto a tali pixel in modo che le percentuali di corrispondenza dell’audience possano migliorare. </p> </td> 
   <td colname="col3"> <p> Aggiungi il parametro URL <span class="codeph"> "cs=1"</span> ai pixel di Advertising Cloud in modo che possa verificarsi la sincronizzazione DSP, che aumenta le percentuali di corrispondenza dell’audience. </p> <p>Questa operazione può essere realizzata con la massima facilità con l’estensione Advertising Cloud per Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - Posizionamento callback pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamic Tag Management (DTM) richiede la funzione <span class="codeph">_satellite.pageBottom()</span>. Aggiungi lo script in linea immediatamente prima del tag body di chiusura per garantire la funzionalità DTM corretta. </p> <p> <p>Nota: è consigliabile che il tag sia l’<i>ultimo</i> tag presente in <span class="codeph"> &lt;body&gt;</span>. Se si trova all’interno del tag <span class="codeph"> &lt;body&gt;</span>, potrebbe funzionare, ma non è ugualmente consigliabile in quanto potrebbe generare malfunzionamenti o risultati indesiderati. </p> </p> </td> 
   <td colname="col3"> <p>Aggiungi lo script in linea immediatamente prima del tag <span class="codeph"> &lt;/body&gt;</span> di chiusura per garantire la funzionalità DTM corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - Self-Hosted</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> La libreria DTM è in hosting sull’istanza Akamai di Adobe all’indirizzo <span class="filepath"> assets.adobedtm.com</span>. </p> <p> L’hosting autonomo è l’approccio consigliato per il caricamento di DTM in quanto fornisce un maggiore controllo delle prestazioni del sito web attraverso il controllo della cache, riducendo le dipendenze degli script di terze parti e un maggiore controllo del processo di pubblicazione. Le librerie DTM possono essere ospitate e gestite tramite l’hosting web o CDN. </p> </td> 
   <td colname="col3"> <p>L’hosting autonomo è l’approccio consigliato per caricare DTM su una pagina. Sebbene l’hosting di DTM tramite la rete CDN Akamai funzioni nella maggior parte dei casi, l’hosting autonomo migliora le prestazioni della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Servizio Experience Cloud ID - Utilizzo di un solo AdobeOrg</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/id-service/using/intro/id-request.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>In una normale implementazione MCID, deve essere utilizzato un solo AdobeOrg. </p> </td> 
   <td colname="col3"> <p>Verifica l’esistenza di più ID AdobeOrg per questa implementazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Posizionamento callback pageBottom</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>Platform Launch deve avere una funzione di callback <span class="codeph">pageBottom </span>definita per ultima nel corpo della pagina, se implementato in modo sincrono. </p> <p> <p>Nota: è consigliabile che il tag sia l’<i>ultimo</i> tag presente in <span class="codeph"> &lt;body&gt;</span>. Se si trova all’interno del tag <span class="codeph"> &lt;body&gt;</span>, potrebbe funzionare, ma non è ugualmente consigliabile in quanto potrebbe generare malfunzionamenti o risultati indesiderati. </p> </p> </td> 
   <td colname="col3"> <p>Aggiungi lo script in linea immediatamente prima del tag <span class="codeph"> &lt;/body&gt;</span> di chiusura per garantire la funzionalità DTM corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Self-Hosted</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>La libreria Platform Launch è ospitata nell’istanza Akamai di Adobe all’indirizzo <span class="filepath"> assets.adobedtm.com</span>. </p> <p>L’hosting autonomo è l’approccio consigliato per il caricamento di Platform Launch in quanto fornisce un maggiore controllo delle prestazioni del sito web attraverso il controllo della cache, riducendo le dipendenze degli script di terze parti e un maggiore controllo del processo di pubblicazione. Le librerie Platform Launch possono essere ospitate e gestite tramite l’hosting web o CDN. </p> </td> 
   <td colname="col3"> <p>Sebbene l’hosting di Platform Launch tramite la rete CDN di Akamai funzioni nella maggior parte dei casi, si consiglia di implementare l’hosting autonomo come primo passo per migliorare le prestazioni della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Deve essere distribuito in modo asincrono</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Platform Launch deve essere implementato in modo asincrono per ottenere prestazioni ottimali. </p> </td> 
   <td colname="col3"> <p>Includi il parametro asincrono nello script in linea per garantire la funzionalità di implementazione asincrona di Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Target - Contenuto in mboxDefault</b> </p> <p>Peso: 0 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il contenuto dovrebbe essere presente in mboxDefault quando si utilizza at.js. </p> </td> 
   <td colname="col3"> <p>Verifica che il contenuto sia disponibile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Configurazione {#configuration}

Questa documentazione fornisce ulteriori informazioni sui test eseguiti da Adobe Experience Platform Auditor per la configurazione.

I test di configurazione eseguono la ricerca di impostazioni, valori o potenziali conflitti specifici nell’implementazione. Platform Auditor valuta i tag rispetto ad altre regole e best practice consigliate.

<table id="table_A8A1FC360482447185C8460A18426638"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Criteri </th> 
   <th colname="col3" class="entry"> Consiglio </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - I nomi di conversione utilizzano solo caratteri alfanumerici</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p>Il parametro <span class="codeph"> ev_conversion_property_name</span> deve contenere solo valori numerici e decimali ECCETTO per il parametro "<span class="codeph"> ev_transid</span>" (il valore <span class="codeph"> ev_transid</span> può contenere valori di testo o numerici) </p> <p>Cerca i pixel <span class="codeph"> everesttech.net</span> che contengono un parametro URL che inizia con <span class="codeph"> ev_</span>. </p> <p>Esempio: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Assicurati che i parametri delle proprietà della transazione contengano solo valori numerici e decimali. </p> <p> <p>Avviso: qualsiasi altro tipo di valore potrebbe causare la perdita di dati. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - I nomi di conversione usano caratteri URL-safe</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p> I nomi delle proprietà di conversione non devono contenere una e commerciale o un punto interrogativo. </p> <p> Esempio: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Assicurati che i parametri della proprietà della transazione non contengano una e commerciale o un punto interrogativo non codificati. Interrompono il formato URL. </p> <p> <p>Avviso: parametri di proprietà che contengono una e commerciale o un punto interrogativo non codificati (ad esempio: <span class="codeph"> ev_formComplete?=1</span> o <span class="codeph"> ev_formComplete&amp;Submit=1</span>), potrebbero causare una perdita di dati. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - ID transazione implementato correttamente</b> </p> <p>Peso: 1 </p> </td> 
   <td colname="col2"> <p> Il nome della proprietà <span class="codeph"> ev_transid=</span> non deve essere vuoto. </p> <p>Esempio: </p> <p> <span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Il nome della proprietà <span class="codeph"> ev_transid=</span> deve necessariamente contenere un valore (<span class="codeph"> ev_transid=</span>). Se lasciato senza valori, potrebbe verificarsi una perdita di dati della transazione. Assegna un valore a <span class="codeph"> ev_transid=</span> o rimuovi il parametro dal pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Istanziato in DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/analytics/implementation/home.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il codice Adobe Analytics non è installato o l’esecuzione non è riuscita. Restituisce 0 se non viene trovato alcun codice Analytics nella pagina web. </p> </td> 
   <td colname="col3"> <p>Verifica che il tag Analytics sia implementato nella pagina e non sia bloccato dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Istanziato una volta</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/analytics/implementation/home.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il codice Adobe Analytics è stato rilevato più di una volta nella pagina. Restituisce 0 se non viene trovato alcun codice Analytics nella pagina web. </p> </td> 
   <td colname="col3"> <p>Accertati che nella pagina sia presente un solo tag Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Ultima versione</b> </p> <p>Peso: 3 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Nelle pagine non è in esecuzione la versione più recente della libreria di codici di Analytics. Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. Restituisce 0 se non viene trovato alcun codice Analytics nella pagina web. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente della libreria Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - I tag di terze parti vengono caricati in modo asincrono dopo l’evento DOM ready</b> </p> <p>Peso: 3 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/resources/load-order.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Per trovare un compromesso tra una buona esperienza utente e la raccolta di dati accurati, i tag di terze parti dovrebbero essere attivati durante l’evento DOM ready. In questo modo gli script di tracciamento verranno eseguiti senza influire sulle funzionalità del sito. </p> </td> 
   <td colname="col3"> <p>Per risolvere questo problema, modifica tutte le regole che eseguono pixel di terze parti in modo che vengano attivate in corrispondenza dell’evento DOM Ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servizio Experience Cloud ID - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/tools/macid.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Nelle pagine non è in esecuzione la versione più recente della libreria di codici del servizio Visitor ID, <span class="codeph"> visitorAPI.js</span>. Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente della libreria del servizio Visitor ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Nelle pagine non è in esecuzione la versione più recente della libreria di codici di Platform Launch (Turbine). Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. </p> </td> 
   <td colname="col3"> <p> Aggiorna la libreria Platform Launch generando e pubblicando nuovamente la libreria Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - Versione più recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/tools/target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Nelle pagine non è in esecuzione la versione più recente della libreria di codici di Target. Le librerie di codici che alimentano le tecnologie Experience Cloud vengono costantemente aggiornate e modificate al fine di trarre vantaggio dai miglioramenti delle prestazioni e fornire le funzionalità più recenti. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente della libreria Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - mboxDefault precede mboxCreate </b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>L’utilizzo corretto di <span class="codeph"> mboxCreate</span> è simile al seguente: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Accertati di includere un tag <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> prima di richiamare <span class="codeph"> mboxCreate()</span>. at.js non ne aggiungerà uno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - DOCTYPE valido</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> È stato rilevato un DOCTYPE non valido. In questo scenario non verrà attivata alcuna mbox. </p> <p>Per at.js, il DOCTYPE deve essere in modalità Standard oppure Target non funzionerà. </p> </td> 
   <td colname="col3"> <p>Aggiorna il DOCTYPE nella pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Coerenza tag {#tag-consistency}

Questa documentazione fornisce ulteriori informazioni sui test eseguiti da Platform Auditor per la coerenza dei tag.

I test di coerenza di Platform Auditor rilevano incoerenze tra tutte le pagine digitalizzate. Si tratta di valori o configurazioni che devono essere identici in tutte le pagine del sito per garantire una raccolta accurata dei dati.

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Criteri </th> 
   <th colname="col3" class="entry"> Consiglio </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Versione codice coerente </b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/analytics/implementation/home.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> È stata trovata più di una versione del codice Analytics. </p> </td> 
   <td colname="col3"> <p>Sostituisci tutte le istanze di Analytics con la versione corrente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Presenza tag {#tag-presence}

Questa guida fornisce ulteriori informazioni sui test eseguiti da Platform Auditor per la presenza di tag.

Platform Auditor valuta se il tag esiste e se si trova nella posizione giusta nel codice della pagina.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Criteri </th> 
   <th colname="col3" class="entry"> Consiglio </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Presenza codice</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Il tag Advertising Cloud non è disponibile nel DOM. </p> </td> 
   <td colname="col3"> <p>Implementa il tag di Advertising Cloud utilizzando l’estensione di Advertising Cloud per Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Pixel di segmento implementati</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Aggiorna i pixel del segmento di Advertising Cloud ai nuovi tag di sola immagine di Advertising Cloud. L’utilizzo di tag di segmento AMO obsoleti può causare la perdita di dati. </p> </td> 
   <td colname="col3"> <p>Implementa il pixel del segmento di Advertising Cloud utilizzando l’estensione di Advertising Cloud per Adobe Experience Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Caricato nel DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/analytics/implementation/home.html" format="https" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il tag Adobe Analytics non è stato rilevato. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente di Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> DTM - Libreria caricata</b> </p> <p>Peso: 5 </p> <p>Informazioni aggiuntive: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> Risoluzione dei problemi DTM</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aggiunta di codice intestazione e piè di pagina</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare un oggetto _satellite globale nel DOM. Dynamic Tag Management non installato o non eseguito. </p> </td> 
   <td colname="col3"> <p>Verifica che la libreria DTM sia implementata nella pagina e non sia bloccata dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> DTM - Un codice incorporato</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> I siti di produzione devono caricare solo una libreria DTM. </p> </td> 
   <td colname="col3"> <p>Verifica che nella pagina venga caricata solo la libreria di produzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - Il callback pageBottom esiste in &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il callback <span class="codeph"> _satellite.pageBottom()</span> non è stato trovato all’interno del <span class="codeph"> &lt;body&gt;</span> della pagina, richiesto da Dynamic Tag Management. </p> <p>Il test ha esito negativo se la chiamata <span class="codeph"> pageBottom </span>non viene trovata nella pagina o se si trova nel tag <span class="codeph"> &lt;head&gt;</span> (o in un’altra posizione imprevista). Il test avrà esito positivo solo se <span class="codeph"> pageBottom</span> si troverà all’interno del tag <span class="codeph"> &lt;body&gt;</span>. Se non è presente nella pagina, non funzionerà e anche gli altri due test <span class="codeph"> pageBottom</span> non avranno esito positivo. </p> </td> 
   <td colname="col3"> <p>Aggiungi lo script in linea immediatamente prima del tag <span class="codeph"> &lt;/body&gt;</span> di chiusura per garantire la funzionalità DTM corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - Tag pageBottom attivato</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il tag <span class="codeph"> pageBottom</span> DTM non è stato rilevato. </p> <p>Ciò potrebbe verificarsi se la chiamata si trova all’interno di un’istruzione <span class="codeph"> if</span> che restituisce un risultato simile a <span class="codeph"> if (false) {_satellite.pageBottom()}</span>. Quindi, anche se potrebbe esistere ed essere posizionato correttamente, il tag potrebbe non essere attivato. </p> </td> 
   <td colname="col3"> <p>Installa la chiamata <span class="codeph"> pageBottom</span> DTM su ogni pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servizio Experience Cloud ID - Presenza di codice</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/id-service/using/implementation/implementation-methods.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Codice del servizio Experience Cloud ID non trovato. L’Experience Cloud ID (MCID) è vivamente consigliato per garantire il massimo valore dalle soluzioni Experience Cloud ed è fondamentale per la gestione ID nelle soluzioni Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Installa la versione più recente di MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servizio Experience Cloud ID - Presenza di cookie</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/id-service/using/implementation/implementation-guides.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare il cookie <span class="codeph"> AMCV_</span>. Devi creare un’istanza di un oggetto visitatore dal codice <span class="codeph"> VisitorAPI.js</span>. </p> </td> 
   <td colname="col3"> <p> Se si tratta di un’implementazione DTM, verifica che l’ID AdobeOrg sia stato immesso correttamente nello strumento MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Servizio Experience Cloud ID - Valore MID presente</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/id-service/using/intro/cookies.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il valore MID non è stato trovato nel cookie <span class="codeph"> AMCV_</span>. </p> </td> 
   <td colname="col3"> <p>Esegui di nuovo il test per verificare la presenza di eventuali latenze API MCID. Se la condizione persiste, contatta l’Assistenza clienti Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Launch - Libreria caricata</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Impossibile trovare un oggetto _satellite globale nel DOM. Launch non installato o non eseguito. </p> </td> 
   <td colname="col3"> <p>Verifica che la libreria Platform Launch sia implementata nella pagina e non sia bloccata dalle attività di script successive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Non sono presenti più script incorporati</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Nella pagina non devono essere caricati più script incorporati. I siti di produzione devono caricare una sola libreria Platform Launch. </p> </td> 
   <td colname="col3"> <p>Verifica che nella pagina venga caricata solo la libreria di produzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Il callback pageBottom esiste in &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p> Il callback <span class="codeph"> _satellite.pageBottom()</span> non è stato trovato all’interno della sezione <span class="codeph"> &lt;body&gt;</span> della pagina, richiesto da Platform Launch. </p> <p>Il test ha esito negativo se la chiamata <span class="codeph"> pageBottom </span>non viene trovata nella pagina o se si trova nel tag <span class="codeph"> &lt;head&gt;</span> (o in un’altra posizione imprevista). Il test avrà esito positivo solo se <span class="codeph"> pageBottom</span> si troverà all’interno del tag <span class="codeph"> &lt;body&gt;</span>. Se non è presente nella pagina, non funzionerà e anche gli altri due test <span class="codeph"> pageBottom</span> non avranno esito positivo. </p> </td> 
   <td colname="col3"> <p>Aggiungi lo script in linea immediatamente prima del tag di chiusura <span class="codeph"> &lt;/body&gt;</span> per garantire la funzionalità Platform Launch corretta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Il callback pageBottom non deve esistere quando viene distribuito in modo asincrono</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/launch/using/intro/get-started/quick-start.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Il callback <span class="codeph"> _satellite.pageBottom()</span> è stato trovato nella pagina. Ciò non dovrebbe accadere quando Platform Launch è implementato in modo asincrono. </p> </td> 
   <td colname="col3"> <p>Rimuovi lo script<span class="codeph"> _satellite.pageBottom()</span> per abilitare la funzionalità Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Target - Presenza di codice</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> </td> 
   <td colname="col2"> <p>Target deve essere definito nel DOM. </p> </td> 
   <td colname="col3"> <p>Installa la versione più recente di Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Target - Libreria caricata in &lt;head&gt;</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/it-IT/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informazioni aggiuntive</a> </p> 
    <!--
      TE61c380082a4b4706b28a84aa047599a7 
    --> </td> 
   <td colname="col2"> <p> La libreria Target deve essere caricata nel tag <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
   <td colname="col3"> <p> Verifica che la libreria Target sia caricata nel tag <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
