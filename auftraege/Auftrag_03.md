# Docsify

**Auftrag:**
Folgende Aufteilung hat der Auftrag 3:

* [Methoden überschreiben](#Überschreiben)
* [Methoden überladen](#Überladen)

## Überschreiben

### Was ist das?

Eine Methode wird überschrieben, wenn diese Methode z.B **fortbewegen()** in der Superklasse Tiere deklariert wird und diese dann in der Subklasse nochmals mit der gleichen Signatur erstellt wird. Der **Rumpf**, also der Inhalt der Methode unterscheidet sich aber von dem der Subklasse.

### Wozu das Ganze?

Somit kann man zum Beispiel in der Superklasse eine Methode **getDefinition()** definieren in der man dann z.B. einen String mit dem Inhalt "Ich gehöre zu der Tierart + art" zurückgibt. Diesen kann man nun in der Subklasse überschreiben und dort einen weiteren expliziteren Inhalt wie z.B. " und ich gehöre zur familie der + familie" hinzufügen.

### Wie kann ich das anwenden?

Dafür muss man wie bereits erwähnt in der Superklasse die Methode definieren und in der Subklasse mit der gleichen Signatur nochmals definieren. Dann kann man in die Super- und Subklasse die jeweiligen Inhalte einfügen.

> [!TIP|style:flat]
> Aus geschichtlichen Gründen wurde es zur gewohnheit, das man @Override über die überschriebenen Methoden in der Subklasse schreibt. Dies diente früher um dem Compiler zu sagen das etwas überschrieben wird und dient heute der übersichtlichkeit.
>

#### Beispiel:

**In Superklasse:**

```java
public String getDefinition()
    return "Ich gehöre zu der Tierart " + this.art;
}
```

**In Subklasse:**

```java
public String getDefinition()
    return " und ich gehöre zur familie der " + this.familie;
}
```

## Überladen

### Was ist das?
### Wozu das Ganze?
### Wie kann ich das anwenden?

#### Beispiel:


> [!NOTE|style:flat]
> **super()** ist eine ......(welche bezeichnung hat das?)
>
