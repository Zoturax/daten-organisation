---
# bibliography: references.bib

title: Daten kodieren

abstract: ""

execute: 
  echo: false
---





## Zahlensysteme

> Als **Zahlensystem** wird die Schreibweise für Zahlenwerte bezeichnet. 

In der Regel verwenden wir das sog. Dezimalsystem, um Zahlen darzustellen. Das Dezimalsystem hat 10 mögliche Symbole, um Zahlenwerte abzubilden. Diese Symbole sind `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9` und `0`. Damit können wir mit einem Symbol Zahlenwerte zwischen `0` und `9` abbilden. 

Gelegentlich lassen sich bestimmte Phänomene nicht gut im Dezimalsystem abbilden. Dadurch lassen sich Werte nur schwer interpretieren. In solchen Fällen hilft der Wechsel in ein anderes Zahlensystem.

> **Merke:**  Durch den Wechsel des Zahlensystems ändert sich nur die Darstellung, aber nicht der Wert einer Zahl! 

> **Definition:** Die Zahl, die als Grundlage für ein Zahlensystem dient,  wird als **Basis** des Zahlensystems bezeichnet. 

Beim in der Schulmathematik üblichen Dezimalsystem ist die Basis `10`.

> **Definition:** **Zahlensysteme** kodieren Zahlenwerte zu einer gegebenen Basis. 

### Die wichtigsten Zahlensysteme 

| Name | Basis | Symbole |
| :--- | :--- | :--- |
| Binärsystem | `2` | `0`, `1` |
| Oktalsystem | `8` | `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7` |
| Dezimalsystem | `10` | `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9` |
| Duodezimalsystem | `12` | `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `A`, `B` |
| Hexadezimalsystem | `16` |  `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `A`, `B`, `C`, `D`, `E`, `F` |
| Sexagesimalsystem | `60` | - |

Das Duodezimalsystem und das Sexagesimalsystem treffen wir im Alltag bei Datums- und Zeitwerten, bei Winkeln sowie in der Musik an. Im Deutschen lässt sich das Duodezimalsystem noch an den Zahlworten elf (`11`) und zwölf (`12`) erkennen.

Das binäre Zahlensystem stellt die Grundlage für digitale Computer dar, weil es nur zwei Werte für die Darstellung von Zahlen benötigt. D.h. alle Werte lassen sich als Vielfache von zweier-Potenzen abbilden. Claude Shannon hat bereits 1938 erkannt, dass diese Darstellung sich direkt die Zustände "ein" und "aus" von Schaltern übersetzen lässt, sodass sich alle Berechnungen mit Hilfe der [*Boolschen Algebra*](@08-boolsche-algebra) mit einfachen Schaltungen realisieren lassen. Daraus ergibt sich, dass das kleinste Bit der Informationstheorie sich im Binären-Zahlensystem abbilden lässt. 

Die Zahlensysteme Oktal und Hexadezimal sind für die Abbildung von Werten in Digitalcomputern von besonderer Bedeutung, weil es sich jeweils um ganzzahlige 2er Potenzen handelt. 

| Name | Basis | 2er-Potenz |
| :--- | :--- | :--- |
| Binär | `2` |$2^1$|
| Oktal | `8` |$2^3$|
| Hexadezimal | `16` |$2^4=2^{2^2}$|

Der Exponent der 2er-Potenz der Basis zeigt an, wie viele Stellen im Binärsystem (Bits) mit dem jeweiligen System abgebildet werden können. Ein Byte bildet per Konvention zwei Stellen im Hexadezimalsystem oder 8 Bit ab. 

> Hexadezimal-Werte werden recht häufig beim Programmieren verwendet, wie z.B. für das Kodieren von Buchstaben und Satzzeichen. Damit diese Werte leichter von Werten im Dezimalsystem unterschieden werden können, werden Werten im Hexadezimalsystem per Konvention die beiden Symbole `0x` vorangestellt.

**Beispiele**

| Dezimal  | Hexadezimal |
| ---: | ---: |
| `0`  | `0x0` |
| `1` | `0x1` |
| `2` | `0x2` |
| `3` | `0x3` |
| `4` | `0x4` |
| `8` | `0x8` |
| `9` | `0x9` |
| `10` | `0xA` | 
| `15` | `0xF` | 
| `16` | `0x10` |

### Binärzahlen

