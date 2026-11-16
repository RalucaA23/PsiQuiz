# Curs: Psihologie experimentală — quiz-uri pe capitole

Fișa cursului pentru skill-ul `curs-mindmap-quiz`. Blocul JSON e citit de scripturi; restul e pentru oameni.

Reconstituită pe 16 nov. 2026, fără a regenera conținut: capitolele (`capNN.json`) au fost extrase din pagina publicată `An1_Sem1/Psihologie_experimentala.html`, iar notele de mai jos vin din vechiul `INSTRUCTIUNI-QUIZ.md` (stare la 11 nov., cap. 1–10).

```json
{
  "schema": "quiz-curs-v1",
  "curs": "Psihologie experimentală",
  "manual": "An1_Sem1/Psihologie Experimentala/08.  PSIHOLOGIE EXPERIMENTALA.pdf (local, C:\\Psi)",
  "sursa": "Manual UTM, Facultatea de Psihologie · recapitulare pe capitole și quiz-uri finale",
  "eticheta_capitol": "Capitolul",
  "capitole": [
    {
      "nr": 1,
      "titlu": "Psihologia experimentală. Știință și metodă",
      "pagini": ""
    },
    {
      "nr": 2,
      "titlu": "Metodele psihologiei experimentale",
      "pagini": ""
    },
    {
      "nr": 3,
      "titlu": "Metoda observației",
      "pagini": ""
    },
    {
      "nr": 4,
      "titlu": "Metoda experimentului",
      "pagini": ""
    },
    {
      "nr": 5,
      "titlu": "Probleme etice ale experimentului psihologic",
      "pagini": ""
    },
    {
      "nr": 6,
      "titlu": "Raportul de cercetare",
      "pagini": ""
    },
    {
      "nr": 7,
      "titlu": "Procese senzoriale",
      "pagini": ""
    },
    {
      "nr": 8,
      "titlu": "Procese perceptive",
      "pagini": ""
    },
    {
      "nr": 9,
      "titlu": "Atenția",
      "pagini": ""
    },
    {
      "nr": 10,
      "titlu": "Memoria",
      "pagini": ""
    },
    {
      "nr": 11,
      "titlu": "Învățarea",
      "pagini": ""
    },
    {
      "nr": 12,
      "titlu": "Gândirea și rezolvarea de probleme",
      "pagini": ""
    },
    {
      "nr": 13,
      "titlu": "Motivația",
      "pagini": ""
    },
    {
      "nr": 14,
      "titlu": "Afectivitatea",
      "pagini": ""
    }
  ],
  "runde": {
    "1": {
      "vizibile": 15,
      "ascunse": 5
    },
    "2": {
      "vizibile": 15,
      "ascunse": 5
    }
  },
  "min_exemple_noi": 5,
  "exceptii": {
    "1": {
      "1": {
        "vizibile": 15,
        "ascunse": 5
      },
      "2": {
        "vizibile": 10,
        "ascunse": 5
      }
    },
    "2": {
      "1": {
        "vizibile": 15,
        "ascunse": 5
      },
      "2": {
        "vizibile": 10,
        "ascunse": 5
      }
    },
    "3": {
      "1": {
        "vizibile": 15,
        "ascunse": 5
      },
      "2": {
        "vizibile": 10,
        "ascunse": 5
      }
    },
    "9": {
      "1": {
        "vizibile": 20,
        "ascunse": 10
      },
      "2": {
        "vizibile": 20,
        "ascunse": 10
      },
      "3": {
        "vizibile": 15,
        "ascunse": 0
      },
      "4": {
        "vizibile": 15,
        "ascunse": 0
      }
    }
  },
  "tipuri_extra": [
    "sectiune",
    "senzatie"
  ],
  "test_final": {
    "intrebari": 30,
    "raport_baza_aplicatii": 2,
    "seed": 1
  },
  "pagini": {
    "capitole": {},
    "asamblata": ""
  }
}
```

## De știut despre reconstituire
- `tip` și `exemplu_nou` nu ajung în pagina publicată, deci lipsesc din toate `capNN.json`; `valideaza_capitol.py` le raportează ca erori. Paginile se construiesc fără ele (`build_curs.py` nu le folosește). Se completează doar dacă se revizuiește un capitol.
- Pagina veche avea alt model de quiz-uri finale (4 quiz-uri cu 30 de întrebări, 80% ascunse, alese aleator la fiecare deschidere). La reconstruire se aplică regula actuală a skill-ului: doar întrebările ascunse, fixe, câte 30 pe quiz.
- `cap01.json`–`cap07.json` folosesc încă forma veche a trimiterilor la capitole (scrise înainte de regula „Cap. N (Titlu)”).
- Paginile manualului (`pagini` la fiecare capitol) și ponderea capitolelor nu au fost salvate; se pot completa din PDF.
- Notele pe capitole pentru cap. 11–14 nu au fost păstrate nicăieri pe disc.

