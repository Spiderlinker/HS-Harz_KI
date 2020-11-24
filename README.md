# HS-Harz_KI

<HTML>
<HEAD>
<META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=iso-8859-1">
</HEAD>

<BODY>
<CENTER>
  <H3>Laboraufgaben zu <EM>Künstliche Intelligenz</EM></H3>
  <A HREF="http://www.hs-harz.de/fstolzenburg">Frieder Stolzenburg</A><BR>
</CENTER>
<hr>
<P><B>AUFGABE 1:</B>
Schreiben Sie ein Prolog-Programm (Fakten und Regeln), das mit
einem Stammbaum (siehe unten) umgehen kann. Dabei bezeichnen
Linien die Eltern-Kind-Relation. &amp; bedeutet <EM>ist
verheiratet mit</EM>. Definieren Sie diese beiden Relationen in
Form von Fakten. Das Geschlecht der Person sollte auch
festgehalten werden. Schreiben Sie nun Regeln für die Vater-,
Geschwister-, Schwester-, Großmutter- und Tantenrelation.</P>
<IMG SRC="/Aufgabenstellung/stamm.gif">

<P><B>AUFGABE 2:</B> 
Schreiben Sie ein Prolog-Programm und zwei Anfragen, welche feststellen, ob (a)
die alten Bundesländer (Baden-Württemberg, Bayern, Bremen, Hamburg, Hessen,
Niedersachsen, Nordrhein-Westfalen, Rheinland-Pfalz, Saarland,
Schleswig-Holstein) und (b) die neuen Bundesländer (Berlin, Brandenburg,
Mecklenburg-Vorpommern, Sachsen, Sachsen-Anhalt, Thüringen) von Deutschland so
mit den 3 Farben rot, gelb und blau eingefärbt werden können, dass keine
benachbarten Bundesländer die gleiche Farbe haben. Welche Lösungen werden
gefunden? (c) Lassen sich alle Bundesländer mit nur 3 Farben auf die o.g. Weise
einfärben?</P>
<IMG SRC="/Aufgabenstellung/map.gif">

<P><B>AUFGABE 3:</B>  <!-- Frühwirth & Abdennadher: A.3.6 -->
Kryptoarithmetische Rätsel sind Darstellungen arithmetischer
Berechnungen, bei denen die Ziffern durch Buchstaben
verschlüsselt sind. Es gilt, diese Rechnungen zu rekonstruieren,
wobei zu beachten ist, dass gleiche Buchstaben gleichen Ziffern
und verschiedene Buchstaben verschiedenen Ziffern entsprechen.
Außerdem darf für einen Buchstaben nicht 0 eingesetzt werden,
wenn er an führender Stelle steht. Schreiben Sie ein
Prolog-Programm, welches das folgende klassische Rätsel löst.
Geben Sie auch die Lösung des Rätsels an! Wie lange braucht Ihr
Programm, bis die Lösung gefunden wird?</P>

<PRE>
  S E N D
+ M O R E
---------
M O N E Y
</PRE>

<B>Hinweise:</B> Verwenden Sie die eingebauten Prädikate <EM>is/2</EM>, welches
das Ergebnis einer Berechung einer Variablen zuweist, z.B. <EM>X is 2*Y+1</EM>,
und <EM>=:=</EM>, welches die Werte zweier arithmetische Ausdrücke miteinander
vergleicht. - In SWI-Prolog kann die Rechenzeit ermittelt werden, indem Sie die
betreffende Anfrage als Argument von <EM>time</EM> aufrufen. 

<br>
<hr>
<br>


<P><B>AUFGABE 4:</B>
Schreiben Sie Prädikate in Prolog, die den folgenden Definitionen
genügen:</P>

