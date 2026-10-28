# Brief: Landing page AikoTouch (Messico + Italia)

## Chi sono
Sono Gianni, proprietario di AikoTouch. Non sono uno sviluppatore: spiegami ogni passaggio in italiano semplice, un passo alla volta, e aspetta la mia conferma prima di andare avanti.

## Obiettivo
Aggiungere al progetto (Vite + React + Tailwind, Supabase, Vercel) la landing page pubblica che apparirà su aikotouch.com. È la pagina dove arrivano i clienti dai social e dai volantini per richiedere il loro evento.

## Riferimento grafico
Il file `landing-prototipo.html` in questa cartella è il prototipo approvato. È scritto in un formato di template (`{{...}}`, `sc-if`, `sc-for`, e una classe JavaScript in fondo con stato e testi). Riproducilo fedelmente in React: stessi colori, caratteri (Italiana + Jost da Google Fonts), spaziature, testi in spagnolo e italiano e comportamento.

## Requisiti
- Lingua predefinita spagnolo, switch ES / IT in alto a destra.
- Tutto deve stare in una sola schermata, anche sul telefono, senza scroll.
- Quattro schermate: inizio → modulo → pagamento → conferma.
- Modulo: tipo di evento (XV años/Quinceañera, Boda/Matrimonio, Bautizo/Battesimo, Primera Comunión/Prima Comunione, Cumpleaños/Compleanno, 18 años/18 anni, Otro/Altro con campo libero), nome o nomi dei festeggiati, data dell'evento, nome di chi ordina, telefono WhatsApp, email (obbligatoria), accettazione privacy (obbligatoria).
- Prefisso telefono: +52 di default in spagnolo, +39 in italiano. Se il cliente cambia lingua, il prefisso segue la lingua, a meno che non l'abbia scelto a mano. Menu con MX, IT, US, ES, CO, AR e "Otro país/Altro paese" con campo per scrivere il prefisso a mano.
- Pagamento: per ora solo SIMULATO (il pulsante passa alla conferma). Il prezzo resta segnaposto. Il pagamento vero lo integreremo dopo.
- Il link WhatsApp in fondo porta a https://wa.me/393385927654.
- Logo: se nel progetto c'è già il logo AikoTouch originale (PNG), usa quello al posto della "A" provvisoria.
- Il link alla privacy per ora resta un segnaposto.

## Salvataggio dati
- Quando il cliente preme "Continuar al pago", salva la richiesta in una nuova tabella Supabase (per esempio `richieste_eventi`) con: tipo evento, testo "altro", nomi festeggiati, data evento, nome cliente, prefisso, telefono, email, lingua, data di creazione, stato ("in_attesa_pagamento").
- Sicurezza (RLS): chi visita il sito può solo INSERIRE richieste, mai leggerle o modificarle.
- Prepara tu lo SQL e dammelo da incollare nel SQL Editor di Supabase, spiegandomi dove cliccare.

## Regole importanti
1. Prima di tutto guarda come è organizzato il progetto e dimmi in parole semplici su quali indirizzi stanno oggi le app (Studio, Evento ospite/amministratore).
2. Non rompere nulla di esistente: i link degli eventi devono continuare a funzionare, e ogni evento deve aprire il proprio evento.
3. La landing va sull'indirizzo principale "/". Se oggi "/" è occupato da un'altra app, proponimi una soluzione prima di cambiare.
4. Lavora su un ramo separato (branch), pubblicalo su GitHub e dammi il link di anteprima di Vercel. Non unire al ramo principale finché non approvo io.