## Capitolele cărții
1. Psihologia experimentală. Știință și metodă
2. Metodele psihologiei experimentale
3. Metoda observației
4. Metoda experimentului
5. Probleme etice ale experimentului psihologic
6. Raportul de cercetare
7. Procese senzoriale
8. Procese perceptive
9. Atenția
10. Memoria
11. Învățarea
12. Gândirea și rezolvarea de probleme
13. Motivația
14. Afectivitatea

Notă despre textul extras: titlurile capitolelor 3, 6 și 8 apar scrise „CAPITOLU 3/6/8” (fără L), deci caută după „CAPITOL”. Secțiunea „3. METODELE CERCETĂRII EXPERIMENTALE” stă după bibliografia capitolului 2 și înainte de „CAPITOLU 3 – METODA OBSERVAȚIEI”. În `cap03.json` ea a fost tratată ca parte din capitolul 3.

## Structura capitolelor (istoric)
| Rundă | Vizibile în quiz | Ascunse (doar pentru testul final) |
|---|---|---|
| Runda 1 · Bază | **15** (cap09: **20**) | **5** (cap09: **10**) |
| Runda 2 · Aplicații | **10** la cap01–03; **15** de la cap04 (la cererea utilizatoarei); cap09: **20**. Cel puțin **5 cu exemple noi** (situații inventate, NU exemplele din carte) | **5** (cap09: **10**) |

Total pe capitol: 25 (cap01–03) sau 30 (de la cap04) de întrebări vizibile și 10 ascunse. Excepție: cap09 (Atenția), cel mai consistent capitol din carte, are la cererea utilizatoarei 20 vizibile + 10 ascunse în rundele 1 și 2, plus două runde de extindere cerute ulterior: **Runda 3 · Bază II** și **Runda 4 · Aplicații II**, câte 15 vizibile, fără ascunse (în total 70 vizibile și 20 ascunse; tab-uri: Mind Map | Runda 1 | Runda 2 | Runda 3 | Runda 4). Excepția e trecută în `EXCEPTII` din `valideaza_capitol.py`, care pentru cap09 cere exact rundele 1–4 și tratează rundele 2 și 4 drept runde de aplicații (`exemplu_nou` obligatoriu, minim 5 exemple noi). Capitolele următoare revin la 15/5 și 15/5, dacă utilizatoarea nu cere altfel. Întrebările ascunse sunt noi, nu reformulări ale celor vizibile.

## Tipuri folosite (istoric)
Valorile `tip` folosite până acum: `metoda`, `variabila`, `ipoteza`, `eroare`, `design`, `test`, `definitie`, `instrument`, `etapa`, `autor` (cercetători și filozofi), `curent` (școli și curente; din cap07 și perspectivele de abordare: psihofizică, fiziologică, a percepției umane, cognitivă, a dezvoltării), `istoric` (date și momente), `principiu` (principii etice, din cap05; din cap09 și legi precum legea intrării prealabile), `sectiune` (secțiunile raportului APA, din cap06), `senzatie` (tipurile de senzații și simțuri, din cap07), `model` (modelele teoretice ale percepției, din cap08; din cap09 și modelele atenției: Broadbent, Treisman, Deutsch, multimodal, FIT, Load Theory, Spotlight, Kahneman, Guided Search, modelul cu patru factori, tehnicile lui Hirst; din cap10 și modelele memoriei: Atkinson-Shiffrin, procesarea informațiilor, recunoaștere și amintire, Baddeley, încărcare duală), `fenomen` (fenomene perceptive: iluzii, constanță, percepție subliminală, aprehensiune, din cap08; din cap09 și răspunsul de orientare, obișnuința, orbirea neatențională, vigilența; din cap10 și interferența proactivă/retroactivă, suprimarea), `tulburare` (tulburările atenției, din cap09), `structura` (structuri cerebrale și neurotransmițători, din cap09). Refolosește-le când se potrivesc. Dacă adaugi un tip nou, adaugă-l și în lista `TIPURI` din `valideaza_capitol.py`.

