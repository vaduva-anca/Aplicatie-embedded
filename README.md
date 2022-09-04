# Aplicatie-embedded
Aplicația va respecta următoarele specificații:
• Temperatura este achiziționată la fiecare X ms în Taskul T1.
• Taskul T2 va controla servomotorul astfel:
▪ Servomotorul este în poziție centrală atunci când temperatura este cuprinsă 
între 20 și 25 C. 
▪ Servomotorul se va deplasa către stânga pentru valori < 20 C și către dreapta 
pentru valori > 25 C
• Taskul T2 se va executa le fiecare Y ms. Unde Y > X
• Taskul T3 va primi valorile achiziționate și le va trimite către interfața serială 
respectând următorul format: temperatura: val C unde val este temperatura citită
• Pe lângă modul automat de comandă, aplicația va pune la dispoziție și un mod manual 
de comandă folosind un potențiometru.
• Schimbarea modului (automat / manual) se va face folosind un switch conectat la un 
pin cu întrerupere externă.
• În modul manual de funcționare, T1, T2 și T3 sunt suspendate și se va activa T4 care 
va comanda servomotorul și, de asemenea, va trimite către portul serial: mod manual. 
• Când se comută din manual în automat, T4 este suspendat și T1,T2, T3 sunt activate.
• Comunicarea între taskuri se va face folosind cozi (queue). 
• Opțional: Modul de funcționare (automat / manual) se va semnaliza folosind un LED 
(de preferat LED-ul integrat pe placa de dezvoltare (LED_BUILDIN).