> Binärzahlen kodieren Zahlenwerte zur Basis 2.

Daraus folgt, dass für jede Ziffer genau zwei Symbole (Ziffern) zur Verfügung stehen: `0` und `1`. 

Wie in anderen Zahlensystemen entspricht eine Stelle im Binärsystem einer Potenz zur gegebenen Basis. Das ist bei Binärwerten `2`. Jede Stelle für eine Ziffer kann also einer 2er-Potenz gleichgesetzt werden.

Die Besonderheit des Binärsystems ist, dass alle Werte als Summe von 2er-Potenzen dargestellt werden können. Diese Summe wird als *additive Darstellung* bezeichnet. 

| Wert | Binärwert | Additive Darstellung | Hexadezimal | 
| ---: | ---: | :---: | ---: | 
| `0` | `0000` | 0 | `0` | 
| `1` | `0001` | $2^0$ | `1` |
| `2` | `0010` | $2^1$ | `2` | 
| `3` | `0011` | $2^1 + 2^0$ | `3` |
| `4` | `0100` | $2^2$ | `4` |
| `5` | `0101` | $2^2 + 2^0$ | `5` |
| `6` | `0110` | $2^2 + 2^1$ | `6` | 
| `7` | `0111` | $2^2 + 2^1 + 2^0$ | `7` |
| `8` | `1000` | $2^3$ | `8` |
| `9` | `1001` | $2^3 + 2^0$ | `9` |
| `10` | `1010` | $2^3 + 2^1$ | `A` |
| `11` | `1011` | $2^3 + 2^1 + 2^0$ | `B` | 
| `12` | `1100` | $2^3 + 2^2$ | `C` |
| `13` | `1101` | $2^3 + 2^2 + 2^0$ | `D` |
| `14` | `1110` | $2^3 + 2^2 + 2^1$ | `E` |
| `15` | `1111` | $2^3 + 2^2 + 2^1 + 2^0$ | `F` |

Aus dieser Tabelle kann man ablesen, dass die Ziffer `1` im Binärsystem bedeutet, dass die 2er-Potenz an der entsprechenden Stelle aktiv ist. 

Jede Ziffer im Binärsystem kann ausserdem als eigenständiges Symbol einer Nachricht verstanden werden. Weil im Binärsystem nur die beiden Ziffern `0` und `1` möglich sind, müssen beim Dekodieren nur diese Beiden Werte unterschieden werden. Jedes andere Zahlensystem kodiert Zahlen mit mehr als zwei Ziffern.

#### 2er-Potenzen und Speichergrössen

Nach diesem Prinzip werden auch die Kapazitäten von Datenspeichern als 2er-Potenzen beschrieben.

| Name | Abkürzung | gespeicherte Byte |
| :--- | :--- | :--- |
| Byte | B |$2^0 = 1$|
| Kilobyte | KB |$2^{10} = 1024^1$|
| Megabyte | MB |$2^{20} = 1024^2 = 1048576$|
| Gigabyte | GB |$2^{30} = 1024^3 = 1073741824$|
| Terabyte | TB |$2^{40} = 1024^4 = 1099511627776$|


<p class="alert alert-warning" markdown="1">
Die *wissenschaftliche Schreibweise* ist **kein eigenes Zahlensystem**.  Sie ist nur eine *Vereinheitlichung* der Schreibweise im Dezimalsystem, um sehr grosse und/oder sehr kleine Zahlen kompakt darstellen zu können. 
</p>

### Winkelangaben als irrationales Zahlensystem

Winkelangaben werden oft als Vielfache von $\pi$ angegeben. Diese Werte werden auch als *Radiant* anstatt als Grad bezeichnet. Dabei handelt es sich um ein Zahlensystem zur Basis $\pi$.

- $\frac{\pi}{6}$ = 30°
- $\frac{\pi}{4}$ = 45°
- $\frac{\pi}{3}$ = 60°
- $\frac{\pi}{2}$= 90°
- $\frac{2\pi}{3}$= 120°
- $\pi$= 180° 
- $\frac{3\pi}{2}$= 270°
- $2\pi$= 360°

### Prinzip eines Zahlensystems

Die in der Mathematik verwendeten Zahlensysteme sind sog. *additive Zahlensysteme*. Die Schreibweise wird durch Addition und Multiplikation mit der jeweiligen Basis bestimmt. 

Das Zählen funktioniert dabei wie folgt: 