## Note pe capitole
- Capitolul 1 conține și secțiunea 1.2 (metode, ipoteze, variabile, erori, tipuri de experiment), care se suprapune mult cu capitolul 2. `cap01.json` pune accentul pe ce e specific capitolului 1 (definiție și obiective, istorie, precursori, pionieri, curente, contribuții celebre, aplicații) și, din 1.2, pe ce nu testează deja `cap02.json` (experimente exploratorii, regula p < 0,05, variabile în SPSS, erorile metodologice, erorile de tip I/II, experimentul cu mascare, experimentul natural ca alternativă etică). La capitolele următoare, verifică suprapunerile cu capitolele deja făcute.
- Capitolul 3: clasificarea testelor de personalitate apare în carte doar ca titlu („Proiective; Obiective: Categoriale; Dimensionale”). În `cap03.json` a fost interpretată ca „proiective și obiective, iar cele obiective categoriale sau dimensionale” (întrebarea ascunsă din Runda 1 și nodul din Mind Map). De corectat dacă la curs se predă altfel.
- Capitolul 4: definițiile de bază VI/VD/VC, randomizarea și grupul de control sunt deja testate în cap02, iar tipurile de experiment și biosemnalele în cap03. `cap04.json` pune accentul pe ce e specific capitolului: cele 14 etape și ordinea lor, constructele vs definițiile operaționale, validitatea și controlul VI, evaluarea și controlul VD, variabila subiect (reprezentativitate), cele cinci VD favorizate (indicatori fiziologici, răspunsuri motorii, timp de reacție, răspunsuri verbale, experimentul asociativ-verbal) și cuvintele cheie (standardizare, aleatorizare). Experimentul pilot apare aici ca etapa 14, cu rol de testare și ajustare a procedurii. În textul extras, subcapitolul variabilelor e numerotat greșit „1.2” (ar fi 4.2).
- Capitolul 5 e foarte scurt (patru principii, rezumat, cinci cuvinte cheie, întrebări de verificare), deci `cap05.json` îl leagă de capitolele 1–4: experimentul natural și cel invocat ca alternative etice, observarea anonimă ca problemă deontologică (cap03), etica interviului, anamnezei și analizei produselor activității (cap03), comitetul de etică (cap01), formularele de consimțământ din anexe și pilotul (cap04), retragerea și efectul de mortalitate (cap01). În carte, „nedivulgarea” înseamnă dreptul de a nu fi indus în eroare privind scopul studiului, nu nedezvăluirea datelor (aceea e confidențialitatea); quiz-ul folosește sensul din carte și o tratează drept capcană. „Conflictele de interese” apar doar într-o întrebare de verificare. Distractorii vin din cap01–04 (randomizare/aleatorizare, standardizare, fidelitate, validitate, efectul Hawthorne, efectul experimenterului, eroarea de selecție).
- Capitolul 6 e foarte scurt (cele 8 secțiuni APA, rezumat, cinci cuvinte cheie, întrebări de verificare). `cap06.json` testează conținutul fiecărei secțiuni (inclusiv 150–250 de cuvinte la abstract, manipularea VI „dacă este cazul” în metodologie, limitele în discuție, referințele = doar sursele citate, anexele opționale) și, în Runda 2, plasarea unor fraze în secțiunea potrivită. Capcane: „Concluzii” e cuvânt cheie, dar nu una dintre cele 8 secțiuni; „Rezumat” înseamnă și abstractul, și rezumatul capitolului din manual. Legături: corespondența dintre cele 14 etape (cap04) și secțiuni (interpretare de studiu, nu apare explicit în carte), replicarea și 1.2.7 prelucrarea/interpretarea/generalizarea (cap01, inclusiv eroarea de generalizare), transparența și confidențialitatea în raportare (cap05), G. Stanley Hall, primul președinte APA (cap01). Distractorii vin din cap01–05 (bibliografia și pilotul, protocolul de observație, fidelitate/etalonare, p < 0,05, eroarea de tip I, Hawthorne, mortalitate, comitetul de etică, principiile etice). Tip nou: `sectiune`.
- Capitolul 7 are 7 secțiuni (perspective, psihofizică, praguri și metode, scale, variabile, tipuri de senzații, tehnici și aparatură), rezumat, cinci cuvinte cheie (percepție, simțuri, transducție, adaptare senzorială, percepție subliminală) și întrebări de verificare. Suprapuneri: variabilele (VI/VD, controlul) sunt deja în cap02 și cap04, deci `cap07.json` testează doar exemplul cu alcoolul și memoria, variabilele de confuzie (oboseala) și rolul controlului în studiul senzațiilor; interviul, chestionarele, observația și testele sunt în cap03, deci din „Tehnici și aparatură” se testează doar IRM/PET, EEG și biofeedback. Particularități ale cărții: pragul absolut și cel diferențial sunt doar numite, fără definiție (harta dă sensul uzual și leagă JND de pragul diferențial); metoda constantă e descrisă ca „un stimul ținut constant, altul variat până la o schimbare raportată”, deci aproape la fel ca „compararea cu standardul” (quiz-ul nu le pune niciodată una împotriva celeilalte când situația s-ar potrivi cu amândouă); în carte, metoda de ajustare măsoară pragul absolut. Perspectivele folosesc `tip` = `curent`. Distractorii vin din cap01–05 (Helmholtz, Wundt, Ebbinghaus, curba uitării, gestalt, condiționarea operantă, Hawthorne, p < 0,05, variabile nominale/ordinale, variabila de control, studii longitudinale/transversale, fidelitate, etalonare, EMG, EDR, EOG/ERG, timpul de reacție, aleatorizarea, nedivulgarea). Tip nou: `senzatie`.
- Capitolul 8: secțiunile 7 (variabile și control) și 8 (tehnici și aparatură) repetă mult din cap02–04, iar pașii metodologiei din 8.2 seamănă cu etapele din cap04; `cap08.json` pune accentul pe ce e specific: bottom-up vs top-down, cele cinci modele (empiric-senzorial, constructiv-alternativ, modular, ierarhic, dual-stream, cu capcana dorsal/ventral inversat), paradigmele (directă/indirectă, înnăscută/dobândită, factori comportamentali; cartea doar le enumeră), percepția subliminală, diferențele individuale, genetice/biologice și socio-culturale, particularitățile stimulilor (intensitate, durată, frecvență, formă și structură, contrast, context și fundal), iluziile Müller-Lyer, Ponzo și Rubin (relația formă-fond), constanța (culoare, dimensiune, formă, distanță), percepția mișcării, aprehensiunea perceptivă (cartea dă două definiții: estimarea dimensiunilor și distanțelor fără măsurare directă, în dezvoltare, și evaluarea și reacția rapidă, în rezumatul secțiunii; quiz-ul o folosește pe prima), cele trei categorii de variabile ale studiilor perceptive, tehnicile specifice (fMRI, PET, VR, eye-tracker) și cuvintele cheie (percepție, recunoaștere, organizare perceptivă, Gestalt, iluzii). Legături: observația directă/indirectă și testele proiective (cap03) ca distractori, nedivulgarea în studiile subliminale (cap05), curentul gestaltist (cap01), VI/VD/VC și variabila subiect (cap02, cap04). Cap08 și cap07 au fost lucrate în paralel: percepția subliminală, cu scenariul celor 10 ms și cu nedivulgarea, e deja testată în `cap07.json`, deci `cap08.json` o păstrează doar ca definiție în Runda 1; conceptele din cap07 (adaptarea senzorială, transducția, pragul absolut, discriminarea senzorială) apar în cap08 doar ca distractori. Corespondența empiric-senzorial ≈ bottom-up și constructiv-alternativ ≈ top-down e o interpretare de studiu, marcată ca atare în Mind Map. Tipuri noi: `model`, `fenomen`.
- Capitolul 9 e cel mai lung din carte (linii ~3255–4983 în textul extras) și are două părți: partea 1 (știința cognitivă a atenției: tipuri 1.1–1.5, constrângeri, conștiință, modelul neuropsihologic cu patru factori, repere istorice 1.2, fundamentele cognitive 1.3 cu Shannon-Weaver, Broadbent, ascultarea dihotică, Hirst, concluzii, modelele selecției) și partea 2 (2.1–2.27, secțiuni scurte de tip enciclopedic: definiții și tipuri, istoric, psihologia cognitivă, intenția și atenția executivă, răspunsul de orientare, electrofiziologie, mecanisme neurale, modelele 2.11, tulburări 2.12–2.18, evaluare clinică 2.19, modele neuropsihologice 2.20, conștientizare 2.21, constrângeri neuronale, neuroimagistică, abordări computaționale), apoi rezumat, 20 de cuvinte cheie și 12 întrebări. Textul conține referiri la „proiect” (antrenarea atenției prin EEG, RV/RA și biofeedback), păstrate în hartă doar ca context. `cap09.json` (20+10 / 20+10) acoperă: definiția și cele 4 elemente, funcțiile (metafora diafragmei camerei – capcană față de Spotlight), tipurile cu exemplele din carte (radio/melodie, dactilograf, paznic, efort fizic extrem; alternanta din 2.1; exogenă/endogenă din cuvintele cheie), cele 4 constrângeri, modelul cu patru factori și componentele lui, reperele istorice (Wundt, Titchener, James, behaviorismul, Gestalt, Descartes, Locke), Shannon-Weaver (niveluri A/B/C și schema), Broadbent, ascultarea dihotică și umbrirea, Neisser, Navon, Moray, vigilența, legea intrării prealabile, tehnicile lui Hirst, modelele de selecție (filtru, atenuare, Deutsch, multimodal, orbirea neatențională) și cele din 2.11 (FIT, Load, Spotlight, Kahneman, Guided Search), RO exogen/endogen și obișnuința, EEG/MEG/ERP-P300, fMRI/PET/sMRI, structurile și neurotransmițătorii, tulburările (neglijență, agnozie asociativă, psihiatrice, de dezvoltare) și evaluarea clinică (anamneză vs interviu), atenția deschisă și nejudicătoare. Particularități ale cărții: „atenție selectivă (concentrată)” e un singur titlu, dar textul distinge concentrata de selectivă, iar cuvintele cheie definesc concentrata și prin durată – quiz-ul nu le pune una împotriva celeilalte și nu opune concentrata susținutei; 2.20 atribuie lui Kahneman și „atenția duală” (Sistemul 1/2), consemnată doar în hartă. Suprapuneri: percepția subliminală (cap07, cap08) apare doar ca distractor și ca legătură cu modelul lui Deutsch; bottom-up/top-down (cap08, acolo perceptive) e testat aici ca tip de control al atenției; fMRI/PET (cap08) și EEG/biofeedback (cap07) apar aici cu ce e specific atenției (benzile EEG, MEG, P300, fluxul sanguin vs glucoza). Distractorii vin din Cap. 1, 3, 7 și 8 (transducția, adaptarea senzorială, pragul absolut și diferențial, percepția, Gestalt și figura-fond, behaviorismul, condiționarea operantă, Hawthorne, EDR/EMG, anamneza). Tipuri noi: `tulburare`, `structura`. Primul capitol scris după regula trimiterilor „Cap. N (Titlu)”. Extinderea cerută ulterior (Runda 3 · Bază II, Runda 4 · Aplicații II, câte 15, 14 exemple noi în Runda 4) acoperă ce nu testau rundele 1–2: cei cinci factori ai interesului, atenția ineficientă, Descartes, originea Gestalt (raționalismul german, Kant), definiția comunicării la Shannon și Weaver, sistemul P al lui Broadbent, Moray, limitele și moștenirea cronometrică a cercetării timpurii, intenția (2.5), procesarea serială, divertismentul atențional (capcana sensului cotidian), SRA, striatumul, conectivitatea funcțională; în aplicații: inhibiția (sarcină de tip go/no-go), factorii energetici vs structurali, absența cererii cognitive, segregarea (Hirst), nivelul C al lui Shannon și Weaver, experimentul lui Treisman cu poveștile schimbate între urechi, EDA pentru RO, RO endogen, Load Theory, atenția duală a lui Kahneman, Parkinson ca tulburare neurologică, asomatognosia vs neglijența, monitorizarea tratamentului, modelele computaționale de saliență, recompensa dopaminergică. Pentru ele au fost adăugate în hartă nodurile „Divertismentul și switching-ul atențional”, „Intenția, selecția răspunsului și atenția executivă”, „Constrângeri neuronale (2.22)”, „Rețele neuronale și conectivitate funcțională”. În `cap09.json`, rundele de extindere au `id` "3" și "4" și `ascunse: []`; pentru o eventuală nouă extindere, pornește de la ele. Distractori noi din Cap. 10 (Memoria): bucla fonologică.
- Capitolul 10 e scurt (linii ~4983–5278 în textul extras): 6 secțiuni (modelele de abordare experimentală; formele memoriei; variabile experimentale și controlul lor; generalizarea rezultatelor; uitarea, interferența și suprimarea; tehnici, procedee, aparatură), rezumat, cinci cuvinte cheie (memorie senzorială, de scurtă durată, de lungă durată, codificare, recuperare) și cinci întrebări. Fiecare secțiune începe cu un rezumat în puncte, apoi îl reia pe larg. `cap10.json` (15+5 / 15+5, toate cele 15 vizibile din Runda 2 cu exemple noi) acoperă: cele trei procese, cele cinci modele (Atkinson-Shiffrin 1968, procesarea informațiilor, recunoaștere vs amintire, Baddeley 1974 cu bucla fonologică / schimbul vizuo-spațial / sistemul executiv, încărcarea duală Baddeley-Hitch 1974), formele memoriei și duratele lor, episodică/semantică/procedurală, variabilele specifice memoriei (tipul și modalitatea prezentării, sarcinile, trăsăturile subiecților), confundantele numite (vârstă, sex, educație), standardizarea, generalizarea internă vs externă, factorii și limitele generalizării, interferența proactivă vs retroactivă, suprimarea, paradigmele (recunoaștere/recuperare, învățare asociativă, memorie de lucru), SPSS/R/MATLAB și eye-trackerul. Particularități ale cărții: textul numește „modelul modal” modelul lui Baddeley cu bucla fonologică (în literatură, „modelul modal” e de obicei Atkinson-Shiffrin) – quiz-ul nu întreabă niciodată după eticheta „modal”, doar după conținut, iar harta notează discrepanța; memoria de lucru e tratată ca sinonimă cu memoria de scurtă durată; durata memoriei senzoriale e „fracțiuni de secundă – câteva secunde” în text și „sub o secundă” în cuvintele cheie (quiz-ul nu le opune); uitarea retroactivă/proactivă și interferența retroactivă/proactivă au aceleași definiții, deci nu sunt puse una împotriva celeilalte; titlul secțiunii 5 e scris „Uitarea, interferența și uitare” (al treilea termen e suprimarea); „generalizarea internă” are în carte un sens propriu (extinderea la alte aspecte ale aceleiași populații), folosit ca atare; întrebarea de verificare 4 despre „recurență” nu are acoperire în text și nu e testată. Suprapuneri: VI/VD, randomizarea și controlul sunt deja în cap02 și cap04, deci se testează doar exemplele și listele capitolului (stresul ca VI, modalitatea prezentării, confundantele numite, standardizarea într-un scenariu); interviurile, chestionarele, testele și observația sunt în cap03 și apar doar ca distractori; EEG/fMRI/PET sunt în cap07–09 și nu sunt retestate. Legături în hartă: Ebbinghaus și curba uitării, Loftus și falsele amintiri, eroarea de generalizare (Cap. 1), atenția ca sinonim al memoriei de scurtă durată (Cap. 9), exemplul alcool–memorie (Cap. 7), experimentul asociativ-verbal (Cap. 4, capcană față de paradigma de învățare asociativă). Distractorii vin din Cap. 1, 2, 3, 4, 5, 7, 8 și 9 (transducția, adaptarea senzorială, pragurile, metodele psihofizice, particularitățile stimulilor, selecția senzorială, filtrul lui Broadbent, Spotlight, obișnuința, ascultarea dihotică, observația, fidelitatea și etalonarea, variabila subiect, nedivulgarea, Hawthorne, erorile de tip I/II, eroarea de generalizare). Fără tipuri noi.
- Capitolele 11–14: note nesalvate (vezi „De știut despre reconstituire”).