<OL>
   <LI> <EM>reversi(L,R)</EM> :- Die Liste <EM>R</EM> enthält die
	Elemente der Liste <EM>L</EM> in umgekehrter Reihenfolge.
   <LI> <EM>insert(X,L1,L2)</EM> :- Das Element <EM>X</EM> ist an
	irgendeiner Stelle vor, in oder hinter der Liste
	<EM>L1</EM> eingefügt. Das Ergebnis ist die Liste
	<EM>L2</EM>.<BR>
	Für <EM>X = x</EM> und <EM>L1 = [a,b]</EM> ergeben sich
	für <EM>L2</EM> etwa die Lösungen <EM>[x,a,b]</EM>,
	<EM>[a,x,b]</EM> und <EM>[a,b,x]</EM>.
   <LI> <EM>permutation(L1,L2)</EM> :- <EM>L2</EM> ist eine
	Permutation der Liste <EM>L1</EM>.<BR>
	Für <EM>L1 = [a,b,c]</EM> z.B. besitzt <EM>L2</EM> die 
	Lösungen <EM>[a,b,c]</EM>, <EM>[a,c,b]</EM>, 
	<EM>[b,a,c]</EM>, <EM>[b,c,a]</EM>, <EM>[c,a,b]</EM>,
	<EM>[c,b,a]</EM>.<BR>
	Sie können hierzu das Prädikat <EM>insert</EM> ausnutzen.
</OL>

<P><B>AUFGABE 5:</B> <!-- Prolog 1997: 2.3 -->
Die Datenstruktur Menge ist in Prolog nicht vordefiniert.
Naheliegenderweise können Mengen durch Listen dargestellt werden.
Beachten Sie aber, dass sowohl die Reihenfolge der Elemente als
auch Mehrfachvorkommen ein und desselben Elementes keine Rolle
spielen dürfen. Schreiben Sie Prozeduren, die folgenden
Beschreibungen genügen (zumindest für Anfragen ohne
Variablen)!</P>

<OL>
   <LI> <EM>alldistinct(M)</EM> :- <EM>M</EM> ist eine echte
	Menge, d.h. enthält nur verschiedene Elemente.
   <LI> <EM>subtract(A,B,C)</EM> :-  Die Menge <EM>C</EM> ist die
        Menge <EM>A\B</EM> (Mengendifferenz).
   <LI> <EM>disjoint(A,B)</EM> :- Die Mengen <EM>A</EM> und
        <EM>B</EM> sind disjunkt.
</OL>

<B>Hinweis:</B> Verwenden Sie ggf. Cut (!), Negation (\+) oder If-Then-Else (-> ;). 

<br>
<hr>
<br>

<P><B>AUFGABE 6:</B>
Drei Missionare und drei Kannibalen versuchen, einen Fluss zu überqueren. Sie
besitzen ein Boot, mit dem jeweils ein oder zwei Personen übersetzen können.
Falls irgendwann an einem Ort die Zahl der Kannibalen größer ist als die der
Missionare, fressen die Kannibalen die Missionare auf. Planen Sie die Überfahrt
so, dass alle Missionare und alle Kannibalen wohlbehalten am anderen Ufer
ankommen.</P>

<UL>
   <LI> Lösen Sie das Problem mittels eines Prolog-Programms! Das
	Programm soll auch die Lösung ausgeben.
   <LI> Repräsentieren Sie das Wissen geeignet! Vermeiden Sie
	Redundanzen!
   <LI> Es soll kein Zustand mehrfach durchlaufen werden. Um dies
	sicher zu stellen, können Sie das eingebaute Prädikat
	<EM>\+</EM> für die Negation verwenden.
</UL>

<B>Hinweis:</B> Um Ergebnisse in voller Länge ausgegeben zu bekommen, sollte im
Programm zu Anfang die Direktive
<EM>:- set_prolog_flag(answer_write_options,[max_depth(100)]).</EM>
eingesetzt werden.