1. Es wird bei `0` gestartet. 
2. Die nächste Ganzzahl wird durch Addition mit `1` erreicht. 
3. Es wird das nächste Ziffernsymbol ausgewählt. 
4. Gibt es für die jeweilige Basis keine Ziffernsymbole für die Ganzzahl mehr, wird die nächsthöhere Stelle um `1` erhöht. 

**Beispiele**

| Dezimal | Binär | Oktal | Hexadezimal |
| ---: | ---: | ---: | ---: |
| `0` | `0` | `0` | `0x0` |
| `1` | `1` | `1` | `0x1` |
| `2` | `10` | `2` | `0x2` |
| `3` | `11` | `3` | `0x3` |
| `4` | `100` | `4` | `0x4` |
| `8` | `1000` | `10` | `0x8` |
| `9` | `1001` | `11` | `0x9` |
| `10` | `1010` | `12` | `0xA` | 
| `15` | `1111` | `17` | `0xF` | 
| `16` | `10000` | `100` | `0x10` |
| `255` | `11111111` | `377` | `0xFF` |
| `256` | `100000000` | `400` | `0x100` |

## Wissenschaftliche Schreibweise von Zahlen

> Als **wissenschaftliche Notation** wird die Schreibweise von Zahlen mit Hilfe von Potenzen zur Basis 10 bezeichnet. 

Bei der wissenschaftlichen Notation wird die erste Ziffer einer Zahl vor ein Komma gesetzt und alle restlichen Ziffern nach dem Komma. Anschliessend werden die restlichen Ziffern gezählt und als 10er-Potenz angegeben. 

Bei kleinen Zahlen wird ähnlich vorgegangen: Die erste Ziffer ungleich `0` wird vor ein Komma gesetzt und alle folgenden Stellen danach. Anschliessend werden alle Nullen und die Ziffer vor dem Komma gezählt und als negative 10er-Potenz angegeben.
 
Neben der ausführlichen wissenschaftlichen Schreibweise wird regelmässig eine abgekürzte Notation verwendet. In dieser Notation wird der Teil $\cdot 10$ durch ein `e` oder `E` ersetzt. Dieses `E` steht für *Exponent*. 

**Beispiele:** 

| Normale Notation | Wissenschaftliche Notation | Kurze wissenschaftliche Notation |
| ---: | ---: | ---: |
| 1 | $1 \cdot 10^0$ | 1e0 |
| 10 | $1 \cdot 10^1$ | 1e1 |
| 100 | $1 \cdot 10^2$ | 1e2 |
| 523140000 | $5.2314 \cdot 10^8$ | 5.2314e8 |
| 0.00000000007234 | $7.234 \cdot 10^-11$ | 7.234e-11 |

Die Stärke der wissenschaftlichen Notation ist die Darstellung sehr grosser oder sehr kleiner Zahlen

Mit dieser Schreibweise lassen sich auch schnell Grössenunterschiede zwischen Werten abschätzen: Dazu wird die Differenz der 10er-Potenzen zweier Zahlen gebildet. Dazu wird die kleinere 10er-Potenz von der grösseren subtrahiert. Das Ergebnis ist wieder eine 10er-Potenz. 

**Beispiel**

- Eine Differenz von 1 entspricht einem ungefähr 10-fachen Grössenunterschied. 
- Eine Differenz von 5 entspricht einem ungefähr 100000-fachen Grössenunterschied.

## Zeichenkodierung

Wir schreiben Texte nicht mit Zahlen, sondern mit Buchstaben, Satz- und Steuerzeichen. Im Computer werden Texte als Zahlen abgebildet. Dazu werden die einzelnen Zeichen eines Textes in Zahlenwerte übersetzt. Diese Übersetzung wird als **Zeichenkodierung** bezeichnet und wird per Konvention festgelegt. 

Weil sich Buchstaben und andere Zeichen nicht direkt als Zahlen übersetzen lassen, bedarf es eines Tricks. Dazu werden alle zu kodierenden Zeichen in einer Liste aufgeschrieben und anschliessend werden alle Zeichen durchnummeriert. Die Nummer des Zeichens wird als Zahlenwert stellvertretend für das jeweilige Zeichen. 

> **Merke:** Mit dem Nummerieren von Symbolen lassen sich beliebige Symbole als Zahlenwerte kodieren.