## Teme testate
- Capitolul 1: Wundt și laboratorul de la Leipzig, precursori: Fechner, Helmholtz, Ebbinghaus, curentele psihologiei, contribuții celebre, obiectivele (domenii studiate), diferențierea de alte ramuri, experimente exploratorii, decizia asupra H0 (p < 0,05), variabile în SPSS, erori metodologice, erori statistice (tip I / tip II), tipuri de experiment, rădăcini filozofice, experimentul natural, controlul variabilelor, erori accidentale vs metodologice, test vs experiment
- Capitolul 2: metodele principale, comparația metodelor: control, comparația metodelor: fezabilitate, cerințele ipotezei, H0 vs H1, teste statistice, VI vs VD vs VC, tipuri de variabile, erori accidentale vs metodologice, tipuri de design, test vs experiment, cuvinte cheie, controlul variabilelor, tipuri de teste, comparația metodelor: interacțiune, etapele prelucrării datelor, etapele testării ipotezelor, identificarea metodei, rolul randomizării, comparația metodelor: generalizare, tipuri de erori, abordarea mixtă, grup experimental vs grup de control, limitele observației
- Capitolul 3: tipuri de observație, experimentul de confirmare, experimentul de explorare, experimentul psihopedagogic, tipuri de interviu, convorbirea și interviul, ancheta psihologică, metoda biografică, calitățile testului, biosemnale psihofiziologice, modelare și simulare, conduita expresivă, verbală, reflexivă, metodele psihologiei experimentale, metoda genetică și comparată, teste de personalitate, aspectele particulare ale observației, avantajele și provocările observației, analiza produselor activității, experimentul invocat (cvasi-experimentul), experimentul pilot, experimentul de laborator vs natural, protocolul observației
- Capitolul 4: Ordinea etapelor, Lucrările de referință, Obiectivele cercetării, Constructele măsurate, Definițiile operaționale, Alegerea metodei, Bibliografie și anexe, Experimentul pilot, Rolul controlului, Validitatea VI, Evaluarea VD, Controlul VD, Variabila subiect, Indicatori fiziologici, Experimentul asociativ-verbal, Timpul de reacție, Standardizare, Răspunsurile verbale, Controlul VI, Reprezentativitate, Ipotezele cercetării, Limitele cercetării, Definiția metodei, Răspunsurile motorii
- Capitolul 5: Consimțământul informat, Elementele informării, Nedivulgarea, Libertatea de a se retrage, Confidențialitatea, Stocarea și protecția datelor, Protecția împotriva consecințelor dăunătoare, Evaluarea riscurilor, Asistență și resurse, Minimizarea daunelor, Integritatea datelor, Principalele probleme etice, Participanți umani și animale de laborator, Coduri etice și protocoale instituționale, Scopul eticii în experiment, Observarea anonimă, Protecția participanților, Comitetul de etică, Etica în celelalte metode, Conflictele de interese, Retragerea și efectul de mortalitate, Experimentul invocat ca alternativă etică, Transparența în raportare, Anonimatul
- Capitolul 6: Raportul de cercetare, Stilul APA, Pagina de titlu, Lungimea rezumatului, Rezumatul (Abstract), Introducerea, Justificarea și literatura, Metodologia, Detaliile metodologiei, Rezultatele, Discuția, Limitele și cercetările viitoare, Referințele, Anexele, De ce structura standard, Concluziile, Ordinea secțiunilor, Stil clar și concis, Etapele experimentului în raport, Replicarea, Tabele și figuri, Transparența și confidențialitatea în raport, Prelucrarea și interpretarea datelor, Rezultate vs discuție
- Capitolul 7: Senzațiile ca procese psihofizice, Perspectivele abordării experimentale, Fechner și legea Weber-Fechner, Legile psihofizice, Discriminarea senzorială, Pragurile senzoriale, Metodele de măsurare a pragurilor, Transducție, Scala numerică și scala analoagă vizuală, Măsurarea variabilelor complexe, Variabile de confuzie, Propriocepție vs kinestezie, Percepție, Simțurile chimice: olfactiv și gustativ, EEG, Imagistica cerebrală (IRM, PET), Scalare vs raportare (JND), Pragul absolut vs pragul diferențial, Adaptare senzorială, Percepție subliminală, Controlul variabilelor, Detectarea schimbărilor în timp, Senzații cutanate, Biofeedback, Variabilele experimentale, Echilibru și sistemul vestibular, Standardizarea evaluării
- Capitolul 8: Bottom-up vs top-down, Modelul constructiv-alternativ, Modelul dual-stream, Modelul perceptual modular, Paradigmele metodologice, Percepția subliminală, Diferențele individuale, Factorii genetici și biologici, Frecvența, Contextul și fundalul, Iluzia Müller-Lyer, Constanța perceptivă, Tipuri de constanță, Aprehensiunea perceptivă, Tehnici specifice percepției, Modelul proceselor ierarhice, Iluzia Rubin, Variabilele în studiile perceptive, Recunoaștere, Forma și structura, Iluzia Ponzo, Contrastul, Factorii socio-culturali, Controlul variabilelor, Iluziile perceptive, Senzorial vs perceptiv, Gestalt, Percepția mișcării, Evaluarea și intervenția, Intensitatea, Replicarea și generalizarea
- Capitolul 9: Definiția atenției, Elementele esențiale ale atenției, Funcțiile atenției, Atenția nu e un proces unitar, Atenția selectivă (concentrată), Atenția distributivă (divizată), Atenția susținută, Atenția executivă (focusată către un scop), Atenția alternantă, Atenția exogenă și endogenă, Viteza de procesare și resurse, Modelul neuropsihologic cu patru factori, Selecția senzorială, Capacitatea de concentrare, Wundt, Titchener (structuralism), Shannon și Weaver (1949), Ascultarea dihotică, Modelul filtrului (Broadbent), Modelul de atenuare (Treisman), Răspunsul de orientare (RO), MEG, Potențiale evocate (ERP) și P300, Neglijența spațială unilaterală, Tehnicile lui Hirst pentru sarcini duble, Load Theory (Lavie), James (funcționalism), Executiv – selecția și controlul răspunsului, Neurotransmițătorii, Behaviorismul și atenția, Modele de selecție târzie (Deutsch), Modelul multimodal (Johnston și Heinz), Obișnuința și sensibilizarea, Neuroimagistica atenției, Agnozia asociativă, Evaluarea clinică, Controlul top-down și bottom-up, Modelul Spotlight (Posner), Feature Integration Theory (FIT), Resource Model (Kahneman), Orbirea neatențională, Vigilența (Broadbent, Parasuraman), Legea intrării prealabile, Comutarea activă, Electroencefalografia (EEG), Tulburări psihiatrice ale atenției, Tulburări de dezvoltare ale atenției, Conștientizare și atenție autodirecționată, Neisser, De ce a crescut interesul (5 factori), Conștiință și conștientizare, Descartes și Locke, Gestalt, Broadbent (1958), Moray și Navon, Concluziile cercetării timpurii, Intenția, selecția răspunsului și atenția executivă, Procesare paralelă și serială, Divertismentul și switching-ul atențional, Constrângeri neuronale (2.22), Structuri cerebrale, Rețele neuronale și conectivitate funcțională, Atenția susținută (ca factor), Tulburări neurologice și factori de risc, Tulburări ale atenției senzoriale selective (2.12), Abordări computaționale
- Capitolul 10: Codificare, stocare, recuperare, Modelul Atkinson-Shiffrin, Modelul lui Baddeley (1974), Modelul de recunoaștere și amintire, Modelul de procesare a informațiilor, Modelul de încărcare duală (Baddeley și Hitch), Memoria senzorială, Memoria de scurtă durată (de lucru), Memoria semantică, Variabilele în studiul memoriei, Variabile confundante, Generalizarea internă și externă, Factori care influențează generalizarea, Interferența proactivă și retroactivă, Suprimarea, Paradigme experimentale ale memoriei, Memoria procedurală, Limitările generalizării, Software de analiză a datelor, Memoria episodică, Controlul variabilelor, Aparatura specializată, Variabile independente și dependente
- Capitolul 11: Definiția învățării, Învățarea dintr-o încercare, Repetiție și consolidare, Automatizarea și habituarea, Cunoaștere explicită și implicită, Conexionismul (Thorndike), Condiționarea clasică (Pavlov), Condiționarea prin contiguitate (Guthrie), Condiționarea și formarea deprinderilor (Hull), Condiționarea instrumentală (Miller și Konorski), Învățarea prin intuiție (Köhler), Învățarea cognitivă, Generalizare și discriminare, Variabilele în studiul învățării, Paradigme experimentale ale învățării, Învățarea socială, Recompensă și pedeapsă, Cele cinci aspecte ale învățării dintr-o încercare, Aparate și tehnologii, Condiționarea operantă (Skinner), Învățarea conceptuală, Controlul variabilelor, Feedback-ul în cele două forme, Legături cu alte capitole
- Capitolul 12: Definiția gândirii și rezolvării de probleme, Paradigmele experimentale, Studii de laborator, Studii comparative, Modele computaționale, Variabilele în studiul rezolvării de probleme, Variabile confundante, Variabile controlate, Design experimental adecvat, Verbalizarea gândurilor, Validarea și triangularea datelor, Definiția incubației, Factori care influențează incubația, Heuristici, Obiectivitate, Studii de teren, Monitorizarea progresului în terapie, Creativitate, Tehnici care stimulează incubația, Etapele rezolvării de probleme, Studii de neuroimagistică, Gândire conștientă și procese inconștiente
- Capitolul 13: Definiția motivației, Motivația intrinsecă, Motivația de putere, Motivația biologică, Ierarhia nevoilor (Maslow), Teoria autodeterminării (Deci și Ryan), Teoria așteptărilor (Vroom), Teoria stimulării cognitive (White), Teoria stimulilor și răspunsurilor (Skinner), Factori biologici, Factori psihologici, Crește performanța și productivitatea, Obiective SMART, Înțelegerea nevoilor și așteptărilor, Motivația de realizare, Factori externi, Stimulează dezvoltarea personală, Echilibrul muncă–viață personală, Genetică și moștenire, Motivația extrinsecă, Motivația socială, Factori sociali, Erori de interacțiune, Oferirea de feedback și susținere, Motivația și atenția (paznicul), Factori interni, Promovarea autonomiei și responsabilității
- Capitolul 14: Definiția afectivității, Emoția, Manipularea variabilelor, Starea afectivă, Reglarea emoțională, Reglare vs inteligență emoțională, Tulburările afective, Scala STAI, Măsurarea fiziologică, Dubla natură: definiție, Observația comportamentală, Testele de laborator pentru inducerea emoțiilor, Studiile neuroimagistice, Definiția modelării, Nivelul de aspirație, Beneficii și limitări ale simulării, Motivația și afectivitatea ca VC, Modelarea și frustrarea, Auto-raportarea, Emoție vs stare afectivă, Inteligența emoțională, Modelarea și agresivitatea, Modelarea și conflictul, Definiția comportamentului simulat, Validitatea ecologică, Motivația și afectivitatea ca VD, Trebuința de stimulare și de performanță, Paradigmele experimentale ale afectivității, Modelare vs metoda modelării și simulării

