# Übung5

Im folgenden Skript werden die Beispiel-Tabellen `VERTRETER`, `VERKAUF` und `ARTIKEL` verwendet.

## Aufgabe 1
Führe das SQL-Skript [DB-Vertreter](./SQL_-_DB-Vertreter.sql) in SQLPlus aus, um die Tabellen anzulegen und mit Beispieldaten zu füllen. Wie lautet dein Befehl um das SQL-Skript auszuführen?

### Lösung
```sql
start C:\Users\Hali\workspace\github.com\Bullboss\vgdb_ws1718\05_VertiefungDML\SQL_-_DB-Vertreter.sql
```

## Aufgabe 2
Mache dich mit den Tabellen vertraut bzgl.:
* Spalten und Datentypen
* Beziehung der Tabellen zueinander
* Datensätzen in den Tabellen und was diese bedeuten
Tabelle Verterter anlegen... --soll Vertreter heißen
Tabelle Artikel anlegen...
Tabelle Verkauf anlegen...
Datensaetze in Vertreter einfuegen ...
Datensaetze in Artikel einfuegen ...
Datensaetze in Verkauf einfuegen ...
```sql
select * from vertreter;
select * from artikel;
select * from verkauf;
```

## Aufgabe 3
Zeige alle Vertreter mit `NAME` und `VNR` an, die eine Provision von  
weniger als 7% erhalten. 

### Lösung
```sql
select vname, vnr from vertreter
where provision<0.07;
```

## Aufgabe 4
Bei welchen Artikeln (`NAME` und `ARTIKELNUMMER`) liegt der Preis über `100`?

### Lösung
```sql
select aname, anr from artikel
where apreis>100;
```

## Aufgabe 5
Zeige alle Vertreter an, die vor dem 01.01.1980 geboren sind und deren Name 
ein i beinhaltet.

### Lösung
```sql
select * from vertreter
where geburtsdatum<01.01.1980 and vname like '%a%';
```

## Aufgabe 6
Füge dich als Vertreter in die Tabelle Vertreter ein mit einer Provision von 
6% und der Mitarbeiternummer 7777.

### Lösung
```sql
insert into vertreter
values (7777, 'Bullboss', to_date('01.01.2001', 'dd.mm.yyyy'), 0.06);
```

## Aufgabe 7
Füge für deinen Vertreter einen Verkauf mit UNR 1014 hinzu. Der neue Datensatz 
soll abbilden, dass heute 22 Wintermäntel vom Vertreter mit VNR 7777 verkauft wurden.

### Lösung
```sql
insert into  verkauf
values (1014, 7777, 13, 22, sysdate);
```

## Aufgabe 8
Ändere den Preis eines Stiefels auf 88,90.

### Lösung
```sql

```

## Aufgabe 9
Füge der Tabelle Vertreter eine Spalte bonus hinzu, in die ein bis zu 
vierstelliger, ganzzahliger Wert eingetragen werden soll.

### Lösung
```sql

```

## Aufgabe 10
Setze den Bonus für alle Vertreter auf 500.

### Lösung
```sql

```

## Aufgabe 11
Ändere den Datentyp für die Spalte vname in der Tabelle vertreter auf VARCHAR2(20);

### Lösung
```sql

```

## Aufgabe 12
An welchen Tagen wurden Verkäufe getätigt? Erzeuge folgende Ausgabe: 
DATUM
----------
27.06.15
28.06.15

### Lösung
```sql

```