Bei den meisten Zeichenkodierungen werden die einzelnen Zeichen so aufgereiht, dass die alphabetische und nummerische Reihenfolge in der Regel erhalten bleibt. Zeichenkodierungen sind standardisiert und müssen nicht mehr selbst entwickelt werden. Es gibt allerdings mehrere Standards, die sich in der Kodierung unterscheiden. Deshalb ist es notwendig, die verwendete Zeichenkodierung zu dokumentieren.

Historisch sind vier Kodierungen für die Praxis im deutschsprachigen Raum von Bedeutung. 

- ASCII - kodiert das Anglo-amerikanische Alphabet mit Ziffern und Satzzeichen in 7 Bit (Zahlen mit max. 7 Stellen binär).
- ANSI - kodiert das Anglo-amerikanische Alphabet mit Ziffern und Satzzeichen in 8 Bit (Zahlen mit max. 8 Stellen binär).
- ISO-8859 - kodiert verschiedene Schriftsysteme in 8 Bit (Zahlen mit max. 8 Stellen binär).
  - ISO-8859-1 (oder ISO Latin 1) - kodiert das westeuropäische Alphabet mit deutschen und französischen Umlauten.
  - ISO-8859-15 (oder ISO Latin 9) - Kodiert das westeuropäische Alphabet wie ISO-8859-1 aber mit dem Euro Symbol (€)
- UTF-8 - kodiert alle gängigen und viele historische Schriftsysteme inkl. Emojis dynamisch mit 8 bis zu 32 Bit. 

Diese Kodierungen sind bis zum Code 01111111 (oder 0x7F) identisch. Die Symbole in diesem Bereich werden deshalb als *ASCII-Codes* bezeichnet.

**Vollständige ASCII-Kodierungstabelle** 