<P><B>AUFGABE 7:</B> <!-- Künstliche Intelligenz 1999: 3 -->
Gegeben sei der Graph G<SUB>N</SUB> bestehend aus einem
Startknoten <EM>start</EM> und den folgenden Knoten:
<UL>
   <LI> <EM>incest(I,J)</EM> für I=0,1 und J=1,..,N
   <LI> <EM>cycle(K)</EM> für K=1,2
   <LI> <EM>tree(L)</EM> für L=1,..,2<SUP>N</SUP>-1
</UL>
Zwischen den Knoten bestehen folgende Verbindungen:
<UL>
   <LI> <EM>start~incest(0,1)<EM>, </EM>start~incest(1,1)</EM>
   <LI> <EM>incest(I,J)~incest(I',J+1)</EM> für I,I'=0,1 und J < N
   <LI> <EM>incest(1,N)~cycle(1)</EM>
   <LI> <EM>cycle(1)~cycle(2)</EM>, </EM>cycle(2)~cycle(1)</EM>
   <LI> <EM>cycle(2)~tree(1)</EM>
   <LI> <EM>tree(L)~tree(2L)</EM>, <EM>tree(L)~tree(2L+1)</EM>
        für L < 2<SUP>N-1</SUP>
</UL>
Dabei bedeutet die Schreibweise <EM>u~v</EM>, dass es eine
Verbindungskante von Knoten <EM>u</EM> nach <EM>v</EM> gibt (aber
nicht notwendigerweise umgekehrt).
<OL>
   <LI> Definieren Sie den Graphen G<SUB>3</SUB> in Prolog durch
	Fakten zum Prädikat <EM>edge/2</EM> für die Kanten. Der
	Startknoten <EM>S</EM> sei durch das Faktum
	<EM>init(S).</EM> gegeben.
   <LI> Programmieren Sie Tiefen- und Breitensuche in Graphen
	explizit in Prolog. Definieren Sie ein Prädikat
	<EM>search/2</EM>, welches im zweiten Argument alle vom
	Startknoten aus erreichbaren Knoten nacheinander durch
	Backtracking berechnet, und zwar in der durch die
	Suchstrategie (= erstes Argument) festgelegten
	Reihenfolge.
   <LI> In welcher Reihenfolge werden bei Tiefen- und
	Breitensuche die Knoten im Graphen G<SUB>3</SUB> besucht?
	Zeichnen Sie gegebenenfalls den Graphen G<SUB>3</SUB>!
</OL>
<B>Hinweise:</B>
<UL>
   <LI> Sie können das Prolog-Prädikat <EM>between(From,To,K)</EM> einsetzen,
	welches nacheinander in <EM>K</EM> die ganzen Zahlen zwischen
	<EM>From</EM> und <EM>To</EM> einschließlich aufzählt.
   <LI> Um Knoten in eine Queue oder einen Stack einzufügen, ist es
	sinnvoll, alle Nachfolgerknoten auf einmal berechnen zu können.
	Das kann man mit dem eingebauten Prädikat <EM>findall</EM> wie
	folgt realisieren: <EM>children(PARENT,CHILDREN) :- findall(CHILD,edge(PARENT,CHILD),CHILDREN).</EM>
   <LI> Jeder Knoten soll nur genau einmal berechnet werden, d.h. bauen Sie eine
	Schleifenerkennung ein und vermeiden so Endlosschleifen.
</UL>
</P>

<P><B>AUFGABE 8:</B>
Lösen Sie das unten stehende kryptoarithmethische Puzzle mit
Hilfe von Constraints über endlichen Domänen.<BR> Wie lange
braucht Ihr Programm, bis die Lösung gefunden wird? Vergleichen
Sie die Zeit mit einer Lösung ohne Constraint-Programmierung!</P>
<PRE>
      S E N D
    + M O R E
    ---------
    M O N E Y
</PRE>
<B>Hinweis:</B> Laufzeiten können Sie in SWI-Prolog mit Hilfe des Prädikats
<EM>time/1</EM> bestimmen.

</BODY>
</HTML>