## Starea curentă
- [x] cap01 (v3: Mind Map cu 8 ramuri + tabel al curentelor, 15+10 vizibile, 5+5 ascunse, 8 exemple noi în Runda 2)
- [x] cap02 (v3: Mind Map, 15+10 vizibile, 5+5 ascunse)
- [x] cap03 (v3: Mind Map cu 8 ramuri + tabel al tipurilor de experiment, 15+10 vizibile, 5+5 ascunse, 8 exemple noi în Runda 2)
- [x] cap04 (v3: Mind Map cu 7 ramuri + tabel al celor 14 etape, 15+15 vizibile, 5+5 ascunse, 12 exemple noi în Runda 2, distractori din cap01–03)
- [x] cap05 (v3: Mind Map cu 8 ramuri + tabel al principiilor etice, 15+15 vizibile, 5+5 ascunse, 12 exemple noi în Runda 2, distractori din cap01–04; tip nou `principiu`)
- [x] cap06 (v3: Mind Map cu 8 ramuri + tabel al celor 8 secțiuni APA × etapele din cap04, 15+15 vizibile, 5+5 ascunse, 14 exemple noi în Runda 2, distractori din cap01–05; tip nou `sectiune`)
- [x] cap07 (v3: Mind Map cu 8 ramuri + 3 tabele: perspectivele, metodele de măsurare a pragurilor, tipurile de senzații; 15+15 vizibile, 5+5 ascunse, 14 exemple noi în Runda 2, distractori din cap01–05; tip nou `senzatie`)
- [x] cap08 (v3: Mind Map cu 8 ramuri + tabel al celor 5 modele, 15+15 vizibile, 5+5 ascunse, 12 exemple noi în Runda 2, distractori din cap01–05 și cap07; tipuri noi `model`, `fenomen`; trimiteri actualizate la „Cap. N (Titlu)”)
- [x] cap09 (v3, excepție la cerere: 20+20 vizibile, 10+10 ascunse, plus extinderea Runda 3 · Bază II și Runda 4 · Aplicații II cu 15+15 vizibile, fără ascunse – 70 vizibile în total; Mind Map cu 8 ramuri + 2 tabele: tipurile de atenție, modelele atenției; 17 + 14 exemple noi în rundele de aplicații, distractori din cap01, cap03, cap07, cap08, cap10; tipuri noi `tulburare`, `structura`; primul cu trimiteri „Cap. N (Titlu)”)
- [x] cap10 (v3: Mind Map cu 8 ramuri + 2 tabele: modelele memoriei, formele memoriei × durată; 15+15 vizibile, 5+5 ascunse, 15 exemple noi în Runda 2, distractori din cap01–05 și cap07–09; fără tipuri noi; trimiteri „Cap. N (Titlu)”)
- [x] cap11 (din pagina publicată: Mind Map cu 8 ramuri, R1 15+5, R2 15+5; note pe capitol nesalvate)
- [x] cap12 (din pagina publicată: Mind Map cu 8 ramuri, R1 15+5, R2 15+5; note pe capitol nesalvate)
- [x] cap13 (din pagina publicată: Mind Map cu 8 ramuri, R1 15+5, R2 15+5; note pe capitol nesalvate)
- [x] cap14 (din pagina publicată: Mind Map cu 8 ramuri, R1 15+5, R2 15+5; note pe capitol nesalvate)
- [x] Pagina asamblată (publicată; de reconstruit din aceste surse cu `psiquiz.py build psi_exp`)
