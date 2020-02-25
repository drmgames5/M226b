# Docsify

**Auftrag:**
Folgende Aufteilung hat der Auftrag 2:

* [Zugriffsrechte und super()](#Zugriffsrechte)

## Zugriffsrechte und super()

Nach dem wir beim letzten Mal die Vererbung angschaut haben gibt es jetzt noch ein paar Dinge zu beachten.

Erstmal muss die Subklasse auf die Superklasse zugreifen können. Deshalb wird der Konstruktor der Superklasse mit dem Zugriffsmodifizierer **protected** erstellt. Dadurch haben ihre Subklassen nun die Zugriffsrechte um auf die Superklasse zugreifen zu können.

**Bsp:**

```java
protected Tier(String art){
    this.art = art
}
```

Wenn man nun eine Subklasse instanzieren will braucht diese ja einen Konstruktor. Nun muss bei der Erstellung dieser Subklasse, z.B. Schlange, auch beachtet werden das die Schlange ja auch ein Tier ist und somit auch den Konstruktor der Superklasse benutzen muss. Dies macht man mit der "super();" bezeichnung.
Das ganze sieht z.B wie folgt aus:

```java
public Schlange(String art, String familie)
    super(art);
    this.familie = familie;
}
```

> [!NOTE|style:flat]
> **super()** ist eine ......(welche bezeichnung hat das?)
>
