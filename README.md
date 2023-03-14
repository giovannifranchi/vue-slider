VUE SLIDER

Partendo dal markup della versione svolta in js plain, rifare lo slider ma questa volta usando Vue.


//Dentro le proprietà di return dell'oggetto di createApp si setta imgObj = sliders array
//Si Crea inoltre una variabile di stato che indicherà l'elemento dell'array di sliders da prendere in cosiderazione
//Fra i methods si aggiunge un prevImg che diminuisce di 1 la variabile di stato e se la variabile di stato è minore di 0 va allla lunghezza dell'array - 1 
//Si aggiunge il metodo nextImg che incrementa la vartiabile di stato fino a quando la medesima è inferiore a lunghezza di array - 1 e altrimenti va a 0
//Si aggiunge metodo goToImg che setta al click la vartiabile di stato uguale all'indice dell'immagine che si è presa in considerazione
//Si aggiunge un metodo stopInterval che prende stoppa l'intervallo
//Si aggiunge un metodo startInterval che fa partire un intervallo che richiama il metodo nextImg
//Nella sezione mounted si aggiunge un intervallo che richiama la funzione nextImg per far partire l'intervallo appena l'app è renderizzata
//Dentro l'html si setta nella sezione img principale dentro il src il valore di imgs all'indice active e alla chiave image
//Dentro l'h3 si mette valore di img all'indice active in chiave titolo e la stessa operazione si ripete per il p con chiave text
//Si eliminano tutti i div di thubnails tranne uno e si rimuove la classe active
//Si fa un v-for per sul div per quanto sono le imgs e si dice che la classe in v-bind è active solo se l'indice corrisponde alla variabile di stato e dentro la source si mette solo la variabile img.image, e si dice che al click scatenano la funzione goToImg
//Alle frecce si aggiunge la funzione al click go to prev e go to next
//Al div img principale si dice con v-on:mouseover che venga invocata la funzione stopInterval mentre al v-on:mouseleave la funzione startInterval