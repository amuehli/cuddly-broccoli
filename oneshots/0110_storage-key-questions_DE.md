<!--
icon: ../resources/logos/C3RDM_EN_V3_transparent_w1156.png
-->

---
# Einführung in den Themenblock 1: "Leitfragen Speicher"

Das Thema Speicherung zieht sich wie ein roter Faden durch das Forschungsdatenmanagement und ist sehr komplex. Dies ist nicht zuletzt so, weil sich im Verlauf eines Forschungsprojektes die Anforderungen, die an Speicherlösungen gestellt werden, stark voneinander unterscheiden können. Deshalb ist es wichtig, am besten schon so früh wie möglich die wichtigsten Fragen zum Speicher in verschiedenen Projektphasen zu stellen und entsprechende Lösungen zu planen – das ist das Ziel des Themenblocks **Leitfragen Speicher**.

Diese **Leitfragen** sind:

1. **Wie viel** Speicherplatz wird voraussichtlich benötigt? **Wie lange** wird zu welchem Zweck gespeichert?
2. Welche Vorsichtsmaßnahmen sollten **zum Schutz vor Datenverlust** getroffen werden?
3.  **Wer** braucht **Zugang**? Gibt es **sensible** Daten und ist die **Speicherlösung hierfür geeignet**?

Themen, die dabei behandelt werden sind u.a.: Replikation, Versionierung, Backup, Archivierung, DSGVO, Verschlüsselung, Passwortmanager

Wenn Sie anhand der Fragen eine bessere Vorstellung darüber gewonnen haben, was sie bei der Planung Ihrer Speicherlösungen berücksichtigen sollten, liefert der [Themenblock 2: Speicherlösungen](./oneshots/0120_storage-solutions_DE.md) einen Überblick über die physischen Speicher (das "Blech"), die an der Universität zu Köln zur Verfügung stehen und der [Themenblock 3: Organisation Daten](./0130_organization-documentation_DE.md) behandelt Themen rund um die Organisation und Dokumentation der Daten, wenn eine Speicherlösung gefunden ist.

---
## Was sind Forschungsdaten?

Forschungsdaten und Forschungsmaterialien können, je nach wissenschaftlicher Disziplin und verwendeten Methoden, sehr unterschiedlicher Art sein. Forschungsdatenmanagement (FDM) bezieht sich in der Regel auf den Umgang mit **digitalen Forschungsdaten**. Neben diesen gibt es aber auch **nicht digitalen Forschungsmaterialien**, die berücksichtigt werden müssen:

**digitale Forschungsdaten**, z.B.:

- digital vorliegende Messwerte, Texte, Audio- und Videodaten, etc.
- Elektronische Laborbücher (ELN), Codebücher, Dokumentationen

**digitalisierbare Forschungsmaterialien**, z.B.:

- nicht digitale Laborbücher
- nicht digitalisierte Datenträger (VHS, Tonband)
- Fragebögen, Einverständniserklärungen, Schlüssellisten

Es ist wichtig zu bedenken, dass diese Materialien ebenfalls zur Nachprüfbarkeit der Forschungsergebnisse erforderlich sein können und damit zu den erhaltenswerten Forschungsdaten zählen. In vielen Fällen lassen sich diese verlustfrei digitalisieren und archivieren. Außerdem gibt es digitale Alternativen wie z.B. elektronische Laborbücher (ELN) und digitale Aufnahmegeräte, wodurch digitale Forschungsdaten im Sinne des FDM entstehen.

**nicht/unvollständig digitalisierbare Forschungsmaterialien**, z.B.:

- tote/lebende/vergängliche Proben (z.B. Saatgut)
- (historische) Gegenstände/Fundstücke (z.B. Bücher, Bilder, andere Exponate)

Diese physischen Forschungsmaterialien sind i.d.R. nicht (z.B. original Fundstücke) oder nicht einfach (z.B. Saatgut) duplizier- bzw. verlustfrei digital abbildbar. Daher gehört die archivgerechte Aufbewahrung solcher Materialien in die Hände spezifisch geschulter Archivar:innen und spezialisierter Facheinrichtungen.

C³RDM hingegen ist auf digitales Forschungsdatenmanagement spezialisiert und unterstützt beispielsweise bei der Entwicklung eine Datenstrategie für Digitalisate von Forschungsmaterialien oder für die bei der Erschließung anfallenden Metadaten.

---
## Wert von Forschungsdaten und -materialien

Unabhängig davon, mit welcher Art Forschungsdaten und Forschungsmaterialien wir es zu tun haben - in der Regel ist ihnen gemein, dass sie für Forschende aus verschiedenen Gründen sehr wertvoll sind:

**Forschungsdaten und -materialien sind extrem wertvoll**

- **monetär** (z.B. teure Proben, Materialien, Umfragen)
- **Zeit** (z.B. langwierige Feldphase, Wartezeit Zugang Messinstrument)
- **Einmaligkeit** von Daten (z.B. Beobachtungsdaten astronomischer Ereignisse)
- Bedeutung für eigene **Karriere** (z.B. Datengrundlage für Promotion)
- Bedeutung für **Wissenschaft/Menschheit** (z.B. Forschungsdaten für Vakzin)

Aus diesen Gründen ist es wichtig, sich bereits früh im Forschungsprozess Gedanken darüber zu machen, wie Forschungsdaten und Forschungsmaterialien möglichst sicher aufbewahrt werden, damit sie nicht verloren gehen können.

---
# Leitfragen Speicher I

Im weiteren Verlauf konzentrieren wir uns auf das Management digitaler Forschungsdaten. Eine der ersten und offensichtlichsten Aufgaben ist dabei die Speicherung.

**Es gibt eine Reihe von Leitfragen zur Orientierung. Beginnen wir zunächst mit:**

- **Wie viel** Speicherplatz wird voraussichtlich benötigt?
- **Wie lange** wird zu welchem Zweck gespeichert?

Abhängig von der jeweiligen Projektphase können die Antworten unterschiedlich ausfallen – und damit geht einher, dass auf verschiedene Aspekte bei der Planung der Speicherung geachtet werden muss.

**Im Folgenden geht es daher um die schrittweise Klärung der Rahmenbedingungen:**