| | 0	| 1	| 2	| 3	| 4	| 5	| 6	| 7	| 8	| 9	| A	| B	| C	| D	| E	| F |
| :--- |  :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | 
| 0x	| ***NUL***	| SOH	| STX	| ETX	| EOT	|	ENQ	|	ACK	|	BEL	|	***BS***	|	***HT***	|	***LF***	|	VT	|	FF	|	***CR***	|	SO	|	SI	|
|1x	|	DLE	|	DC1	|	DC2	|	DC3	|	DC4	|	NAK	|	SYN	|	ETB	|	CAN	|	EM	|	SUB	|	***ESC***	|	FS	|	GS	|	RS	|	US	|
| 2x	|	 ***SPC***	| 	!	|	"	|	#	|	$	|	%	|	&	|	'	|	(	|	)	|	*		| +	|	,	|	-	|	.	|	/ |
| 3x	|	0	|	1	|	2	|	3	|	4	|	5	|	6	|	7	|	8	|	9	|	:	|	;	|	<	|	=	|	>	|	?	|
| 4x	|	@	|	A	|	B	|	C	|	D	|	E	|	F	|	G	|	H	|	I	|	J	|	K	|	L	|	M	|	N	|	O	|
| 5x	|	P	|	Q	|	R	|	S	|	T	|	U	|	V	|	W	|	X	|	Y	|	Z	|	[	|	\	|	]	|	^	|	_	|
| 6x	|	`	| a	|	b	|	c	|	d	|	e	|	f	|	g	|	h	|	i	|	j	|	k	|	l	|	m	|	n	|	o	|
| 7x	|	p	|	q	|	r	|	s	|	t	|	u	|	v	|	w	|	x	|	y	|	z	|	{	|	\|	|	}	| ~	| ***DEL*** |

Neben Buchstaben werden auch sog. *nicht-druckbare Zeichen* wie Buchstaben, Satzzeichen und Ziffern kodiert. Dazu gehören u.a. Leerzeichen, Tabulatoren und Zeilenumbrüche. Viele dieser besonderen Buchstaben haben heute keine Bedeutung mehr. In der folgenden Tabelle sind die aktuell verwendeten nicht-druckbaren Zeichen mit `*` markiert.

| Zeichen | ASCII-Code | Bedeutung |
| :---: | :---: | :--- |
| `NUL*` | `0x00` | NULL (Nullzeichen, "Kein Wert", "Ende einer Zeichenkette") |
| `SOH` | `0x01` | Start of Heading |
| `STX` | `0x02` | Start of Text |
| `ETX` | `0x03` | End of Text |
| `ENQ` | `0x05` | Enquiry |
| `EOT`/`EOF` | `0x04` | End of Transmission/End of File (Dateiende)|
| `ACK` | `0x06` | Acknowledgement |
| `BEL*` | `0x07` | Bell (Klingelzeichen, wird meist ignoriert) |
| `BS` | `0x08` | Backspace (Rückschritt/Rückwärtslöschen) |
| `HT*` | `0x09` | Horizontal Tabulation (Horizontaler Tabulator) |
| `LF*` | `0x0A` | Line Feed (Zeilenvorschub, Zeilenumbruch, Zeilenende) |
| `VT` | `0x0B` | Vertical Tabulation (Vertikaler Tabulator) |
| `FF` | `0x0C` | Form Feed (Seitenvorschub) |
| `CR*` | `0x0D` | Carriage Return (Wagenrücklauf, *nur Windows*) |
| `SO` | `0x0E` | Shift Out |
| `SI` | `0x0F` | Shift In |
| `DLE` | `0x10` | Data Link Escape |
| `DC1` | `0x11` | Device Control 1 |
| `DC2` | `0x12` | Device Control 2 |
| `DC3` | `0x13` | Device Control 3 |
| `DC4` | `0x14` | Device Control 4 |
| `NAK` | `0x15` | Negative Acknowledgement |
| `SYN` | `0x16` | Synchronous Idle |
| `ETB` | `0x17` | End of Transmission Block |
| `CAN` | `0x18` | Cancel |
| `EM` | `0x19` | End of Medium |
| `SUB` | `0x1A` | Substitute (Dateiende/Datenende, *nur Windows*) |
| `ESC` | `0x1B` | Escape (Abbruch oder Funktionsänderung) |
| `FS` | `0x1C` | File Separator (Dateiende, veraltet) |
| `GS` | `0x1D` | Group Separator |
| `RS` | `0x1E` | Record Separator |
| `US` | `0x1F` | Unit Separator |
| `SPC*` | `0x20` | Space (Leerzeichen, Leerschlag) |
| `DEL` | `0x7F` | Delete (Vorwärtslöschen) |

Die Zeichen für Löschen (`BS` und `DEL`) und Funktionsumstellung (`ESC`) finden sich nicht mehr in Zeichenketten und Dateien. Sie dienen inzwischen nur als Steuerzeichen für die Eingabe mit der Tastatur.

Das Zeichen für das Dateiende (`EOF` bzw.  unter Windows `SUB`) ist kein kodiertes Zeichen in einer Zeichenkette, sondern wird vom Betriebssystem gesetzt. Dieses Symbol findet sich nicht in einer Datei und sollte nicht eingefügt werden.

Normalerweise werden nicht-druckbare Zeichen nicht in Zeichenketten dargestellt, obwohl sie in der Zeichenkette enthalten sind.

### Ziffernkodierung

Arabische Ziffern werden mit den Werten `0x30` (Ziffer `0`) bis `0x39` (Ziffer `9`) kodiert.

> **Merke:** Ziffern in Zeichenketten sind nicht gleichwertig mit den Ziffern in Zahlen. 

Eine Zahl wird als eine Abfolge von Ziffern dargestellt. Wird ein Wert als Zahl dargestellt, dann werden die Ziffern entsprechend der gewählten Basis interpretiert. Werden Ziffern als Zeichenkette kodiert, dann entspricht der *Wert* der Ziffer der entsprechenden Kodierung. D.h.z.B. die Ziffer `"1"` in einer Zeichenkette hat nicht den Wert `1`, sondern den Wert `49` (`0x31`). Folgen mehrere Ziffern aufeinander in einer Zeichenkette, dann werden die kodierten Zahlen aneinandergereiht. Die Ziffern `"123"` entsprechen deshalb nicht dem Wert `123`, sondern dem Wert `3224115` (`0x313233`). 

> **Excel**, *R* und *Python* konvertieren Ziffern in Zeichenketten *oft* automatisch in die richtigen Zahlenwerte, **solange** keine anderen Zeichen in der jeweiligen Zeichenketten kodiert wurden.

> Nicht alle Programmiersprachen konvertieren Ziffern in Zeichenketten automatisch in Zahlenwerte.

### Serialisierung

> **Definition:** Ein Zahlenwert kann bei einer Darstellung zu einer Basis in mehreren Ziffern erfolgen. Diese Zifferndarstellung wird als **Serialisierung** bezeichnet. 

*Serialisierung* bedeutet, dass die Ziffern eines Werts *in einer bestimmten Reihenfolge* dargestellt werden. Jede Ziffer einer solchen Darstellung können wir uns als ein *Symbol* einer Nachricht vorstellen. 

Weil ein Zahlenwert in verschiedenen Zahlensystemen dargestellt werden kann, ergibt sich daraus der folgende Merksatz:

> **Merke:** Ein Zahlenwert hat *mehrere* zulässige Serialisierungen. 


## Symbole und Kompression

Das zentrale Element von Shannon's Informationstheorie sind *Nachrichten*, die aus Symbolen bestehen. Entsprechend trägt jedes Symbol zur Information einer Nachricht (`N`) bei. Shannon versteht unter dem Begriff *Symbol* sowohl Zahlen, Buchstaben, Worte als auch Wortfolgen. Dabei lassen sich Wortfolgen in mehrere Worte und Worte in Buchstaben aufteilen. 

> Ein Symbol, das nicht in einfachere Symbole unterteilt werden kann, wird als (Informations-) *Bit* bezeichnet.

Sich wiederholende Bits oder Bitfolgen können abgekürzt werden, indem die Bitfolge nur einmal zusammen mit Anzahl der Wiederholungen angegeben wird. 

> Das Abkürzen einer Bitfolge wird als **Kompression** bezeichnet.

Veranschaulichen wir uns das mit Hilfe der Nachricht `"aaaaaaaaaa"`. Diese Bitfolge kann als `[a]`$^{10}$ abgekürzt werden. 

Der Exponent zeigt uns, wie stark eine Bitfolge komprimiert wurde. 

Mit diesem Wissen können wir die Nachricht `"ababababab"` komprimieren. Die Kompression ist in diesem Fall `[ab]`$^5$. 

Dieses Spiel können wir weiter treiben: Die Nachricht `"aber aber "` lässt sich als [aber]$^2$ und die Nachricht `"aber hallo"` lässt sich als `[aber hallo]` $^1$ komprimieren.

Der *Kompressionsgrad* (`K`) ergibt sich aus der Länge der ursprünglichen Nachricht `l(N)` und der Kompression `k`: 

$$
K = \frac{k}{l(N)}
$$

In unserem Beispiel haben alle Nachrichten die Länge `10`. 

Daraus ergeben sich die folgenden Kompressionsgrade: 

| Nachricht | Kompressionsgrad |
| :--- | :--- |
| `"aaaaaaaaaa"` | 1 |
| `"ababababab"` | .5 |
| `"aber aber "` | .2 |
| `"aber hallo"` | .1 |

Die Kompressionsgrade stehen im umgekehrten Verhältnis zum Informationsgehalt ($I_g$) einer Nachricht. Es gilt also: 

$$
I_g = \frac{1}{K} = \frac{l(N)}{k}
$$

> **Merke:** Je stärker eine Nachricht komprimiert werden kann, desto weniger Information enthält sie. 

> Eine Nachricht mit dem Kompressionsgrad `1` wird als *informationslos* bezeichnet. Sie enthält also *keine* Information.


## Zusammenfassung: Symbole und Bits

Ausgehend von der Informationstheorie bestehen Nachrichten aus Symbolen. Symbole können Sätze, Worte, Wortkombinationen, Buchstaben oder Buchstabenfolgen sein. Ein Symbol repräsentiert einen Teil einer Nachricht.

> **Definition:** Ein Symbol einer Nachricht wird als **Bit** (engl. Teil) bezeichnet. 

In den vorherigen Abschnitten haben wir wichtige Erkenntnisse abgeleitet: 

1. Symbole können aus einfacheren Symbolen zusammengesetzt sein. 
1. Zahlensysteme **kodieren** Zahlenwerte zu einer Basis. 
2. Die Basis eines Zahlensystems legt fest, wie viele Ziffern für Zahlenwerte zur Verfügung stehen. 
3. Die kleinste Basis für ein Zahlensystem ist 2.
4. Beliebige Symbole als Zahlenwerte abgebildetet werden können. 
5. Ziffern sind Symbole. 

Daraus ergibt sich der folgende Merksatz. 

> **Merke:** Das die einfachste Bit-Kodierung für eine Nachricht ist die Unterscheidung zwischen `0` und `1`.