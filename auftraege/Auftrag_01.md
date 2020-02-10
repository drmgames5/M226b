# Docsify

**Auftrag:**
Folgende Aufteilung hat der Auftrag 1:

* [Vererbung](#Vererbung)
* [Polymorphie](#Polymorphie)

## Vererbung

### Was ist das?

Vererbung ist das übergeben von variablen und methoden aus einer Superklasse in eine Subklasse.
Erstellte Methoden sind dann auch in einer Subklasse nutzbar.

> [!TIP|style:flat]
> Eine Superklasse ist sozusagen ein Elternteil und eine Subklasse das Kind.
>

### Wozu das Ganze?

Durch das vererben von Methoden und Variablen sparrt man eine menge an code. Muss man diese nicht auch in den Subklassen nochmals schreiben.
Auch hat man dadurch einen Zentralen Code für die einzelnen Methoden und Variablen. Wenn man eine Methode bearbeiten muss, so muss man nicht darauf achten diese auch bei den Subklassen zu bearbeiten.

Sagen wir zum Beispiel wir wollen ein Spiel mit verschiedenen Tieren erstellen.
Darunter:

* Hunde
* Schlangen
* Kühe
* Menschen

Nun haben diese Tiere einige Dinge gemeinsam, zum Beispiel müssen alle essen oder bewegen sich. Diese Dinge wären im Beispiel Methoden. Nun will man aber nicht für jedes Tier die gleichen Methoden einzeln coden. Also macht man eine Superklasse

* Tiere

und schreibt dort beide Methoden hinein. Dann kann man diese von den unterklassen:

* Tiere
    * **Hunde**
    * **Schlangen**
    * **Kühe**
    * **Menschen**

aus aufrufen ohne sie nochmals schreiben zu müssen.

### Wie kann ich das anwenden in Java?

#### Superklasse

Um eine Superklasse zu erstellen muss man einfach nur eine Normale Klasse erstellen.

```java
    public class Superklasse{
        whatever...
    }
```

#### Subklasse

Um eine Subklasse zu erstellen muss man die Superklasse wie folgt einbinden:

```java
    public class Subklasse extends Superklasse{
        whatever...
    }
```

## Polymorphie

### Was ist das?

Mit polymorphie kann man Subklassen

* Hunde
* Schlangen
* Kühe
* Menschen

von mehreren Klassen erben lassen. Zum Beispiel könnten sie von den Klassen

* Tiere

und

* Erdlingen

erben. Auch kann man Methoden und Variablen von Superklassen in den Subklassen ändern/überschreiben.

### Wozu das Ganze?

Nun, ein Mensch bewegt sich zum Beispiel mit einer anderen geschwindigkeit als ein Hund. Wenn wir also eine Variable "**max.Geschwindigkeit = 322 km/h**" in der Klasse **Tiere** hätten. so könnte man diese in der Subklasse **Menschen** zB. mit dem Wert **44,72 km/h** und in der Subklasse **Hunde** mit **70kmh** überschreiben. Die **bewegen** Methode müsste man jedoch trotzdem nicht neu schreiben.

### Wie kann ich das anwenden?

Polymorphie kann heissen, dass man Methoden überlädt (Wie wir es von Konstruktoren kennen) oder aber überschreibt. Beim überladen hat man zB. zwei Methoden die den gleichen Namen aber eine andere Signatur haben. Beim überschreiben können Methoden die genau gleiche Signatur haben, sie müssen aber einen anderen "Rumpf" also inhalt haben.

#### Beispiel:

* **Tiere:**

```java
    public bewegen("maxGeschwindigkeit"){
        System.out.println("Ein Tier bewegt sich mit einer Geschwindigkeit zwischen 0.1 und " + maxGeschwindigkeit);
    }
```

* **Menschen:**


```java
    public bewegen("maxGeschwindigkeit"){
        System.out.println("Der Mensch bewegt sich mit einer Geschwindigkeit zwischen 0.1 und " + maxGeschwindigkeit);
    }
```

* **Hunde:**

```java
    public bewegen("maxGeschwindigkeit"){
        System.out.println("Der Hund bewegt sich mit einer Geschwindigkeit zwischen 0.1 und " + maxGeschwindigkeit);
    }
```

Dadurch gäbe es bei folgenden aufruf:

```java
    mensch1.bewegen();
    hund1.bewegen();
```

Eine angespasste ausgabe für jedes tier wie folgt:

```
    Der Mensch bewegt sich mit einer Geschwindigkeit zwischen 0.1 und 44.72 kmh
    Der Hund bewegt sich mit einer Geschwindigkeit zwischen 0.1 und 70 kmh
```

> [!TIP|style:flat]
> Das Programm ergäbe zwar so nicht viel Sinn, erklärt es jedoch ganz gut.
>