- [Datennutzungsszenarien](#datennutzungsszenarien)
- [Geschwindigkeit vs. Kapazität](#geschwindigkeit-vs-kapazität)
- [Speicherdauer und -zweck](#speicherdauer-und-zweck)

---
## Datennutzungsszenarien

Oft unterscheiden sich in Forschungsprojekten die Anforderungen, die an digitale Datenspeicher gestellt werden, erheblich in verschiedenen Phasen eines Projekts. In der Regel korrespondieren diese Anforderungen mit der in der IT üblichen Unterscheidung in heiße, warme und kalte Daten bzw. Speichermöglichkeiten (auch „tiered storage“ genannt).

Über den Zeitverlauf lässt sich das so visualisieren:

![Zeitachse von links nach rechts: Heiße, warme und kalte Speicher über Zeit mit heißem Speicher zu Beginn und kaltem zum Ende hin.](../resources/figures/storage-hot-warm-cold_DE_0010_data-usage-scenarios_w1920.png "Speicher heiß, warm, kalt - DE - 0010 - Datennutzungsznenarien, Lizenz: CC0")

Dabei geht es bei der Temperaturanalogie zunächst um die **Unterscheidung, wie oft auf die Daten zugegriffen wird bzw. wie schnell der Datenzugriff sein muss**, um sinnvoll mit den Daten arbeiten zu können: Je heißer bedeutet dabei um so mehr bzw. um so schneller. Das spielt beispielsweise dann eine Rolle, wenn bei einer Messung oder einer Simulation ein großer Strom an Daten anfällt, der dann schnell untergebracht werden muss.

Im Forschungsdatenalltag bedeutet das üblicherweise:

- Im Prozess der Datenproduktion und Auswertung wird oft aktiver und mit größeren Datenmengen gearbeitet. Um solche großen Datenmengen speichern oder verarbeiten zu können, müssen diese schneller gespeichert und gelesen werden können; die Daten werden als "heiß" bezeichnet.
- Im weiteren Verlauf kühlen sich die Daten oft ab. Mit den nun "warmen" Daten wird zwar noch aktiv gearbeitet, die Geschwindigkeit, mit der auf sie zugegriffen werden muss und die Datenmengen, die aktiv benötigt werden, reduzieren sich aber.
- Insbesondere am Ende eines Projekts ist der aktive Zugriff auf Daten eher die Ausnahme und der dauerhaft sichere Datenerhalt wird wichtiger als der schnelle Zugriff – wir sind bei "kalten" Daten angelangt.

---
## Geschwindigkeit vs. Kapazität

Die Speichersysteme für heißere Daten sind in der Regel performanter in Bezug auf Zugriffs- und Schreibgeschwindigkeit – d.h. sie erlauben schnelleren Zugang zu den Daten bzw. schnellere Speicherung. Je kälter die Daten werden, desto weniger performant muss das System diesbezüglich sein, weil auf die Daten eher seltener zugegriffen wird bzw. eine langsamere Schreib- oder Lesegeschwindigkeit keinen relevanten Flaschenhals mehr darstellt.

![Von heißem zu kaltem Speicher über Zeit mit inverser Beziehung zwischen Geschwindigkeit und Kapazität. Zu Beginn bei heißem Speicher hohe Geschwindigkeit mit geringer Kapazität und zum Ende bei kaltem Speicher geringe Geschwindigkeit bei hoher Kapazität.](../resources/figures/storage-hot-warm-cold_DE_0020_speed-vs-capacity_w1920.png "Speicher heiß, warm, kalt - DE - 0020 - Geschwindigkeit vs. Kapazität, Lizenz: CC0")

Umgekehrt verhält es sich mit der Kapazität (und Langlebigkeit) der Speichersysteme: Hier sind die Hochkapazitätssysteme eher bei kalten Daten zu finden, die dauerhaft archiviert werden sollen, weil hier große Mengen an Daten über lange Zeiträume kumulieren. Kapazität und Sicherheit haben dann Priorität, Geschwindigkeit spielt keine Rolle mehr für den Projekterfolg. Die schnellen, heißen Datenspeicher haben hingegen oft nur (relativ) geringe Kapazität, weil hier verhältnismäßig teure Speichersysteme zum Einsatz kommen.

Auf dem Kontinuum zwischen heißen und kalten Daten gibt es nun verschiedene Lösungen für warme Daten, die sich zwischen diesen beiden Extremen befinden. Aus der Sicht eines Rechenzentrums ist es wünschenswert, Daten schnellstmöglich von den heißen auf warme Speicher zu verschieben, um die teuren und meist knapperen Ressourcen heißer Speicher wieder freigeben zu können. Speicher für kalte Daten haben hingegen oft besondere Eigenschaften, so dass diese kalten Speicher erst sinnvoll sind, wenn Daten tatsächlich archiviert werden sollen und nur noch selten zugegriffen werden.

---
## Speicherdauer und -zweck

Einerseits gibt es immer mehr Speichermedien, worauf auch große Datenmengen gespeichert werden können. Andererseits fallen auch immer mehr Daten an, womit die Medien gefüllt werden. In der Praxis führt das leider dazu, dass oft einfach alle anfallenden Daten unselektiert abgelegt werden. So entstehen häufig undokumentierte und nicht ausreichend gewartete Datengräber, deren Speichermedien irgendwann ausfallen. Dann ist im Nachhinein unklar, ob darunter potenziell wichtige Daten verloren gegangen sind.

Aus diesem Grund sollte im Vorfeld darüber entschieden werden, warum welche Daten für welche Dauer sinnvoll aufzubewahren sind, damit diese mit vertretbarem Aufwand entsprechend ausreichend dokumentiert werden können. Um Ergebnisse nachvollziehen zu können ist es oft ebenso klug z.B. Skripte für Auswertungen und eine Dokumentation von Berechnungs- oder Bearbeitungsschritten zu erhalten. Zusätzlich macht es dabei einen großen Unterschied, ob die Daten nur für die Projektlaufzeit, für eine Dekade oder längerfristig festgehalten werden sollen.

**Typische Gründe für die längerfristige Speicherung von Daten sind:**

- Dokumentation der eigenen Forschungstätigkeit
- eigene weiterführende Auswertungen zu einem späteren Zeitpunkt
- [Gute Wissenschaftliche Praxis](https://doi.org/10.5281/zenodo.3923601) (i.d.R. 10 Jahre)
- gesetzliche Regelungen (z.B. i.d.R. [30 Jahre für stationäre medizinische Versorgungsdaten](http://www.nestor.sub.uni-goettingen.de/bestandsaufnahme/kapitel/nestor_bestandsaufnahme_012.pdf))
- Nachnutzung der Daten durch Dritte (oft als Anforderung durch Förderer oder Fachgesellschaften)

---
# Leitfragen Speicher II

**Kommen wir zur nächsten Leitfrage:**

- ~Wie viel Speicherplatz wird voraussichtlich benötigt?~
- ~Wie lange wird zu welchem Zweck gespeichert?~
- Welche Vorsichtsmaßnahmen sollten zum **Schutz vor Datenverlust** getroffen werden?

Vorsichtsmaßnahmen zum Schutz vor Datenverlust erfordern eine sorgfältige Planung, insbesondere weil diese Maßnahmen je nach Projektphase und Datennutzungsszenario (also der "Temperatur" der Daten) variieren. Daher ist eine abgestimmte **Datensicherheitsstrategie** für alle Phasen des Projekts und alle Datennutzungsszenarien erforderlich.

**Im Folgenden geht es um die Grundlagen von Datensicherheitsstrategien:**

- [Replikation](#datensicherheitsstrategie-replikation)
- [Versionierung](#datensicherheitsstrategie-versionierung)
- [Backup](#datensicherheitsstrategie-backup)
- [Archivierung](#datensicherheitsstrategie-archivierung)

---
## Datensicherheitsstrategie: Replikation

Da Ihre Forschungsdaten wertvoll sind (z.B. wegen der Kosten oder der Einzigartigkeit), ist es von entscheidender Bedeutung, dass die Sicherheit Ihrer Daten jeder Zeit gewährleistet ist. Eine Datensicherheitsstrategie umfasst mehrere Schritte, die wir nacheinander durchgehen, beginnend mit der **Replikation**:

Bei der Replikation werden Ihre Daten von Beginn an redundant auf mehrere Speichermedien parallel gespeichert – es gibt also nicht nur ein Original, sondern mehrere Duplikate, die (automatisch) in Echtzeit angefertigt werden. Das kann darüber geschehen, dass die Daten z.B. auf mehrere Festplatten gleichzeitig gespeichert werden – die Daten der Platten stellen dann jeweils eine Spiegelung der anderen dar. Es können aber für die Replikation auch zwei ganz verschiedene Speichermedien zum Einsatz kommen, beispielsweise eine lokale Festplatte bei gleichzeitiger Speicherung der Daten in der Cloud, die mit dem lokalen Speichermedium synchron gehalten wird.

![Zeitstrahl von links nach rechts. Darunter, von links an erster Stelle, Replikation: Zwei Datencontainer sind übereinander gespiegelt und beinhalten zum Zeitpunkt t=0 die gleichen Daten parallel. Unten: Legende mit Angaben für Datenträger und jetzigen Zeitpunkt.](../resources/figures/data-security-strategy_DE_0010_replication_legend_w1920.png "Datensicherheitsstrategie - DE - 0010 - Replikation, Lizenz: CC0")

In der Abbildung steht dabei t<sub>0</sub> für den gegenwärtigen Zeitpunkt auf der Zeitachse. Die beiden Zylinder beschreiben zwei getrennte Speichermedien, die beide identischen Inhalts sind und den aktuellen Stand der Daten beinhalten.

---
### Überblick Replikation

**Replikation:**

- erstellt ein Duplikat Ihrer Daten in Echtzeit – die Daten werden auf mehrere Medien gespiegelt
- typische Beispiele:

  - Cloud-Speicher, der (automatisch) sofort alle Änderungen lokal gespeicherter Dateien synchronisiert.
  - RAID 1[^1] (oft eine Option für NAS-Systeme [^2]) bezeichnet einen Festplattenverbund, bei dem neue oder veränderte Dateien nicht wie üblich auf nur ein lokales Laufwerk, sondern auf (mindestens) zwei physische Laufwerke parallel geschrieben werden.

- Vorteile:

  - Redundanz durch die Spiegelung der Daten: selbst wenn eine Kopie komplett ausfällt, sind trotzdem noch alle Daten vorhanden – auch die jüngsten Änderungen.
  - Im Fall von RAID 1 kann bei Ausfall eines der gespiegelten Medien trotzdem normal weitergearbeitet werden. Bei nur zwei Festplatten im Verbund allerdings liegt keine Redundanz mehr vor, bis das defekte Medium ersetzt und die Daten wieder gespiegelt worden sind.

- Nachteile:

  - Ein Fehler (z.B. eine versehentlich gelöschte oder überschriebene Datei) oder eine Schadsoftware (z.B. Ransomware, auch als Erpressungs- oder Kryptotrojaner bekannt) wirkt sich sofort auf alle Replikate aus.
  - Replikation bietet keinen Schutz vor einem katastrophalen Ereignis (z.B. einem Brand).
  - Das zur Verfügung stehende Speichervolumen reduziert sich, weil mehrere Medien die gleichen Daten beinhalten.

---
[^1] RAID steht für "redundant array of independent disks" (DE: redundantes Array unabhängiger Festplatten). Die Nummer spezifiziert den sog. RAID-Level, die für sehr unterschiedliche Szenarien gedacht sind. Der hier beschriebene Level 1 steht für "Spiegelung" (EN: mirroring).

[^2] NAS steht für "network attached storage" (DE: netzgebundener Speicher), im Prinzip ein spezialisierter Computer zur Verwaltung und Bereitstellung von Speicherkapazitäten über ein Netzwerk.

---
## Datensicherheitsstrategie: Versionierung

Datenverlust geschieht nicht allein durch Hardwaredefekte oder katastrophale Ereignisse. Oft reicht schon ein Moment der Unaufmerksamkeit.

Das versehentliche Löschen einer Datei kann in modernen Dateisystemen (über den Papierkorb) in der Regel einfach rückgängig gemacht werden. Anders sieht es aus, wenn versehentlich eine Datei überschrieben wird: Stellen Sie sich vor, sie möchten eine doch nicht so gelungene Umformulierung eines besonders anspruchsvollen Textabschnitts wieder rückgängig machen, haben aber in der Zwischenzeit schon auf 'Speichern' geklickt – in diesem Fall sind ohne weitere Vorkehrungen die Informationen der überschriebenen Dateiversion unwiederbringlich verloren.

Besonders bei der Arbeit mit Datensätzen kommt es nicht selten zur Entdeckung eines Fehlers (z.B. durch eine Transformation) erst nachträglich, ohne dass es eine Möglichkeit gibt, zur alten Version zurückzukehren.

Hier hilft die **Versionierung**:

![Zeitstrahl von links nach rechts. Darunter, von links an zweiter Stelle, Versionierung: Mehrere Dokumente sind vom Zeitpunkt t=0 nach links in die Vergangenheit versetzt angeordnet und symbolisieren verschiedene Zustände der aktuellen Datei in die Vergangenheit hinein. Unten: Legende mit Angaben für Datenträger, jetzigen Zeitpunkt, Datei und vorherigen Zeitpunkt.](../resources/figures/data-security-strategy_DE_0020_versioning_legend_w1920.png "Datensicherheitsstrategie - DE - 0020 - Versionierung, Lizenz: CC0")

Durch die Versionierung wird nicht nur der aktuelle Zustand einer Datei gespeichert (z.B. File A zum Zeitpunkt t<sub>0</sub>), sondern es werden verschiedene Versionen der gleichen Datei aus der Vergangenheit ebenfalls gespeichert (File A zu den vergangenen Zeitpunkten t<sub>-1</sub>, t<sub>-2</sub>, t<sub>-3</sub> usw.).

---
### Gängige Versionierungsansätze

Oft werden im Rahmen von auto-save-Funktionen in Programmen Versionen automatisch nach bestimmten Zeitintervallen (z.B. alle 10 Minuten) und für eine bestimmte Anzahl von Versionen (z.B. die letzten 10 Versionen) gespeichert, häufig aber nur bis eine manuelle Speicherung oder das Schließen des Programms erfolgt. Dies greift für eine Versionierung zu kurz, weil dafür einige der vergangenen Zustände längerfristig erhalten bleiben sollten. Auch liefern nicht alle relevanten Programme solche Funktionen oder sie sind verschieden implementiert, was eine regelhafte und verlässliche Versionierung erschwert.

Ziel einer Versionierung ist es also **systematisch** ältere Zustände zu behalten, um diese ganz oder teilweise wiederherstellen zu können. Dabei werden oft kürzer getaktete Versionen (und damit mehr Speicherpunkte pro Zeiteinheit) in der jüngeren Vergangenheit angelegt, um Fehler an aktuelleren Bearbeitungen gezielt rückgängig machen zu können. Je weiter die Bearbeitungen zurückliegen, desto weniger Versionen sind in den meisten Anwendungsfällen pro Zeiteinheit notwendig – die Speicherpunktdichte reduziert sich folglich mit größerem zeitlichen Abstand. Hier ist es wichtiger möglichst lange Zeiträume abzudecken. Denn je länger diese zurückreichen, desto wahrscheinlicher kann auch ein längere Zeit unentdeckter Fehler wieder rückgängig gemacht werden. Dieser Prozess kann manuell vorgenommen werden oder automatisiert ablaufen (z.B. über Skripte).

Automatisierte Prozesse laufen dabei i.d.R. letztlich nach einem bestimmten Zeitraster – was auch für manuelle Speicherungen imitiert werden kann (z.B. eine Speicherung einer Version am Ende eines jeden Arbeitstags). Ein anderer Ansatz ist die bewusste und schriftlich dokumentierte Entscheidung, zu welchen Zeitpunkten bestimmte Dateizustände festgehalten werden sollen – dies kann manuell über das Anlegen von Kopien und das Führen einer Dokumentation zu den verschiedenen Versionen geschehen oder über spezielle Versionierungstools wie [git](https://git-scm.com/).

---
### Überblick Versionierung

**Versionierung:**

- Speicherung von Kopien verschiedener Zustände geänderter Dateien über Zeit
- typische Beispiele:

  - MS Word AutoSave
  - Git
  - (leider oft unsystematisches) manuelles Speichern von Kopien und Dokumentation

- Vorteil: Eine ordnungsgemäße Versionierung bietet eine Historie Ihrer Arbeit, so dass Sie den aktuellen Zustand mit älteren Versionen vergleichen können, um ggf. Probleme oder Fehler zu erkennen.
- Nachteil: Eine schlecht implementierte Versionierung kann zu Unordnung und Verwirrung führen, beispielsweise wenn manuell Kopien über Kopien gemacht werden, die aber nicht klar benannt sind und dazu einladen, mit einer obsoleten Version weiterzuarbeiten.

---
## Datensicherheitsstrategie: Backup

Die vermutlich geläufigste Datensicherheitsstrategie dürfte das klassische Backup sein, verstanden als Sicherheitskopien der vorhandenen Daten zu bestimmten Zeitpunkten:

Backups stellen häufig die einzig vorgenommene Form der Datensicherheitsstrategie dar. Auch wenn ein Backup besser ist als gar keine Maßnahme zur Datensicherheit, so sind Backups leider oft unbrauchbar implementiert. Wird nämlich nur eine Kopie der aktuellen Daten zu unregelmäßigen Zeitpunkten vorgenommen und irgendwo auf dem internen Speicher des zu sichernden Systems gespeichert, geht das Backup ebenfalls verloren falls dieses System kompromittiert wird. Genau dies soll ein Backup aber verhindern.

Eine der Kerneigenschaften eines Backups ist deshalb, dass es außerhalb – und damit unabhängig – des aktiven Speichersystems liegen soll, z.B. auf externen Medien oder Servern. Dabei ist nicht nur wichtig, dass die Systeme nicht permanent verbunden sind – also im Vergleich zur Replikation nicht sofort alle Änderungen am aktiven Speicher auch am Backup vorgenommen werden -, sondern idealerweise auch eine räumliche Trennung erfolgt, damit ein katastrophaler Zwischenfall wie ein Brand oder eine Flut nur mit geringerer Wahrscheinlichkeit auch das Backup zerstören können.

![Zeitstrahl von links nach rechts. Darunter, von links an dritter Stelle, Backup: Zwei Datencontainer sind vom Zeitpunkt t=0 nach links in die Vergangenheit versetzt angeordnet und symbolisieren Kopien aller Daten zu verschiedenen Zeitpunkten in der Vergangenheit. Unten: Legende mit Angaben für Datenträger, jetzigen Zeitpunkt, Datei und vorherigen Zeitpunkt.](../resources/figures/data-security-strategy_DE_0030_backup_legend_w1920.png "Datensicherheitsstrategie - DE - 0030 - Backup, Lizenz: CC0")

Die Abbildung verdeutlicht, dass Backups, im Gegensatz zur Replikation, nicht den Ist-Zustand speichern, sondern zeitlich versetzt (t<sub>-1</sub>, t<sub>-2</sub>, ...) mehrere (idealerweise: möglichst viele und möglichst lange zurückreichende) Kopien aller Daten umfassen.

---
### Gängige Backup-Typen

Backup-Schemata beginnen in der Regel mit einer vollständigen Kopie aller Daten (**Voll-Backup**).

Beim sogenannten **inkrementelle Backups** wird für alle weiteren Backups jeweils der Unterschied zwischen Original und letztem vorangegangenen Backup verglichen - und nur die jeweiligen Änderungen gespeichert: 1) Voll-Backup, 2) nur Änderungen seit Voll-Backup, 3) nur Änderungen seit den letzten Änderungen usw. Dies hat gegenüber dem Voll-Backup den Vorteil, dass die inkrementelle Sicherung schneller geht und weniger Speicher benötigt. So können mehrere inkrementelle Backups – und damit Sicherungen mehrerer Zeitpunkte – auf einem Speichermedium untergebracht werden.

Für die Wiederherstellung sollte beachtet werden, dass nicht zu viele inkrementelle Backups vor der nächsten vollständigen Kopie erstellt werden sollten. Sonst kann der Vorgang komplizierter (und damit unsicherer) werden, weil nicht nur die ursprüngliche Kopie aller Daten (die den ältesten Zustand beinhaltet) wiederhergestellt werden muss, sondern auch sukzessive alle inkrementellen Änderungen, die aufeinander aufbauen und nur gemeinsam das aktuellste Backup ausmachen.

Das **differenzielle Backup** stellt einen Kompromiss in Bezug auf Backup-Geschwindigkeit und Speicherplatz dar – es bezieht sich immer auf das letzte Voll-Backup und ist daher einfacher wiederherzustellen, benötigt aber wiederum mehr Zeit und Speicherplatz als das inkrementelle Backup.

Außerdem empfiehlt es sich mehrere Speichermedien einzusetzen, um mehr Zeitpunkte sichern zu können.

---
### 3-2-1-Backup

Idealerweise kommen professionelle, institutionalisierte Backup Lösungen zum Einsatz, die von Spezialist:innen entwickelt und gewartet werden (für Lösungen der UzK siehe den [C³RDM-Servicekatalog](https://fdm.uni-koeln.de/serviceangebot/servicekatalog-1), Stichwort ["Backup and Archive"](https://fdm.uni-koeln.de/serviceangebot/servicekatalog-1#c123782)). Als Wissenschaftler:in ist es aber oft auch sinnvoll, eine Lösung für eigene Forschungsdaten zu haben, die auch bei einem Institutionenwechsel funktioniert z.B. in einer Übergangsphase die Sicherheit Ihrer Daten sicherstellt.

Auch wenn es keine umfassende Datensicherheitsstrategie ist, so ist die einfachste empfehlenswerte Minimallösung das sogenannte **3-2-1-Backup Regime**:

- mindestens **3 Kopien**  

  Redundanz reduziert die Ausfallwahrscheinlichkeit. Die Erfahrung zeigt außerdem, dass im tatsächlichen Ernstfall gerne schon mal mindestens ein Backup beim Wiedereinspielen beschädigt wird durch Anwendungsfehler in einer Stresssituation
- auf mindestens **2 verschiedenen Speichermedien** (und von mindestens 2 Personen zugänglich)  

  Verschiedene Medien reduzieren u.a. die Wahrscheinlichkeit für den gleichzeitigen Ausfall mehrerer Sicherungen, beispielsweise weil eine defekte Charge einer Festplattenproduktion vorliegt. Mehrere Personen mit Zugriff – z.B. bei verschlüsselten Lösungen – erlauben Kontinuität auch bei personellen Ausfällen.
- davon mindestens **1 dezentral**  

  Damit z.B. bei einem Brand nicht alle Backups gemeinsam mit dem Original verloren gehen, weil diese im gleichen Gebäude lagern.

(ein ausführlicheres und praktisches Tutorial zu 3-2-1-Backup ist geplant)

---
### Überblick Backup

**Backup:**

- Erstellt wird ein Duplikat Ihrer Daten zu bestimmten Zeitpunkten (z.B. täglich, wöchentlich und monatlich) mit mindestens einer dezentralen (externen) Kopie.
- typische Beispiele:

  - Backup-Lösung über NAS
  - Backup-Kopien auf externen Medien (z.B. externen Festplatten)
  - Apple Time Machine
  - 3-2-1-Backup (Tutorial in Planung)

- Auf ein Voll-Backup folgen in der Regel inkrementelle Backups, um Zeit und Speicherplatz zu sparen – bis ein neuer Zyklus mit einer vollständigen Kopie beginnt.
- Vorteil: Selbst nach dem Verlust aller aktiven Systeme (z.B. durch Überspannung, Feuer oder Schadsoftware) ist eine nahezu vollständige Wiederherstellung der Daten möglich. Dies gilt auch, wenn der Datenverlust nicht sofort entdeckt wird, vorausgesetzt, dass die Backups lange genug zurückreichen.
- Nachteil: Neue Daten und aktuelle Änderungen, die noch nicht in einer aktuellen Sicherung enthalten sind, gehen verloren.

---
## Datensicherheitsstrategie: Archivierung

Die Archivierung ist ein Prozess, der nur zu bestimmten Zeitpunkten stattfindet. In der Regel werden am Projektende ausgewählte und kuratierte Datensets in einer endgültigen Fassung zur dauerhaften Aufbewahrung an ein Archiv übergeben. In manchen Fällen empfiehlt sich aber auch die frühzeitige Archivierung bestimmter, besonders wichtiger Daten:

![Zeitstrahl von links nach rechts. Darunter, von links an vierter Stelle, Archivierung: Ein ausgewählter Datensatz wird zum aktuellen Zeitpunkt in eine preservation black box der Erhaltung der Archivdaten gegeben und kann dieser, nach einem unbestimmten Zeitintervall, wieder entnommen werden. Unten: Legende mit Angaben für Datenträger, jetzigen Zeitpunkt, Datei, vorherigen Zeitpunkt, Unveränderbarkeit und Zeitpunkt der finalen Version.](../resources/figures/data-security-strategy_DE_0040_archive_legend_w1920.png "Datensicherheitsstrategie - DE - 0040 - Archivierung, Lizenz: CC0")

Wie in der Abbildung dargestellt, werden aus dem vollständigen Datenbestand üblicherweise nur einzelne Datensätze (t <sub>fin</sub> als finale Fassung) ausgewählt, die in genau diesem Zustand (deshalb das Schlosssymbol) für einen längeren Zeitraum erhalten werden sollen (idealerweise inf. also unendlich): Dies können im Fall der Archivierung besonders wichtiger heißer oder warmer Daten wenige Jahre der Projektlaufzeit sein, für kalte Daten sind es mindestens 10 Jahre Aufbewahrungsfrist gemäß **Guter Wissenschaftlicher Praxis**, es gibt aber auch besonders erhaltenswerte Daten, die für eine **Langzeitarchivierung** vorgesehen sind und theoretisch auf unbestimmte Zeit erhalten bleiben sollen. Für eine solche Langzeitarchivierung spielen dann Auswahl, Dokumentation und Beschreibung sowie der sehr komplexe Prozess der Erhaltung/Kuration (preservation black box) eine besondere Rolle (ausführlichere Darstellung in einem gesonderten Themenblock, derzeit noch in Entwicklung, vgl. [Überblicksseite der Themenblöcke](https://www.ilias.uni-koeln.de/ilias/goto_uk_fold_4178361.html)).

---
### Typische Archivierungsszenarien

Es gibt bestimmte Daten, die bereits in frühen Projektphasen (in einer heißen oder warmen Phase) zur **(manipulations-)sicheren Aufbewahrung** archiviert werden sollten. Das ist z.B. der Fall, wenn es sich um Rohdaten einer Befragung handelt oder besonders aufwändig aufbereitete Daten als Grundlage weiterer Analysen, die oft zur Dokumentation und späteren Kontrolle über die gesamte Projektlaufzeit erhalten bleiben müssen. Zu diesem Zweck haben Rechenzentren üblicherweise besonders sichere Speicherlösungen im Angebot, die zusätzlich besondere Maßnahmen gegen Veränderung oder Manipulation der Daten beinhalten.

Insbesondere nach Abschluss eines Forschungsprojekts, wenn alle Forschungsdaten gesammelt, bereinigt, aufbereitet, ausgewertet oder sonst wie verarbeitet wurden (oder mit anderen Worten: wenn die Daten **kalt** sind), ist es sinnvoll – und aus Sicht der Guten Wissenschafltichen Praxis auch oft notwendig – die Daten zur längerfristigen Aufbewahrung zu archivieren und idealerweise Dritten zur Nachnutzung zur Verfügung zu stellen. Diese Aufgabe wird in der Regel von fachspezifischen oder generischen **Repositorien**[^1] übernommen. Im Idealfall stellen diese sicher, dass mindestens die Metadaten zu einem Projekt dauerhaft erhalten bleiben und FAIR[^2] sind; dass auch die zugehörigen Daten und deren Dokumentation möglichst lange (i.d.R. mind. 10 Jahre) archiviert werden; und, dass die Daten so offen, wie dies im Projektkontext und aus Datenschutz- und anderen Erwägungen möglich ist, für Dritte zur Nachnutzung angeboten werden.

Auch wenn der Begriff nicht trennscharf ist, ist die Perspektive langfristiger Speicherung unter dem Label der **Langzeitarchivierung** oft eine von unbestimmter Dauer, die aber über die 10 Jahre der Guten Wissenschaftlichen Praxis weit hinausgehen kann. Der Aufwand kann dabei enorm steigen, weil bei längeren Zeiträumen sowohl die technischen Hürden der reinen Speicherung komplexer werden als auch die der Lesbarkeit von Dateiformaten und Ausführbarkeit von Programmen sehr viel stärker berücksichtigt werden und in eine Erhaltungsstrategie eingehen müssen. Während eine 10-Jährige Speicherung unter den Maßgaben Guter Wissenschaftlicher Praxis idealerweise einfach für alle wissenschaftlichen Daten erfolgen sollte (wir klammern hier Datenschutz, Patente, bestimmte disziplinspezifische Besonderheiten etc. aus), kommt eine "echte" Langzeitarchivierung als wartungsintensiver, nur in Kooperation mit Spezialanbietern möglicher Prozess nur für besonders erhaltenswerte Daten in Frage (ausführlichere Darstellung in einem gesonderten Themenblock, derzeit noch in Entwicklung, vgl. [Überblicksseite der Themenblöcke](https://www.ilias.uni-koeln.de/ilias/goto_uk_fold_4178361.html)).

---
[^1] Ein Repositorium ist ein Dienst oder ein Ort zur Speicherung oder Ablage von Daten, im Kontext von Forschungsdaten meist ein Online-Repositorium zur Speicherung digitaler Daten. Die Speicherung erfolgt strukturiert, die Daten werden durch sogenannte Metadaten (Daten beschreibende Daten) beschrieben (z.B. Schöpfer:in, Datentyp, Erhebungsdatum usw.). Idealerweise ist die  Institution, die einen solchen Dienst anbietet, vertrauenswürdig (z.B. über Bekanntheit oder Zertifikate). Beispiel für ein (generisches) Forschungsdatenrepositorium ist [zenodo](https://zenodo.org/), ein Verzeichnis für Forschungsdatenrepositorien ist [re3data](https://www.re3data.org/). (ausführlichere Darstellung in einem gesonderten Themenblock, derzeit noch in Entwicklung, vgl. [Überblicksseite der Themenblöcke](https://www.ilias.uni-koeln.de/ilias/goto_uk_fold_4178361.html))

[^2] Die [FAIR-Prinzipien](https://www.go-fair.org/fair-principles/) geben Anregungen, wie Daten und Metadaten (Daten beschreibende Daten) so gestaltet werden können, dass diese möglichst gut gefunden werden können (**f**indable), zugänglich sind (**a**ccessible), zwischen verschiedenen Systemen austauschbar bzw. nicht an ein bestimmtes System gebunden sind (**i**nteroperable) um wiederverwertet werden zu können (**r**eusable). Dies soll maschinenlesbar umgesetzt werden, um die Verarbeitbarkeit des stetig anwachsenden Datenvolumen mittels Automatisierungsprozessen sicherzustellen (ausführlichere Darstellung in einem gesonderten Themenblock, derzeit noch in Entwicklung, vgl. [Überblicksseite der Themenblöcke](https://www.ilias.uni-koeln.de/ilias/goto_uk_fold_4178361.html)).

---
### Überblick Archivierung

**Archivierung:**

- Dauerhafte Aufbewahrung wichtiger Daten zur Gewährleistung der Sicherheit in einer manipulationssicheren, unveränderten Kopie und/oder Archivierung kuratierter Daten in speziellen Speicherlösungen und Datenzentren (Repositorien), die die langfristige Zugänglichkeit und Bewahrung gewährleisten
- typische Beispiele:

  - manipulationssichere, redundante und mehrfach gesicherte Speichersysteme in Rechenzentren (z.B. für Rohdaten)
  - Repositorien zur Archivierung und idealerweise Nachnutzung von Daten
  - Langzeitarchive (oft Speziallösungen)

- Vorteil: ermöglicht den langfristigen Datenerhalt
- Nachteil: In der Regel müssen die Daten sorgfältig aufbereitet und kuratiert werden, um eine ordnungsgemäße Langzeitarchivierung zu ermöglichen, was einen arbeits- und kostenintensiven Prozess darstellt.

---
## Datensicherheitsstrategie (komplett)

Insgesamt gibt es also vier Säulen, auf denen eine Datensicherheitsstrategie steht:

![Zeitstrahl von links nach rechts. Darunter, von links nach rechts angeordnet an einem Zeitstrahl, Abbildungen für Replikation, Versionierung, Backup und Archivierung. Unten: Legende mit Angaben für Datenträger, jetzigen Zeitpunkt, Datei, vorherigen Zeitpunkt, Unveränderbarkeit und Zeitpunkt der finalen Version.](../resources/figures/data-security-strategy_DE_0050_complete_legend_w1920.png "Datensicherheitsstrategie - DE - 0050 - komplett, Lizenz: CC0")

Replikation, Versionierung, Backups und Archivierung adressieren dabei unterschiedliche relevante Aspekte für die Sicherheit von (Forschungs-)Daten:

- **Replikation** geschieht in Echtzeit, so dass auch die jüngsten Änderungen erfasst werden, und schützt insb. vor einem Datenverlust durch Hardwareausfall im Speichersystem im laufenden Betrieb.
- **Versionierung** läuft automatisiert zu bestimmten Intervallen und/oder manuell angestoßen nach inhaltlich relevanten Kriterien und schützt u.a. vor versehentlichen Veränderungen. Versionierung kann auch Teil der Dokumentation von Forschungsarbeit sein.
- **Backups** werden üblicherweise in bestimmten Zeitintervallen durchgeführt, die je nach der erforderlichen Datensicherheit und den verfügbaren Ressourcen festgelegt werden, sind immer extern und schützen insb. vor dem Verlust aller Daten durch katastrophale Ereignisse wie Brände oder Befall durch Ransomware. Sie sind oft die letzte Rettungsmöglichkeit, selbst wenn die jüngsten Änderungen, die zwischen einem datenvernichtenten Ereignis und dem letzten (funktionierenden oder unkompromittierten) Backup verloren gehen.
- **Archive** kommen vor allem nach Abschluss eines Forschungsprojekts in Form von Repositorien zum Einsatz, um die Langzeitarchivierung sicherzustellen und gegebenenfalls die Nachnutzung der Daten zu ermöglichen. Für ausgewählte und besonders wichtige Daten (z.B. bestimmte Rohdaten), kann auch schon frühzeitige manipulationssicherere Archivierungen erforderlich werden.

Für eine umfassende Datensicherheitsstrategie werden Replikation, Versionierung und Backups (und gegebenenfalls auch Archivierung) idealerweise miteinander verbunden und auf das aktuelle Datennutzungsszenario angepasst. Denn je nachdem, ob in einer spezifischen Projektphase eher heiße, warme oder kalte Speicherlösungen benötigt werden, wird sich damit auch die Konfiguration einer adäquaten Datensicherheitsstrategie verändern.

---
## Planung einer Datensicherheitsstrategie

Unabhängig davon, wie genau eine Datensicherheitsstrategie umgesetzt wird, gibt es bestimmte Aspekte, die immer berücksichtigt werden sollten: Die **Auswahl der Daten** und die **Organisation der Sicherungen**.

**Auswahl der Daten**

- **Welche Daten** sind wichtig und müssen in Sicherungen eingeschlossen werden?
- **Wo** genau liegen die Daten?
- Was könnten Sie **vergessen** haben?  

  typische Beispiele:

  - (vermeintlich sichere) Daten in der Cloud  

    (z.B. E-Mails)


  - Browserdaten  

    (z.B. Lesezeichen, gespeicherte Passwörter – sind eigentlich keine gute Idee, aber seien wir realistisch ...)

  - schwer nachvollziehbare Einstellungen  

    (z.B. von Programmen oder Messgeräten)

  - arbeitsintensiv eingepflegte Metadaten  

    (kennen Sie z.B. den Pfad zur Datenbank Ihrer Bibliographiesoftware?)

**Organisation der Sicherung**

- **Wer** macht das Backup und  **wann**?  

  (klären Sie Zuständigkeiten in Arbeitsgruppen, setzen Sie sich Erinnerungen für Prüfungen und manuelle Prozesse)
- **Testen** Sie Ihre Lösungen **vorher**  

  (nicht das Backup/die Versionierung ist wichtig sondern die Wiederherstellung – probieren Sie vorher aus, ob Ihre Lösungen so funktionieren, wie Sie es erwarten, bitte mit unwichtigen oder anderweitig gesicherten Daten bzw. Kopien)
- Automatisierung  

  (automatisieren Sie Prozesse, wo möglich, kontrollieren Sie deren Ergebnisse oder verwenden Sie Monitoring-Lösungen, beispielsweise Backup-Monitoring integrierter Lösungen wie NAS)

---
## Empfehlungen zur Datensicherheitsstrategie

Die verschiedenen Komponenten einer umfassenden Datensicherheitsstrategie, die vielen Freiheitsgrade bei der Umsetzung, die potentiell katastrophalen Folgen bei Planungsfehlern und die sehr unterschiedlichen fach- und projektspezifischen Bedarfe machen Datensicherheit zu einer sehr komplexen Aufgabe, die allein kaum bewältigbar erscheint – und die oft genau aus diesen Gründen gar nicht erst umgesetzt wird. Dann ist aber nicht die Frage, **ob** es zum Datenverlust kommt, sondern eher **wann**.

Damit es nicht soweit kommt, hier ein paar **Empfehlungen**:

- nutzen Sie die **institutionalisierten Speicherlösungen** der UzK: Das RRZK (und teilweise Ihr Institut oder Ihr Projekt) bieten verschiedene Speicherlösungen an, die in eine Datensicherheitsstrategie eingebunden sind oder verschiedene Aspekte einer solchen abbilden. Für einen Überblick über Speicherlösungen siehe den Themenblock [**Speicherlösungen**](./0120_storage-solutions_DE.md).
- nutzen Sie **Beratungsangebote**: Speicherung und Datensicherheit sind ein integraler Bestandteil des Forschungsdatenmanagements – das [C³RDM-Team](https://fdm.uni-koeln.de/c3rdm-team) berät Sie gerne.
- wenn Sie sonst (noch) nichts tun, machen Sie **mindestens das 3-2-1-Backup** für Ihre eigenen Daten.

---
# Leitfragen Speicher III

**Kommen wir zu den letzten Leitfragen:**

- ~Wie viel Speicherplatz wird voraussichtlich benötigt?~
- ~Wie lange wird zu welchem Zweck gespeichert?~
- ~Welche Vorsichtsmaßnahmen sollten zum Schutz vor Datenverlust getroffen werden?~
- **Wer** braucht **Zugang**?
- Gibt es **sensible** Daten und ist die **Speicherlösung hierfür geeignet**?

Gerade wenn Forschende z.B. in einer Arbeitsgruppe gemeinsam an Projekten arbeiten, ist es wichtig sich Gedanken darüber zu machen, wer auf welche Daten **Zugriffsrechte** haben soll. Zusätzlich müssen Konflikte vermieden werden, wenn mehrere Personen kollaborativ an den gleichen Daten arbeiten.

Wenn es in einem Projekt **sensible Daten** gibt, dann reicht in der Regel ein einfaches Rechtemanagement nicht mehr aus um deren Sicherheit garantieren zu können. Hier müssen spezielle Speicherlösungen genutzt und die Daten gegebenenfalls verschlüsselt werden.

**Im Folgenden geht es um Grundlagen zum datenschutzkonformen Umgang mit Daten:**

- [Zugriffsrechte](#zugriffsrechte-synchronisation-und-kollaboration)
- [Was sind sensible Daten?](#sensible-daten)
- [sicherer Umgang mit sensiblen Daten](#sicherer-umgang-mit-sensibler-daten)
- [Anonymisierung](#anonymisierung)

---
## Zugriffsrechte, Synchronisation und Kollaboration

In vielen Projekt- und Forschungsszenarien sind es mehrere Personen, die kollaborativ mit Forschungsdaten arbeiten. Dabei ist es nicht immer notwendig und ggf. auch nicht empfehlenswert, allen Beteiligten Zugriff auf alle Daten zu gewähren. Gerade besonders sensible Informationen wie beispielsweise Pseudonymisierungslisten, die eine Zuordnung von Klarnamen zu Pseudonymen von Probanden erlauben, sollten besonders geschützt aufbewahrt werden und Zugang sollte nur einem möglichst kleinen, klar definierten Kreis möglich sein.

Selbst bei Daten, die nicht per se sensibel sind, ist es ratsam, **Zugriffsrechte** angemessen zu verwalten. So kann es z.B. sinnvoll sein, allen Projektbeteiligten Leserechte an einem zentralen Dokument zu geben, aber nur ausgewählten Personen auch Schreibberechtigung zu erteilen. Denn je nachdem, welche Speicherlösung verwendet wird, kann **kollaborative Bearbeitung** zu Versionskonflikten führen, die teilweise nur schwer aufzulösen sind und je nach technischer Implementation unter Umständen sogar erst auffallen, wenn es bereits zu Datenverlust gekommen ist.

Es gibt Programme, die bei der **Synchronisation** zwischen mehreren Geräten und mehreren Benutzer:innen unterstützen. Auch existieren Dateisysteme, die den Schreibzugriff auf Dateien, die durch andere Benutzer:innen bearbeitet werden, automatisch sperren und nur noch Lesezugriff gewähren. Oder es können sogar Tools benutzt werden, die kooperatives, gleichzeitiges Bearbeiten erlauben. Leider funktionieren diese Lösungen aber nicht immer in allen Datennutzungsszenarien und sind sehr von den Umständen abhängig.

**Es ist also wichtig vorab über folgende Fragen nachzudenken:**

- Wer braucht Zugang zu welchen Daten?
- Welcher Personenkreis sollte welche Rechte haben?
- Sollen mehrere Geräte mehrerer Nutzer:innen synchron gehalten werden?
- Soll es möglich sein, dass mehrere Personen gleichzeitig an den gleichen Dokumenten arbeiten?
- In welchen Projektphasen und für welche Daten soll das jeweils möglich sein?
- Was lässt sich davon mit den zur Verfügung stehenden Speicherlösungen umsetzen?
- Gibt es sensible Daten, die getrennt gehalten werden müssen?

---
## Sensible Daten?

Es gibt eine Reihe von Gründen, warum Daten sensibel sein können und (z.B. durch technische Maßnahmen) vor unberechtigtem Zugriff geschützt werden müssen. Daten können u.a.:

- **vertraglich geschützt** sein: Ein Beispiel wäre die Zusammenarbeit mit einem Unternehmen, das seine Geschäftsdaten für eine wissenschaftliche Analyse zur Verfügung stellt und mit dem ein Vertrag über die vertrauliche Nutzung geschlossen wurde.
- **urheberrechtlich geschützt** sein: Z.B. kann es zulässig sein Daten, obwohl sie urheberrechtlich geschützt sind, für wissenschaftliche Analysen zu vervielfältigen (beispielsweise beim Data Mining). Sie dürfen dann aber nur für eben diese wissenschaftliche Analyse genutzt werden – eine Weitergabe oder Veröffentlichung der Daten ist i.d.R. nicht zulässig und es ist sicherzustellen, dass auf diese nicht unberechtigt zugegriffen werden kann.
- **datenschutzrechtlich geschützt** sein: Hier finden sich die vielen verschiedenen Szenarien, bei denen die Datenschutzgrundverordnung (DSGVO) greift. Der Datenschutz ist ausschließlich dann relevant, wenn personenbezogene Daten vorliegen – beispielsweise die Namen von Probanden (auf diesen Punkt gehen wir gleich auch noch etwas detaillierter ein).
- aus **ethischen** oder anderen Gründen **schützenswert** sein: Unabhängig von bestehenden oder nicht bestehenden vertraglichen oder rechtlichen Schutzgründen können Daten auch aus ethischen oder anderen Gründen sensibel sein und deshalb zu schützen. Das wäre beispielsweise der Fall bei einem Projekt zum Geotagging von Wildtieren (wobei hier auch gesetzliche Schutzmaßnahmen gegen Wilderer greifen können) oder zur Erstellung besonders detaillierter Geodaten von Krisengebieten.

Die rechtlichen und ethischen Implikationen dieser Beispiele sind i.d.R. sehr komplex und selbst die Frage, ob und welche Rechtsnorm eine Rolle spielt (teilweise sind es auch mehrere gleichzeitig), ist oft nicht einfach zu beantworten. **C³RDM kann keine Rechtsberatung** vornehmen, sondern lediglich vorläufige Hinweise geben – und an die Rechtsexpert:innen der entsprechenden Beratungsinstanzen vermitteln (beispielsweise an die [Stabsstelle Datenschutz und IT-Sicherheit](https://verwaltung.uni-koeln.de/stabsstelle02.3/content/index_ger.html)).

---
### DSGVO – wann typischerweise anzuwenden

Datenschutzrechtlich geschützte Daten sind in bestimmten Disziplinen eher die Norm als die Ausnahme (z.B. Medizin, Soziologie, Bildungsforschung) und stellen besondere Herausforderungen an das Forschungsdatenmanagement. Denn während auf der einen Seite die Forderungen nach Nachnutzung und Transparenz von Daten stehen, muss auf der anderen Seite auch die informationelle Selbstbestimmung berücksichtigt werden.

Das ist insb. dann der Fall, wenn Daten unter die Datenschutzgrundverordnung (DSGVO) fallen. Das ist der Fall für **direkt oder indirekt personenbezogenen** Daten. Dabei handelt es sich um Informationen, die direkt (z.B. über einen Klarnamen) oder auch indirekt (z.B. ein Pseudonym) einer Person zugeordnet werden können.

Besonders wichtig zu beachten sind eben diese **"indirekt" personenbeziehbaren Daten**, die gerne übersehen werden. Die DSGVO ist auch dann relevant, wenn gar kein direkter Personenbezug besteht (also z.B. gar kein Name angegeben ist), aber z.B. die betreffende Person über eine Kombination von Merkmalen eindeutig identifiziert werden kann. Z.B. werden die Daten "Geschlecht", "Alter", "Klinik" und "Aufnahmedatum" sehr wahrscheinlich ausreichen, um eine bestimmte Person zu identifizieren. Bitte beachten Sie, dass es sich bei **pseudonymisierten Daten** um indirekte personenbezogene Daten handelt (und nicht um anonymisierte Daten) – es gilt also die DSGVO.

---
### DSGVO – was heißt das für die Daten?

Wenn Ihre Daten unter die DSGVO fallen, was bedeutet das dann üblicherweise?
Personenbezogene Daten genießen nun **Datenschutz** und dürfen i.d.R.:

- **nicht** einfach geteilt,
- **nicht** ohne besonderen (technischen) Schutz gespeichert,
- **nicht** ohne Einverständnis und nicht zu jedem Zweck verarbeitet werden und
- auch **nicht** einfach dauerhaft archiviert werden sondern müssen ggf. sicher gelöscht werden.

Ein noch höheres Schutzniveau gilt für die sogenannten **besonderen Kategorien personenbezogener Daten**; hierzu gehören u.a.:

- ethnische Herkunft
- politische Meinung
- religiöse/philosophische Überzeugungen
- aber auch genetische und Gesundheitsdaten

Spätestens, wenn solche Daten vorliegen oder Daten, aus denen sich solche besonders sensiblen Daten ableiten lassen, sollten Sie die ausgewiesene Rechtsexpert:innen der [Stabsstelle Datenschutz und IT-Sicherheit](https://verwaltung.uni-koeln.de/stabsstelle02.3/content/index_ger.html) hinzuziehen (dort finden Sie auch [Informationen zum Forschungsdatenschutz](https://verwaltung.uni-koeln.de/stabsstelle02.3/content/forschungsdatenschutz/index_ger.html)). Bitte beachten Sie auch das [Verzeichnis von Verarbeitungstätigkeiten (Verarbeitungsverzeichnis) der UzK](https://vvv.uni-koeln.de/) zur Dokumentation von Prozessen rund um die Verarbeitung personenbezogener Daten.

---
## Sicherer Umgang mit sensibler Daten

Insbesondere bei personenbezogenen, aber auch anderen sensiblen Daten, muss von Anfang an die (technisch) **sichere Speicherung und Übertragung** gewährleistet werden. Selbst wenn ein Speichersystem über eine Zugangskontrolle verfügt, beispielsweise durch ein Login mit Passwort, werden die Daten oft im Klartext übertragen und gespeichert. Dadurch sind u.a. folgende, die Datensicherheit kompromittierende Szenarien nicht auszuschließen:

- **Mitschneiden** der Daten im Transfer (z.B. durch einem Man-in-the-Middle-Angriff bei Nutzung eines Cloud-Speichers)
- **Auslesen** der Daten von einem Datenträger (z.B. bei Diebstahl eines Laptops)
- **Einsehen** der Daten auf einem Speichersystem (z.B. durch den Betreiber)

Die einfachste Lösung für diese Probleme ist es, die Daten zu **verschlüsseln**. Liegen die Daten im verschlüsselten Zustand vor, können Sie theoretisch weder bei der Übertragung eingesehen noch ausgelesen oder eingesehen werden – oder zumindest nicht ohne unrealistisch großen Aufwand. Selbst wenn die Übertragung kompromittiert, der Datenträger gestohlen oder ein Betreiber vertrauensunwürdig ist – Dritten liegen immer nur die verschlüsselten, nicht einsehbaren Daten vor, die ohne Schlüssel wertlos sind. Damit das in der Praxis auch funktioniert, muss aber eine adäquate Verschlüsselungslösung verwendet und das gesamte Verfahren sicher implementiert werden. Neben der eher technischen-praktischen Perspektive, auf die wir uns hier konzentrieren, bedeutet sicher aber insb. auch rechtssicher. Informationen und Beratung zu rechtlichen Aspekten erhalten Sie bei der [Stabsstelle Datenschutz und IT-Sicherheit](https://verwaltung.uni-koeln.de/stabsstelle02.3/content/index_ger.html).

Eine (vereinfachte) Analogie für Verschlüsselung ist ein konventionelles Schloss:

- Die **Verschlüsselungsstrategie** entspräche dann den Fragen, wie gut das Schloss ist, wo es eingebaut wurde und was es absichern soll (handelt es sich z.B. um ein fest verbautes Schloss einer Haustür, um ein Vorhängeschloss eines Gartentörchens oder um den Schließmechanismus eines gepanzerten Tresors).
- Der **Verschlüsselungsalgorithmus** und die Wahl des **Passwortes** sagen etwas darüber aus, wie komplex das Schloss und der dazugehörige Schlüssel sind (ist es ein einfaches Buntbartschloss und könnte mit einer Haarnadel "geknackt" werden oder ist es ein komplexeres Stiftschloss?).
- Der sichere **Umgang mit Passwörtern** schließlich entspricht der Aufbewahrung der Schlüssel zu einem konventionellen Schloss (trage ich diese an mir und sichere sie über eine Kette an meiner Kleidung oder liegt der Schlüssel "versteckt" auf dem Türrahmen der durch ihn zu sichernden Tür).

Wesentlich für eine funktionierende Verschlüsselung sind damit vor allem die folgenden Faktoren, mit denen wir uns im Folgenden beschäftigen:

- eine **Verschlüsselungsstrategie**
- ein sicherer **Verschlüsselungsalgorithmus** und die Wahl sicherer **Passwörter** und
- einen sicheren **Umgang mit Passwörtern**

---
### Verschlüsselungsstrategie

Es gibt bei Verschlüsselung unterschiedliche Vorgehensweisen:

**auf der Dateiebene**

- Verschlüsselung einzelner **Dateien** (Dateiname bei manchen Lösungen im Klartext)
- günstig für die **Synchronisation** mit Cloud-Speichern
- Vorsicht: teilweise in Bearbeitungsprogramme eingebaut (i.d.R. **nicht** empfehlenswert, oft unsicher implementiert)
- Beispiel: [Cryptomator](https://cryptomator.org/) (plattformübergreifend, [hier](https://rrzk.uni-koeln.de/informationssicherheit/it-sicherheit/verschluesselung-von-daten/verschluesselung-in-cloudspeichern) Informationen des RRZK zur Dateiverschlüsselung mit Cryptomator)

**über Container**

- verschlüsselter **Bereich** in einer Containerdatei
- die Datei wird als (virtuelles) Laufwerk in das bestehende Dateisystem eingebunden
- erfordert mehr Planung, Containergröße oft fix
- i.d.R. sicherere Lösung
- Beispiel: [VeraCrypt](https://veracrypt.fr/en/Home.html) (plattformübergreifend)

**ganze Speichermedien**

- Verschlüsselung kompletter Speichermedien wie Festplatten oder USB-Sticks (teilweise auch für Systemplatten möglich)
- Wichtig: Backup **vor** Implementierung (bestehende Daten können verlorengehen)
- im Alltag einfach zu nutzen
- nicht geeignet zur sicheren Übertragung von Daten über Netzwerke oder als eigene Verschlüsselungslösung auf Cloud-Speichern
- Beispiele:

  - [VeraCrypt](https://veracrypt.fr/en/Home.html) (plattformübergreifend, [hier](https://rrzk.uni-koeln.de/informationssicherheit/it-sicherheit/verschluesselung-von-daten/verschluessellung-mit-veracrypt) Informationen des RRZK zur Datenträgerverschlüsselung mit VeraCrypt)
  - BitLocker (Win10 integriert, [hier](https://rrzk.uni-koeln.de/informationssicherheit/it-sicherheit/verschluesselung-von-daten/verschluesselung-mit-bitlocker) Informationen des RRZK zur Datenträgerverschlüsselung mit BitLocker)
  - FileVault2 (macOS integriert)

**Spezialfall: plausible deniability**

- unsichtbarer, verschlüsselter (innerer) Container in einem verschlüsselten (äußeren) Container
- Kann sinnvoll sein in Szenarien mit hohem Risiko, in dem z.B. unter Straf- oder Gewaltandrohung die Entschlüsselung (des äußeren Containers) erzwungen wird um plausibel abstreiten zu können (plausible deniability), dass sensible Daten (im unentdeckten inneren Container) vorliegen.
- der äußere Container verhält sich wie ein konventioneller Container (s.o.), hier werden nur moderat vertrauliche Daten abgelegt
- der innere Container ist unsichtbar und enthält die eigentlich schützenswerten oder geheimen Daten
- Anwendungsfall wäre z.B. Feldforschung unter Dissidenten in einem autoritären politischen System, bei dem Gefahr besteht, dass die/der Forscher:in zur Herausgabe gezwungen wird und die Befragten gefährdet werden
- Beispiel: [VeraCrypt](https://veracrypt.fr/en/Home.html) (plattformübergreifend)

Bei jeder Verschlüsselung sollte sehr auf die Auswahl eines wirklich geeigneten Verfahrens geachtet werden. Beispielsweise haben einige klassische proprietäre Anwendungen wie MS Office Word und Excel oder auch Adobe-Produkten zur Arbeit mit pdf-Dateien Zusatzfunktionen zum Schutz auf der Dateiebene. Die sehr unterschiedliche (und teilweise hochgradig unsichere) Implementation in den einzelnen Programmversionen lassen diese für eine ernstzunehmende Verschlüsselung aber als nicht empfehlenswert erscheinen. Insgesamt sind Quelloffene Lösungen proprietären in aller Regel vorzuziehen. Informieren Sie sich bei einer vertrauenswürdigen Quelle vorab darüber, wie die Sicherheit einer Verschlüsselungslösung eingeschätzt werden kann (z.B. [hier](https://rrzk.uni-koeln.de/informationssicherheit/it-sicherheit/verschluesselung-von-daten) auf den Seiten des RRZK zu diesem Thema).

---
### Sicherer Verschlüsselungsalgorithmus und sichere Passwörter
Kommen wir zu den  nächsten beiden Faktoren, die maßgeblich für die praktische Sicherheit einer Verschlüsselung verantwortlich sind:

- die Wahl eines geeigneten **Verschlüsselungsalgorithmus**
- die Verwendung eines **sicheren Passworts**

**Verschlüsselungsalgorithmus**

Je nach Anwendungsfall und Software können eine ganze Reihe verschiedener Verschlüsselungsalgorithmen zum Einsatz kommen. Bei einer sicheren, gut implementierten Software (wie z.B. [VeraCrypt](https://veracrypt.fr/en/Home.html) oder [Cryptomator](https://cryptomator.org/)) wird in der Regel die Voreinstellung des Algorithmus einen adäquaten Sicherheitsstandard für alle hier plausiblen Szenarien mitbringen.

**Sichere Passwörter**

Die Konstruktion eines sicheren Passworts hängt insbesondere von der Komplexität und der Länge ab:

- Die **Komplexität** eines Passworts ergibt sich aus dem Raum des verwendeten Zeichensatzes (also der Anzahl möglicher verschiedener Zeichen pro verwendetem Zeichen, z.B. GROSS- und Kleinbuchstaben, Ziffern, Sonderzeichen). Die Komplexität ist unter anderem auch deshalb so wichtig, weil ein komplexeres Passwort sich schlechter erraten lässt. Erraten inkludiert hier auch, dass bei einem Wörterbuchangriff systematisch gängige Passwörter in Passwortlisten durchprobiert werden. Umso mehr verschiedene Zeichen um so willkürlicher kombiniert sind, desto sicherer ist ein Passwort bei gleichbleibender Länge (und desto unwahrscheinlicher ist es, dass es in einem Lexikon hinterlegt ist).
- Die **Länge** eines Passworts geht als Exponent in die Berechnung der Anzahl der möglichen Kombinationen ein, die bei einem Brute-Force-Angriff durchprobiert werden müssen (während der Raum der verschiedenen Zeichen als Basis eingeht). Deshalb ist die Länge ein zweites, wesentliches Sicherheitsmerkmal eines Passworts.

Das führt in der Praxis zu drei **verschiedenen Strategien**, sichere Passwörter zu generieren:

- **komplex**: Ältere und inzwischen seltener empfohlene Strategie. Fordert möglichst arbiträre Passwörter, dabei Verwendung von Großbuchstaben **und** Kleinbuchstaben **und** Ziffern **und** Sonderzeichen. Nachteil ist, dass entsprechende Passwörter sehr schlecht memoriert werden und deshalb oft auch verhältnismäßig kurz sind (i.d.R. um die 8 Zeichen). Bietet sich dennoch dann an, wenn systembedingt nur kurze Passwörter möglich sind.

  Beispiel: `i4*kP3(T`

- **lang**: Inzwischen etabliert sich der Ansatz, längere Passwörter zu generieren, die trotzdem memoriert werden können. Eine Einfache Vorgehensweise ist, möglichst arbiträr Wörter (aus einem Wörterbuch) aneinanderzuhängen. Oft werden die einzelnen Wörter durch ein Sonderzeichen getrennt und zufällig komplett groß- oder kleingeschrieben. Ein Passwort dieser Art sollte aber deutlich mehr als 8 Zeichen haben und es ist wichtig, dass die Wörter keinen Zusammenhang haben.

  Beispiel: `hardhat-SPIFFY-boatload-smug-TWINT`

- **Passphrase**: Eine Mischung aus komplex und lang, bei der das Passwort selbst aus einer gut merkbaren Passphrase abgeleitet wird. Oft sind dies die Anfangsbuchstaben aller Wörter in einem Satz, aber es sind auch komplexere Muster möglich (z.B. 1. Buchstabe des ersten Worts, 2. Buchstabe des Dritten, etc.). Zusätzliche Sicherheit besteht, wenn auch noch Satzzeichen hinzugenommen werden und eine Phrase mindestens eine Nummer enthalten soll. ABER: Vorsicht vor abgenutzten und zu kurzen Phrasen.  

  Negativbeispiel (kurz und abgenutzt): `Mtfbwy` (für: **M**ay **t**he **f**orce **b**e **w**ith **y**ou)

  Positivbeispiel: `Pctnohehacoypkatiuasp` (für: **P**lease **c**onfirm **t**hat **n**o **o**ne **h**as **e**ver **h**ad **a** **c**opy **o**f **y**our **p**rivate **k**ey **a**nd **t**hat **i**t **u**ses **a** **s**trong **p**assphrase)

Aktuelle Empfehlungen zur Erstellung sicherer Passwörter finden Sie auf den Informationsseiten des [Bundesamts für Sicherheit in der Informationstechnik](https://www.bsi.bund.de/DE/Themen/Verbraucherinnen-und-Verbraucher/Informationen-und-Empfehlungen/Cyber-Sicherheitsempfehlungen/Accountschutz/Sichere-Passwoerter-erstellen/sichere-passwoerter-erstellen_node.html).

---
### Sicherer Umgang mit Passwörtern

Die beste kryptographische Lösung mit einem sehr sicheren Passwort nützt nicht viel, wenn der Umgang mit den Passwörtern nicht sicher ist – sowohl vor Verlust als auch vor Missbrauch. Folgende Punkte sind besonders **wichtig für den sicheren Umgang** mit Passwörtern:

- Benutzen Sie für **jeden** Dienst ein **anderes** Passwort.
- Eine generelle Empfehlung zum regelmäßigen **Ändern von Passwörtern** besteht nicht mehr, aber ändern Sie Ihre Passwörter spätestens dann, wenn es zu einem sicherheitsrelevanten Vorfall kam (wenn ein Anbieter z.B. gehackt und Passwörter geleakt wurden).
- Verwenden Sie eine **Zweifaktor-Authentifizierung**, wenn es sie gibt.
- Benutzen Sie einen **Passwortmanager**.
- **Sichern Sie Ihre Passwörter** (aber bitte nicht mit einem Post-It am Monitor des zu sichernden Computers, besser ist ein Schließfach).

Ein **Passwortmanager** hilft den Überblick über die vielen Zugangsdaten der vielen verschiedenen Dienste, die oft notwendig sind, zu behalten. Im Prinzip funktioniert ein Passwortmanager wie ein verschlüsselter Container, in dem alle Zugangsdaten enthalten sind und der selbst über ein Passwort gesichert wird. Zusatzfunktionen wie Cloud-Synchronisation der verschlüsselten Zugangsdaten zwischen mehreren Geräten (nur bedingt zu empfehlen) oder Browser-Integration (um die Zugangsdaten direkt vom Passwortmanager in eine Anmeldemaske eines über einen Browser zugegriffenen Dienstes zu übertragen) existieren in vielen verschiedenen Lösungen, die derzeit auf dem Markt sind. Auch helfen die Lösungen bei der Generierung sicherer Passwörter und es kann oft zwischen verschiedenen Strategien wie Komplexität vs Länge ausgewählt werden.

**Hinweise zur Verwendung eines Passwortmanagers**

- **Hauptpasswort** für den Passwort-Manager

  - SEHR sicher (maximal komplex und lang, nicht digital speichern)
  - redundant aufbewahren (z.B. Kopie in ein Schließfach)

- (fast) alle anderen Passwörter: via Passwort-Manager
- viele Lösungen, z.B. [KeePass](https://keepass.info/) (siehe [hier](https://www.heise.de/tipps-tricks/Passwortmanager-So-verwalten-Sie-Ihre-Passwoerter-3934582.html) für eine Anleitung)

**Hinweise für verschlüsselte Container**

- Passwörter für verschlüsselte Container mit sensiblen oder hochgradig sensiblen Daten sollten ähnliche Anforderungen erfüllen wie das Haupt-Passwort für den Passwort-Manager (komplex und lang)
- i.d.R. sollten diese nicht im Passwort-Manager gespeichert werden – wird dieser kompromittiert, sind alle Container mit einem Schlag ebenfalls kompromittiert.

---
## Anonymisierung

Verschlüsselung ist ein wichtiger Bestandteil des sicheren Umgangs mit sensiblen Daten, löst aber nicht das Problem, wie diese trotzdem weitergegeben oder veröffentlicht werden können, z.B. für einen Reviewprozess oder zur Nachnutzung durch Dritte. Eine Möglichkeit trotz personenbezogener Ausgangsdaten diese weitergeben zu können ist eine **Anonymisierung** – denn anonyme Daten fallen nicht unter die DSGVO. Problematisch ist dabei allerdings sicherzustellen die Daten so zu anonymisieren, dass diese auch wirklich anonym bleiben und nicht **deanonymisiert** werden können. Gerade im Kontext von Big Data,  Data Mining und Data Linkage wird dies immer schwieriger, weil die Möglichkeiten zunächst anonym erscheinende Daten so zu kombinieren und zu analysieren, dass diese doch wieder einen Personenbezug zulassen, nicht gleich bleiben sondern zunehmen.

Dennoch ist die Anonymisierung das Mittel der Wahl, um ursprünglich aus Sicht der DSGVO geschützte Daten veröffentlichen und zur Nachnutzung zur Verfügung stellen zu können. Um eine **möglichst sichere Anomymisierung** vorzubereiten, helfen folgende Schritte:

- Überlegen Sie im Vorfeld, welche Daten im Datensatz vorhanden sind und **welche personenbezogenen Informationen sich** daraus theoretisch **ableiten lassen**.
- Lassen sich die Daten dabei mit **vertretbarem Aufwand** auf individuelle (oder sehr wenige) Personen zurückverfolgen, greift weiterhin die DSGVO.
- Überlegen Sie, welchen wissenschaftlichen Informationsverlust die **Löschung oder Aggregation** von zur Deanonymisierung nutzbarer Variablen bedeutet und wägen Sie beide gegeneinander ab. M.a.W.: Löschen/aggregieren Sie so wenig wie nötig zur Sicherstellung faktischer Anonymität, behalten Sie so viele Daten wie möglich zur Erhaltung ableitbaren Informationsgehalts der Daten.
- Prüfen Sie die Möglichkeit nur Metadaten zu veröffentlichen und einen vollständigen Datensatz entweder nur unter **Restriktionen** herauszugeben (z.B. Zugang nur nach Prüfung nur für einen eingeschränkten Nutzerkreis) oder die Analyse ohne Herausgabe der Daten auch längerfristig in einer sicheren Institution zu ermöglichen. Idealerweise wird gleichzeitig ein anonymisierter (dann aber unvollständiger) Datensatz ohne weitere Beschränkungen veröffentlicht.
- Nutzen Sie **Beratungsmöglichkeiten**, beispielsweise der [Stabsstelle Datenschutz und IT-Sicherheit](https://verwaltung.uni-koeln.de/stabsstelle02.3/content/index_ger.html).

---
# Zusammenfassung Themenblock 1: "Leitfragen Speicher"

In diesem Themenblock wurden Leitfragen zur Speicherung von Forschungsdaten behandelt um einen Überblick über die wichtigsten Themen zu liefern, die am besten schon in der Planung eines Forschungsprojektes berücksichtigt werden.  
Diese **Leitfragen** und **Themen** sind:

1. **Wie viel** Speicherplatz wird voraussichtlich benötigt? **Wie lange** wird zu welchem Zweck gespeichert?  

    Themen: heißer, warmer, kalter Speicher
2. Welche Vorsichtsmaßnahmen sollten **zum Schutz vor Datenverlust** getroffen werden?  

    Themen: Replikation, Versionierung, Backup, Archivierung
3.  **Wer** braucht **Zugang**? Gibt es **sensible** Daten und ist die **Speicherlösung hierfür geeignet**?  

    Themen: DSGVO, Verschlüsselung, Passwortmanager

Als nächsten Schritt empfehlen wir Ihnen, sich mit dem [Themenblock 2: Speicherlösungen](./0120_storage-solutions_DE.md) zu beschäftigen. Dieser liefert eine Einführung in die physischen Speicher (das "Blech"), die an der Universität zu Köln zur Verfügung stehen.

Im [Themenblock 3: Organisation Daten](./0130_organization-documentation_DE.md) gibt es außerdem Anregungen für die Organisation und Dokumentation der Daten.
