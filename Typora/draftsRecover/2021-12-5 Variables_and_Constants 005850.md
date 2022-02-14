# 06 - Variables and Constants

Una variabile è un'astrazione di un indirizzo di memoria.

Ogni variabile ha un tipo e un valore e va dichiarata prima di essere usata

```cpp
double name;
```

**NB:** Non puoi ricichiarare un nome nello stesso scope

Sii consistente con il nome delle variabili: MyVariableName vs my_variable_name

Dichiara le variabili sempre in un blocco vicino a dove vengono usate

## Inizializzazione

**NB** Una variabile non inizializzata avrà comunque un valore ma può essere un valore qualsiasi

Ci sono diversi modi per inizializzare una variabile

```cpp
int age=21;   // C like
int age (21); // Constructor initialization
int age {21}; // C++11 list initialization syntax
			  // questo ha dei benefit che vedremo successivamente
```

## Global variables

 Ogni variabile "vive" in uno scope. Se definiamo un avariabile nel main è vista solo nel main e nelle sue funzioni interne ma non al di fuori.

E' possibile dichiarare delle variabili globali in modo tale che siano sempre visibili a tutti

Le variabili globali sono automaticamente inizializzate a 0

Per dichiarare una variabile globale basta dichiararla al di fuori di qualsiasi funzione

**NB** Le variabili locali oscurano quelle globali quindi se abbiamo una variabile globale chiamata "age" e una variabile locale nel main chiamata sempre "age" nel main "age" sarà riferito alla variabile locale

## Tipi

**Problema** In C++ il size e la precisione di un tipo dipende dal sistema e dal compilatore che stiamo usando

#include<climits> contiene le informazioni sui size del compilatore in uso

Se un tipo ha un size di n bit il numero di valori rappresentbili è $2^{n}$ 

### Caratteri

Tipi usati per singola lettera

- char (almeno 8 bit)
- char16_t (almeno 16bit)
- char_32_t (almeno 32bit)
- wchar_t (Può rappresentare l'insieme di caratteri il più grande possibile)

char può rappresentare 256 caratteri, più che sufficienti per l'alfabeto latino

### Integer

- int (almeno 16 bit)
- long (almeno 32 bit)
- long long (almeno 64 bit)

In aggiunta a questi, aggiungendo il prefisso **unsigned** (tranne per int che non è unsigned int ma solo unsigned) è possibile avere dei tipi con lo stesso size ma privi di segno

### Floating point

- float (7 cifre decimali) (range $1.2 \cdot 10^{-38}$ to $3.4 \cdot 10^{38}$) 
- double (da 7 a 15 cifre decimali) (range $2.2 \cdot 10^{-308}$ to $1.8 \cdot 10^{308}$)
- long double (da 15 a 19 cifre decimali) (range $3.3 \cdot 10^{-4932}$ to $1.2 \cdot 10^{4932}$) 

Ricorda che i floating point sono rappresentati da esponente e mantissa. La presione rappresenta il numero di cifre nella mantissa

RICORDA SEMPRE CHE PRECISIONE E SIZE SONO COMPILER DEPENDENT 
