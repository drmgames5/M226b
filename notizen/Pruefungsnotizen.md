# Docsify

**Auftrag:**
Folgende Aufteilung hat der Auftrag 1:

* [Was erbt Superklasse](#Superclass)
* [Abstrakte Klassen](#Abstract)

## Superclass erbung

**getClass()**

gibt die gerade verwendete klasse an.

**toString()**

Gibt einen String zurück der die Klasse beschreibt.

**equals()**

vergleicht ob ein Object gleich them ausführenden Objekt ist

**hashCode()**

erstellt einen HashCode aus der ausführenden Klasse

## Abstract

### Klassen

Eine Abstrakte klasse wäre zum Beispiel person. diese soll nie selbst erstellt werden, da sie noch nicht genug genau definiert ist. Sie soll nur ein Grundgerüst sein also macht man eine abstract klasse draus die nicht instanziert werden kann.

### Methoden

Abstrakte Methoden sind Methoden die nur vorgeben sollen welche Methoden in den unterklassen immer ausprogrammiert werden müssen. Diese schreibt man ohne rumpf da dieser ja nicht nötig ist.

**protected**
Um variablen nur in unterklassen zu verwenden erstellt man diese als protected.

## Interfaces 

Dies sind Schnittstellen zwischen klassen. Sie definieren wie eine Klasse die sie implementiert, auszusehen hat, bzw welche Methoden und variablen beinhaltet sein müssen.

**BSP-Interface**

```java
public interface InterfaceName{
    int meinInt();
    String Bewertung(Object yamom);
}

```

> [!TIP|style:flat]
> Das sind beides Methoden
>

**BSP-using Interface**

```java
public class Person implements InterfaceName{
    @Override
    public int meinInt(){
        //was der shit halt macht
    }
    public String Bewertung(){
        //dieser shit macht halt was anderes 
    }
}

```

> [!TIP|style:flat]
> Eine Superklasse ist sozusagen ein Elternteil und eine Subklasse das Kind.
>
