<!--
icon: ../resources/logos/C3RDM_EN_V3_transparent_w1156.png
-->

filename: 0120_storage-solutions_DE.md
path: ./MAIN/oneshots/
assets: ../resources/

description: module on storage-solutions especially within University of Cologne infrastructure
language: DE

---
# Einführung in den Themenblock 2: "Speicherlösungen"

In dem vorherigen [Themenblock 1: Leitfragen Speicher](./0110_storage-key-questions_DE.md) ging es darum anhand der wichtigsten, typischsten Themen Ihre Speicherbedarfe zu ermitteln.

Jetzt stellt sich die Frage, welche Möglichkeiten es gibt, diese Bedarfe auch tatsächlich technisch und organisatorisch umzusetzen. Im vorliegenden Themenblock **Speicherlösungen** erhalten Sie deshalb einen Überblick über verschiedene Formen von digitalen Speichern mit Fokus auf Angebote oder Empfehlungen der Universität zu Köln (UzK). Diese Speicherlösungen sind:

1. **Lokale** Speicher

    SSD, HHD, NAS
2. **Remote**speicher

    Sciebo, SoFS, TSM
3. **Archiv**lösungen

    TSM, Repositorien

Wenn Sie nach dem Lesen wissen, welche technische Speicherlösung für Sie geeignet sein könnte, behandelt der nachfolgende [Themenblock 3: Organisation Daten](./0130_organization-documentation_DE.md) Themen rund um die Organisation und Dokumentation der Daten.

---
# Speicherorte

Unterschiedliche Anforderungen beispielsweise an Geschwindigkeit vs. Kapazität in verschiedenen Projektphasen (vgl. [Themenblock 1: Leitfragen Speicher](./0110_storage-key-questions_DE.md)) erfordern oft unterschiedliche Speicherlösungen.

Grundsätzlich ist zwischen **lokalen** und **remote** verfügbaren Speicherressourcen zu unterscheiden. Für hochperformante Speicher in Bezug auf **Geschwindigkeit** kann z.B. Distanz durchaus eine Rolle spielen: Ein lokales System, das nicht erst über den Flaschenhals einer Schnittstelle laufen muss, kann einen schnelleren Zugriff erlauben als ein Remote-System, dass erst über eine  Netzwerkverbindung angesprochen werden muss. Auch kann je nach Aufgabe bei heißen Systemen die **Latenz** (die Reaktions- bzw. Verzögerungszeit, die durch die Netzwerkverbindung entsteht) eine Rolle spielen, weshalb sich hier keine Speicherlösungen anbieten, die weiter entfernt liegen.

Deshalb kann generell davon ausgegangen werden, dass **heißere Daten/Speicher** eher lokal sind. Je **kälter Daten** werden, desto eher bieten sich Formen von Netzwerk- oder Cloudlösungen an. Dies trifft auch auf kalte Daten zu, die archiviert werden. Für **Archivspeicher** gelten allerdings besondere Regeln, weshalb diese hier nicht einfach in die Kategorie "remote" fallen.

![Überblick über verschiedene Speicherorte in Relation zu heißem, warmem und kaltem Speicher (von links nach rechts). Heiße Speicher werden eher mit lokalen Speicherorten, warme eher mit remote-Speichern in Verbindung gebracht, überlappen sich aber und sind nicht klar zu trennen. Kalte Speicher werden Archiven zugeordnet und stehen als Speziallösung für sich.](../resources/figures/storage-hot-warm-cold_DE_0200_storage-locations_w1920.png "Speicher heiß, warm, kalt - DE - 0200 - Speicherorte, Lizenz: CC0")

Neben Fragen der Performanz in Bezug auf Geschwindigkeit oder Speicherkapazität gibt es noch weitere **Unterschiede zwischen Speicherlösungen**, die bei deren Auswahl nach Eignung zu berücksichtigen sind, z.B.:

- **Gemeinsame Nutzung/Rechteverwaltung:** Die lokale Speicherung ist in den meisten Fällen nicht ideal für die gemeinsame Nutzung von Informationen/den Fernzugriff. Zur Kollaboration eignen sich entfernte Speicherorte (sprich: Cloudlösungen) besser.
- **Speicherung sensibler/geschützter Daten:** Die Eignung eines Speichers hängt hier sehr stark von den Umständen ab.

  - Einerseits lässt sich der Zugriff auf einen **lokaler Speicher** besonders gut kontrollieren (z.B. eine verschlüsselte externe Festplatte im Safe), es kann aber auch sein, dass lokale Laufwerke überhaupt nicht zulässig sind, z.B. wenn sie sich nicht physisch innerhalb der Universität befinden (z.B. Laptop).
  - Wird eine **Remotelösung** verwendet, muss der Speicher ausreichend sicher, die anbietende Institution vertrauenswürdig und auch eine sichere Datenübertragung über Netzwerke gewährleistet sein. Viele Cloudlösungen schließen über ihre Nutzungsbedingungen das Speichern sensibler Daten kategorisch aus oder überlassen das Problem der Einhaltung gesetzlicher Vorgaben letztlich den Nutzenden. Wenn eine Nutzung überhaupt möglich ist, erfordert dies i.d.R. manuelle Verschlüsselung.

**Kurzbeschreibung lokal, remote, Archiv**

| lokal | remote | Archiv |
|-------|--------|--------|
| Lokale Speicher sind üblicherweise in Computern verbaute oder extern angeschlossene Festplatten. Es kann sich auch um den Speicher in einem Messgerät oder, gerade bei großen Speichermengen, einen lokal angeschlossenen Dateiserver wie beispielsweise ein NAS[^1] handeln (technisch gesehen als Netzwerksystem remote, aber hier Teil der lokalen Struktur). | Bei NAS-Systemen, Instituts- bzw. eigenen Projektservern oder Projektdatenbanken handelt es sich um Speicherressourcen, die in der Regel über ein Netzwerk remote angesprochen und oft mit mehreren Akteuren geteilt werden (was in der Regel Rechteverwaltung und unter Umständen auch eine Synchronisationsfunktion beinhaltet). | Für die langfristige Datenarchivierung gibt sehr verschiedene Möglichkeiten der technischen Umsetzung, die vorzugsweise an eine vertrauenswürdige Institution (wie das RRZK oder ein Repositorium[^2]) mit der notwendigen Expertise angebunden ist, um sichere Speicherlösungen auch längerfristig zur Verfügung stellen, warten und zukunftssicher weiterentwickeln zu können. |

Im Folgenden werden wir verschiedene Speicherlösungen für diese drei Kategorien nacheinander genauer betrachten.

---
[^1] NAS steht für "network attached storage" (DE: netzgebundener Speicher), im Prinzip ein spezialisierter Computer zur Verwaltung und Bereitstellung von Speicherkapazitäten über ein Netzwerk.

[^2] Ein Repositorium ist ein Dienst oder ein Ort zur Speicherung oder Ablage von Daten, im Kontext von Forschungsdaten meist ein Online-Repositorium zur Speicherung digitaler Daten. Die Speicherung erfolgt strukturiert, die Daten werden durch sogenannte Metadaten (Daten beschreibende Daten) beschrieben (z.B. Schöpfer:in, Datentyp, Erhebungsdatum usw.). Idealerweise ist die  Institution, die einen solchen Dienst anbietet, vertrauenswürdig (z.B. über Bekanntheit oder Zertifikate). Beispiel für ein (generisches) Forschungsdatenrepositorium ist [zenodo](https://zenodo.org/), ein Verzeichnis für Forschungsdatenrepositorien ist [re3data](https://www.re3data.org/). (ausführlichere Darstellung in einem gesonderten Themenblock, derzeit noch in Entwicklung, vgl. [Überblicksseite der Themenblöcke](https://www.ilias.uni-koeln.de/ilias/goto_uk_fold_4178361.html))

---
# Lokale Speicherorte

Lokaler Speicher beschreibt die Speicherlösung, die direkt in genutzte Geräte verbaut (z.B. Festplatten in Desktop-Rechnern oder Laptops) oder unmittelbar lokal angeschlossen ist (z.B. externe Festplatten). Wir betrachten hier mit NAS auch Netzwerkspeicher, wenn sie lokal in unmittelbarer Nähe des Arbeitsplatzrechners zum Einsatz kommen, auch wenn sie über ein Netzwerk angesprochen werden.

Welche Speichermedien kommen für lokale Daten in der Regel zum Einsatz und welche für die Datensicherheit relevanten Eigenschaften haben diese?

![Überblick über verschiedene Speicherorte in Relation zu heißem, warmem und kaltem Speicher (von links nach rechts). Lokaler Speicher als Speicherort ist hervorgehoben. Diesem zugeordnet werden SDD, HDD und NAS. Die Zuordnung überlappt mit dem nicht hervorgehobenem Speicherort remote.](../resources/figures/storage-hot-warm-cold_DE_0210_local-ssd-hdd-nas_w1920.png "Speicher heiß, warm, kalt - DE - 0210 - Lokal SSD HDD NAS, Lizenz: CC0")

**SSD:**

- Solid State Disk
- Festplatte ohne bewegliche Teile
- schnell, kleine Bauweise möglich
- „relativ“ teuer pro TB (2 TB derzeit typische Größe für Standardbaugrößen)
- technische Limitation der Anzahl von Speicherzyklen, spielt heute kaum noch eine Rolle in der Praxis
- insb. ältere Modelle haben deshalb Probleme mit bestimmten Verschlüsselungsverfahren
- insb. alte SSDs lassen sich nicht sicher löschen!
- insb. alte SSDs müssen ab und zu an die Stromversorgung!

**HDD:**

- Hard Disk Drive
- herkömmliche Festplatte mit beweglichen Teilen (magnetisches Speichermedium)
- deutlich langsamer als SSD, typische Bauweisen sind derzeit 2.5 (Laptop) und 3.5 (Desktop) Zoll
- relativ günstig pro TB (12 TB derzeit ca. 300 €)
- es gibt verschiedene Typen für verschiedene Nutzungsszenarien (z.B. spezielle Serverplatten)

Da bei lokalem Speicher keine Institution die Wartung Ihrer Speicherlösung in der Hand hat, sind Sie selbst dafür verantwortlich, eine Datensicherheitsstrategie umzusetzen – oft bedeutet dies, dass auf das Prinzip des **3-2-1-Backup** zurückgegriffen wird. Auch müssen Sie selbst eine Verschlüsselung umsetzen, wenn Sie mit sensiblen Daten arbeiten. Für lokalen Speicher eignet sich ggf. dabei die Verschlüsselung ganzer Speichermedien. Mehr zum Thema Backup und Verschlüsselung siehe [Themenblock 1: Leitfragen Speicher](./0110_storage-key-questions_DE.md).

Um auch im privaten Büro oder zu Hause eine komplexere Datensicherheitsstrategie aufsetzen und bei größerem Speicherbedarf entsprechende  Kapazitäten zur Verfügung stellen zu können, gehen wir schließlich noch auf NAS-Speichersysteme ein.

**NAS:**

- Network Attached Storage
- Dateiserver, d.h. vereinfacht ein Festplattensystem, das speziell darauf ausgerichtet ist Speicherkapazität im Netzwerk zur Verfügung zu stellen
- ideal als eigene Backup-Lösung im Büro oder für zu Hause (Automatisierung möglich, Backup-Monitoring, etc.)
- in einem NAS kommen in der Regel HDDs als Speichermedien zum Einsatz
- **Achtung:** NAS mit mehreren Festplatten können für verschiedene Szenarien konfiguriert werden. Konfigurationsmöglichkeiten unterscheiden sich in Bezug auf a) Kapazität (Speicherplatz), b) Performanz (Geschwindigkeit) und c) Redundanz (Datensicherheit).
Als Faustregel gilt: je sicherer, desto langsamer und desto weniger Speicher. Konfigurieren Sie ein NAS entweder als hochkapazitives oder als hochperformantes System, haben Sie in der Regel MASSIVE Einbußen in Bezug auf die Datensicherheit (keine Redundanz, möglicherweise Verlust aller Speicher bei Defekt eines Mediums bei Konfiguration auf maximale Geschwindigkeit u.ä.).

---
# Remotespeicher

Jetzt betrachten wir als Speicherorte remote-Lösungen (aka: die "Cloud"), die eher dem Kontext warmer Daten zuzuschreiben sind, aber auch bei heißen gefunden werden können.

![Überblick über verschiedene Speicherorte in Relation zu heißem, warmem und kaltem Speicher (von links nach rechts). Heiße Speicher werden eher mit lokalen Speicherorten, warme eher mit remote-Speichern in Verbindung gebracht, überlappen sich aber und sind nicht klar zu trennen. Kalte Speicher werden Archiven zugeordnet und stehen als Speziallösung für sich. Remote ist hervorgehoben.](../resources/figures/storage-hot-warm-cold_DE_0220_remote_w1920.png "Speicher heiß, warm, kalt - DE - 0220 - Remote, Lizenz: CC0")

Im Vergleich zu rein lokalen Speicherlösungen sind hier andere Nutzungsprofile möglich. Insbesondere können Daten mit Dritten zur Bearbeitung geteilt oder sogar gemeinsam mit diesen bearbeitet werden, so dass:

- Rechteverwaltung und
- Synchronisierung

eine größere Rolle spielen.

Außerdem verändern sich hierbei auch die Anforderungen in Bezug auf

- Verschlüsselung,
- sinnvolle Backup-Lösungen und
- Organisation.

Denn der Zugriff durch mehrere Personen erfordert Absprachen, gemeinsame Konventionen und Dokumentation.

---
## Remotespeicher Sciebo

Eine Remotespeicherlösung, die sich besonders für den Austausch von Daten und die Zusammenarbeit mit anderen eignet, ist die NRW-Cloud für Forschung und Lehre namens [Sciebo](https://hochschulcloud.nrw/). Die Kerneigenschaften sind::

- Replikation
- Studierende 30 GB, Angestellte 500 GB, Projekte 2 TB
- Synchronisation mehrerer Geräte
- Freigabeoptionen, Echtzeitkollaboration

**ABER**

- keine automatische Verschlüsselung (Speicherung besonderer Kategorien personenbezogener Daten ist **nicht** erlaubt)
- kein Backup
- keine dauerhafte Datenablage

![Überblick über verschiedene Speicherorte in Relation zu heißem, warmem und kaltem Speicher (von links nach rechts). Heiße Speicher werden eher mit lokalen Speicherorten, warme eher mit remote-Speichern in Verbindung gebracht, überlappen sich aber und sind nicht klar zu trennen. Kalte Speicher werden Archiven zugeordnet und stehen als Speziallösung für sich. Remote ist hervorgehoben. Dem zugeordnet und ebenfalls hervorgehoben ist die Speicherlösung Sciebo. Sciebo deckt dabei die Datensicherheitsstrategie Replikation ab.](../resources/figures/storage-hot-warm-cold_DE_0230_remote-sciebo_w1920.png "Speicher heiß, warm, kalt - DE - 0230 - Remote Sciebo, Lizenz: CC0")

**Anwendungsszenario**

Sciebo ist konzipiert als eine nicht-kommerzielle Cloud für die Wissenschaft für das Land NRW, gestützt durch 29 Hochschulen, Hauptspeicherzentrum ist die WWU Münster. Sciebo kann über ein Webinterface per Browser oder über einen Desktop-Client betrieben werden; über letzteren sind Daten verschiedener Geräte automatisch synchronisierbar.

**Freigabe und Kollaboration**

In Sciebo können Ordner und Dateien sowohl anderen Beschäftigten der UzK wie auch Externen per Freigabe zur Verfügung gestellt werden. Es ist möglich über das Webinterface in Echtzeit gemeinsam Dokumente zu bearbeiten. Die ins Webinterface integrierte App [OnlyOffice](https://rrzk.uni-koeln.de/daten-speichern-teilen/sciebo/onlyoffice) erlaubt dabei insbesondere auch Kollaboration an Microsoft Office-Dokumenten (Word, Excel, PowerPoint). Das funktioniert für Inhalte in der Praxis sehr gut, gerade bei PowerPoint ist aber Vorsicht angebracht was das Layout angeht, hier verschieben sich gerne schon mal Objekte.

**Speicherkapazität**

Studierenden stehen 30 GB, Beschäftigten 30 GB Speicherplatz zur Verfügung. Beschäftigte können diesen auf 500 GB erweitern sowie sogenannte Projektboxen für die Arbeit in Projekten oder Gruppen beantragen (diese dann mit bis zu 2 TB Kapazität).

**Zusammengefasst sind die Vor- und Nachteile von Sciebo:**

- **Vorteile**

  - gute Alternative zu kommerziellen Anbietern (u.a. weil Daten in Deutschland liegen)
  - mehr Speicher als in RRZK-eigenen SoFS
  - gut geeignet für die Zusammenarbeit (Synchronisation in Client-Software integriert, Echtzeitkollaboration über das Webinterface, einfaches Teilen von Daten mit Externen möglich)

- **Nachteile**

  - Daten liegen nicht in Köln/RRZK (sondern primär in Münster)
  - es gibt kein automatisches Backup im eigentlichen Sinne (Halter der Besitzrechte an einer Datei können diese aber innerhalb von 7 Tagen wiederherstellen)
  - Keine klar definierte Redundanz (d.h. es ist nicht ersichtlich, wie sicher die Daten systemintern repliziert werden). Damit ist nicht sichergestellt, dass ein Systemausfall bei Sciebo nicht zu permanentem Datenverlust führt. Deshalb ist es auch nicht als dauerhafte Datenablage geeignet.
  - Das Speichern von Daten, die zu den besonderen Kategorien personenbezogener Daten Dritter fallen, ist grundsätzlich nicht erlaubt! (vgl. [Sciebo Nutzungsbedingungen](https://hochschulcloud.nrw/de/nutzungsbedingungen/))
  - Kollaboratives Arbeiten im Webinterface mit OnlyOffice führt manchmal zu Fehlern im Layout von Dokumenten

---
**Links zum Dienst**

- [Allgemeine Informationen zu Sciebo](https://rrzk.uni-koeln.de/daten-speichern-teilen/sciebo)
- [Anmeldung (how-to)](https://rrzk.uni-koeln.de/daten-speichern-teilen/sciebo/registrierung)
- [Upgrade auf 500 GB (how-to, nur für Angestellte)](https://rrzk.uni-koeln.de/daten-speichern-teilen/sciebo/funktionen)
- [Projektbox (how-to, nur für Angestellte)](https://rrzk.uni-koeln.de/daten-speichern-teilen/sciebo/projektbox)
- [Sciebo Registrierung (Studierende und Angestellte)](https://sns-sp.sciebo.de/secure/de.php)

---
## Remotespeicher SoFS

SoFS (Scale-out File Server) ist eine Remotespeicherlösung für Angehörige der UzK mit folgenden Kerneigenschaften:

- RRZK, online NAS-System
- mit automatischer Replikation, Versionierung, Backup (via TSM)
- persönlich max. 10 GB, Institution 1TB+
- Versionierung älterer Dateiversionen (stündlich, täglich, wöchentlich)
- Freigabeoptionen (Gastaccounts möglich)
- Zugangswege: UKLAN/VPN/WebDAV

**ABER**

- Speicherung **UN**verschlüsselt
- direkter Zugriff auf Versionierung nur unter Windows

![Überblick über verschiedene Speicherorte in Relation zu heißem, warmem und kaltem Speicher (von links nach rechts). Heiße Speicher werden eher mit lokalen Speicherorten, warme eher mit remote-Speichern in Verbindung gebracht, überlappen sich aber und sind nicht klar zu trennen. Kalte Speicher werden Archiven zugeordnet und stehen als Speziallösung für sich. Remote ist hervorgehoben. Dem zugeordnet und ebenfalls hervorgehoben ist die Speicherlösung SoFS. Das RRZK ist als Dienstanbieter gekennzeichnet. SoFS deckt dabei die Datensicherheitsstrategie Replikation, Versionierung und Backup ab.](../resources/figures/storage-hot-warm-cold_DE_0240_remote-sofs_w1920.png "Speicher heiß, warm, kalt - DE - 0240 - Remote SoFS, Lizenz: CC0")

**Anwendungsszenario**

Der vom RRZK angebotene SoFS-Speicher ist besonders geeignet für die sichere Speicherung von Daten während Projektphasen, in denen heißer und warmer Speicher benötigt wird, sowie für den sicheren Austausch von Daten innerhalb der UzK. SoFS ist eine Remotespeicherlösung, die am einfachsten als externes Laufwerk in das jeweilige lokale Dateisystem eingebunden werden kann; der SoFS-Speicher erscheint dann als ein zusätzliches Laufwerk auf dem eigenen PC oder Laptop.

**Freigabe**

SoFS ist aufgeteilt in einen privaten und einen öffentlichen Bereich. In letzterem ist es über die Rechtevergabe möglich, Dateien oder Ordner für andere Mitglieder der UzK innerhalb von SoFS zu sperren oder freizugeben. Benutzende von außerhalb der UzK haben grundsätzlich keinen Zugang, es ist aber möglich Gastaccounts für diese zu beantragen, eine Verlängerung ist jeweils nach einem Jahr notwendig.

**Zugang und Speicherkapazität**

Der Speicher ist innerhalb des UKLAN oder über VPN bzw. WebDAV erreichbar. Er eignet sich besonders als primärer Speicherort oder als Remotelaufwerk, über das die lokalen Laufwerke synchronisiert werden können. Im Gegensatz zu Sciebo, wo die Synchronisation in die Client-Software integriert ist und automatisch erfolgt, geschieht dies bei SoFS allerdings nicht automatisiert, sondern erfordert eine gesonderte Synchronisationssoftware, die selbst angeschafft und konfiguriert werden muss. Angehörige der UzK haben automatisch mit ihrem UzK-Account Zugang zu SoFS, die Speicherkapazität beträgt 10 GB. Institutionen der UzK können einen SoFS-Bereich für Projekte beantragen und haben 1TB frei pro Kostenstelle, eine optionale Erweiterung ist kostenpflichtig. Der Speicher pro Kostenstelle kann über die Rechteverwaltung aufgeteilt werden.

**Replikation, Versionierung, Backup**

SoFS verfügt über Replikation, Versionierung und ist an die Backup-Lösung TSM (siehe unten) angeschlossen. Standardmäßig erfolgen Snapshots um 8.00, 12.00, 16.00 und 20.00 Uhr automatisch und werden am nächsten Tag wieder überschrieben bei Änderungen.  Tägliche Sicherungen erfolgen um Mitternacht und werden eine Woche aufgehoben, wöchentliche Sicherungen erfolgen um Mitternacht Sonntag auf Montag – hiervon werden insg. 30 Sicherungen vorgehalten. Bitte beachten Sie, dass ein direkter Zugriff auf die Versionierung nur über Windows möglich ist. Außerdem erfolgt eine interne Replikation (diese kann an den Bedarf angepasst werden). Es gibt also im RRZK nicht nur eine Kopie, sondern mehrere (mind. 2) Versionen, die auf unterschiedlichen Systemen verteilt gespeichert werden. SoFS wird automatisch im TSM gesichert (d.h. ein Backup liegt automatisch vor).

**Verschlüsselung und personenbezogene Daten**

Daten im SoFS werden im RRZK unverschlüsselt gespeichert. Besonders schutzbedürftige Daten (wie personenbezoene Daten) sollten deshalb grundsätzlich nicht in SoFS gespeichert werden. Ist eine solche Speicherung dennoch notwendig, ist zwingend eine  manuelle Verschlüsselung notwendig (z.B. mit [VeraCrypt](https://www.veracrypt.fr/en/Home.html)).

---
**Links zum Dienst**

- [SoFS Überblick](https://rrzk.uni-koeln.de/daten-speichern-teilen/online-speicher-sofs)
- [Info über SoFS-Versionierung](https://rrzk.uni-koeln.de/daten-speichern-teilen/online-speicher-sofs/funktionsumfang)
- [Anleitungen für Zugang (Windows)](https://rrzk.uni-koeln.de/daten-speichern-teilen/online-speicher-sofs/anleitungen/windows)
- [Zugang zur Versionierung (how-to)](https://rrzk.uni-koeln.de/daten-speichern-teilen/online-speicher-sofs/anleitungen/zugriff-auf-vorgaengerversionen)
- [SoFS Informationen für Institutionen](https://rrzk.uni-koeln.de/daten-speichern-teilen/online-speicher-sofs/sofs-fuer-einrichtungen)

---
## Remote-Backup und Archivlösung TSM

Beim TSM (Tivoli Storage Manager) handelt es sich um einen Bandroboter des RRZK, der mit Sicherung und Archivierung zwei verschiedene Funktionen abdeckt und folgende Kerneigenschaften aufweist:

- RRZK TSM
- Backup: SoFS, einige Institute, eigener PC (2 Versionen + Replikation)
- Archiv: permanent (mit Replikation)
- Zugangswege: UKLAN/VPN/WebDAV
- nicht verschlüsselt aber gesichert

**ABER**

- Beantragung, Clientinstallation und Konfiguration notwendig
- Archiv nicht durch Nutzer:in löschbar

![Überblick über verschiedene Speicherorte in Relation zu heißem, warmem und kaltem Speicher (von links nach rechts). Heiße Speicher werden eher mit lokalen Speicherorten, warme eher mit remote-Speichern in Verbindung gebracht, überlappen sich aber und sind nicht klar zu trennen. Kalte Speicher werden Archiven zugeordnet und stehen als Speziallösung für sich. Remote und Archiv sind hervorgehoben. Remote zugeordnet ist SoFS im Verbund mit der Speicherlösung TSM. Ein zweites Icon von TSM ist Archiv zugeordnet. Das RRZK ist als Dienstanbieter gekennzeichnet. TSM deckt dabei die Datensicherheitsstrategie Replikation, Versionierung, Backup und Archivierung ab.](../resources/figures/storage-hot-warm-cold_DE_0250_remote-archive-tsm_w1920.png "Speicher heiß, warm, kalt - DE - 0250 - Remote und Archiv TSM, Lizenz: CC0")

**TSM als Backuplösung**

Der TSM ist die zentrale Backuplösung des RRZK, die andere Dienste und Institutionen nutzen können. So wird z.B. SoFS automatisch im TSM gesichert und es sind auch einige Institutsserver mit dem TSM verbunden (bitte fragen Sie Ihren lokalen IT-Support).

Es können auch Daten aus Forschung und Lehre sowie dienstliche Daten auf lokalen Laufwerken des eigenen Rechners (z.B. Laptop oder Desktop) über TSM im Backup gesichert werden. Hierzu ist eine Beantragung notwendig. Das Backup erfolgt über eine Client-Software, die konfiguriert werden muss (d.h. es gibt einen gewissen Aufwand). Wenn lokale Daten ohnehin auch auf Institutsservern gespeichert werden, prüfen Sie bitte vor der Beantragung, ob der Institutsserver bereits ans TMS angeschlossen ist. Dann ist es ggf. einfacher, ein Backup hierüber vorzunehmen und es werden (in diesem Fall unnötige) Redundanzen vermieden.

Je nach Anforderungen an die Datensicherheit erlaubt der TSM verschiedene Einstellungen. Üblicherweise wird eine minimale Versionierung vorgenommen (2 Backups werden behalten), der Backup-Zyklus ist abhängig vom genutzten Dienst und den Anforderungen der Nutzer:innen, aber üblicherweise werden Daten nach 60 Tagen fallengelassen.

**TSM als Archiv**

Neben der Backup- bietet der TSM auch eine Archivfunktion. Hier bleiben die Daten erhalten, egal was mit den lokalen Originaldateien passiert. Die Idee dabei ist es, die Daten im Zustand der Archivierung möglichst lange zu speichern – dies bietet sich folglich nur für Daten an, die nicht weiter bearbeitet, sondern in einem bestimmten Zustand erhalten werden sollen. Im Archiv gespeicherte Daten können deshalb weder verändert noch manuell gelöscht  werden. Es gibt keine prinzipiellen Kapazitätsbeschränkung, aber ab spätestens 5 TB entstehen zusätzliche Kosten.

---
**Links zum Dienst**

- [TSM allgemeine Informationen](https://rrzk.uni-koeln.de/daten-speichern-teilen/backup-system-tsm)
- [TSM Registrierung](https://rrzk.uni-koeln.de/daten-speichern-teilen/backup-system-tsm/tsm-registrierung)
- [TSM Anleitung](https://rrzk.uni-koeln.de/en/daten-speichern-teilen/backup-system-tsm/tsm-anleitungen)
- [TSM Client-Software](https://rrzk.uni-koeln.de/daten-speichern-teilen/backup-system-tsm/tsm-client-software)

---
# Archivlösung

Zum Schluss werfen wir noch einen kurzen ersten Blick auf Archivlösungen.
Hier ändern sich die Anforderungen grundlegend:

- Veränderungen der Daten sind hier im Prinzip nicht mehr vorgesehen.
- Stattdessen werden Daten, die aufbereitet und bearbeitet sind,

  - sorgfältig ausgewählt,
  - möglichst langfristig und
  -  sicher gespeichert.
  - Außerdem kann die Veröffentlichung derart archivierter Daten zur Nachnutzung durch Dritte eine relevante Anforderung sein.

![Überblick über verschiedene Speicherorte in Relation zu heißem, warmem und kaltem Speicher (von links nach rechts). Heiße Speicher werden eher mit lokalen Speicherorten, warme eher mit remote-Speichern in Verbindung gebracht, überlappen sich aber und sind nicht klar zu trennen. Kalte Speicher werden Archiven zugeordnet und stehen als Speziallösung für sich. Archiv ist hervorgehoben.](../resources/figures/storage-hot-warm-cold_DE_0260_archive_w1920.png "Speicher heiß, warm, kalt - DE - 0260 - Archiv, Lizenz: CC0")

Wie wir bereits gesehen haben, ist der TSM neben seiner Backup-Funktion auch als einfaches Archiv verwendbar, um Daten sicher in einem bestimmten Zustand festzuhalten. Eine Veröffentlichung, systematische Dokumentation über Metadaten oder Bereitstellung zur Nachnutzung durch Dritte erfordert aber andere Lösungen.

---
## Archivlösung Repositorien

Repositorien und spezialisierte Archivlösungen sind ein komplexes Thema, das zunächst nur überblicksartig und etwas vereinfacht dargestellt wird (ausführlichere Darstellung in einem gesonderten Themenblock, derzeit noch in Entwicklung, vgl. [Überblicksseite der Themenblöcke](https://www.ilias.uni-koeln.de/ilias/goto_uk_fold_4178361.html)). Ein Repositorium ist i.d.R. ein nachhaltiger Dienst, der von einer vertrauenswürdigen Institution (z.B. einer Universität oder einem Forschungsdatenzentrum) zur Verfügung gestellt wird, um Forschungsdaten mittel- (max. 10 Jahre) oder langfristig (10+ Jahre) zu archivieren. Repositorien sind entweder generisch, disziplinspezifisch oder institutionell organisiert. Neben den Daten selbst ist die Dokumentation der Daten (über sogenannte Metadaten) ein wesentlicher Bestandteil der Archivierung. Eine erste Anlaufstelle für die Suche nach einem geeigneten Repositorium für Ihre Daten oder nach Repositorien, in denen Sie für die eigene Forschung nachnutzbare Daten finden können ist z.B. [re3data.org](https://www.re3data.org/).

![Überblick über verschiedene Speicherorte in Relation zu heißem, warmem und kaltem Speicher (von links nach rechts). Heiße Speicher werden eher mit lokalen Speicherorten, warme eher mit remote-Speichern in Verbindung gebracht, überlappen sich aber und sind nicht klar zu trennen. Kalte Speicher werden Archiven zugeordnet und stehen als Speziallösung für sich. Archiv ist hervorgehoben. Dem zugeordnet und ebenfalls hervorgehoben sind Repositorien. Repositorien decken dabei die Datensicherheitsstrategie Archivierung ab.](../resources/figures/storage-hot-warm-cold_DE_0270_archive-repository_w1920.png "Speicher heiß, warm, kalt - DE - 0270 - Archiv Repositorium, Lizenz: CC0")

**Nachnutzung und Metadaten**

Oft ist das Ziel der Datenübergabe an ein Repositorium nicht nur die sichere Archivierung der Forschungsdaten und Metadaten, sondern auch deren Auffindbar- und Verfügbarmachung zur Nachnutzung durch Dritte.
Wenn Daten nicht oder nur eingeschränkt (z.B. mit zeitlichem Embargo) von Dritten genutzt werden dürfen oder nach einer bestimmten Zeit gelöscht werden müssen (z.B. aufgrund der DSGVO), kann der Zugriff auf die Daten selbst eingeschränkt werden oder die Daten können gelöscht werden. Eine Beschreibung der Daten durch Metadaten und damit der Nachweis über deren Existenz wird hingegen dauerhaft aufbewahrt. Dadurch bleiben auch dann Informationen über ein Projekt und die zugrundeliegenden Daten erhalten, wenn die Daten selbst noch nicht oder nicht mehr zur Verfügung gestellt werden können.

**Repositorien an der UzK**

An der UzK befindet sich ein Forschungsdatenspeicher (RDS) im Aufbau (Basis ist ein Objektspeicher), für den die Aufnahme des Regelbetriebs für Mitte 2022 erwartet wird. Dieser eignet sich zur Umsetzung von institutionellen Repositoriumslösungen. Die Implementierung solcher Repositoriumslösungen ist derzeit in Arbeit.

---
# Speicherorte dos and don'ts

Wir lassen die verschiedenen vorgestellten Speicherlösungen noch einmal Revue passieren und gehen dabei auch auf nicht empfohlene Varianten ein:

![Überblick über verschiedene lokale, Remote- und Archivspeicher, aufgeteilt nach do (empfohlene Lösung) in grün und don't (nicht empfohlene Lösung) in rot. In grün Empfehlungen von links nach rechts von lokalem über remote zu Archiv sind: SSD, HDD, NAS, Sciebo, SoFS, TSM, Repositorien. In rot (nicht empfohlene Lösungen) von links nach rechts von lokalem über remote zu Archiv sind: Laptop, Messgerät, Sharehoster, Dropbox, USB-Stick, externe HD.](../resources/figures/storage-hot-warm-cold_DE_0280_do-dont_w1920.png "Speicher heiß, warm, kalt - DE - 0280 - dos and don'ts, Lizenz: CC0")

**Lokal**

- **Empfohlen** sind lokale Speicher in Form von Festplatten (SSD, HDD) in z.B. Desktops oder Laptops, wenn sie in eine Datensicherheitsstrategie eingebunden sind. Die Minimallösung ist ein 3-2-1-Backup (siehe [Themenblock 1: Leitfragen Speicher](./0110_storage-key-questions_DE.md)). Ein NAS ist eine Möglichkeit zumindest Teile einer Datensicherheitsstrategie (insb. Backup und Replikation) auch mit eigenen Mitteln umsetzen zu können.
- **NICHT empfohlen** ist hingegen, Daten nur an einer Stelle zu speichern. Besonders riskant ist es, wenn dieser Speicher konstruktions- oder zweckbedingt gefährdet ist (z.B. auf einem Laptop, der gestohlen werden kann oder auf einem Messgerät, wo die Daten von anderen Nutzer:innen überschrieben werden können).

**Remote**

- **Empfohlen** werden Sciebo, insbesondere für die Zusammenarbeit mit Dritten und das Teilen von Daten im Projektverlauf, und SoFS als sicherer institutioneller Datenspeicher, der im Zusammenspiel mit TSM über eine vollständige Datensicherheitsstrategie verfügt.
- **NICHT empfohlen** ist die Nutzung von Sharehostern (auch One-Click-Hoster) zum Teilen von Dateien, es sein denn, es handelt sich um spezielle Angebote für den akademischen Bereich. Sobald die Daten auch nur ansatzweise personenbezogene oder in irgendeiner Form sensible Informationen enthalten könnten, sind diese Anbieter in aller Regel nicht ausreichend vertrauenswürdig. Aus Sicht des Datenschutzes ebenfalls problematisch sind proprietäre Clouddienste wie Dropbox. Hier kann grundsätzlich die Frage gestellt werden, wie vertrauenswürdig die Anbieter sind und ob z.B. bei der Übernahme eines Dienstes durch einen anderen Anbieter die Sicherheit der Daten kompromittiert wird.

**Archiv**

- **Empfohlen** wird der TSM des RRZK, wenn es weniger um Metadatenbeschreibungen und Teilen/Nachnutzung geht, sondern um ein sicheres, institutionellen Archiv für ausgewählte Daten, die sicher aufbewahrt werden sollen – auch während eines Projektes. In den meisten Anwendungsfällen, in denen Daten – oder zumindest die Metadaten – nach einem Projekt sicher gespeichert und ggf. auch geteilt werden sollen, sind Repositorien vertrauenswürdiger Institutionen sinnvoll.
- **NICHT empfohlen** ist es Daten am Ende eines Projekts auf mobilen Datenträgern gleich welcher Art abzulegen und zu hoffen, dass diese damit sicher aufbewahrt sind. Es gibt hier mehrere typische Probleme, warum eine solche Strategie in der Regel nicht greift:

  - Datenträger veralten z.T. schnell (und können z.B. nicht mehr angeschlossen werden, weil die Schnittstelle obsolet ist).
  - Es gibt kein Verfahren die Integrität der Daten sicherzustellen (z.B. wenn keine Bitstream Preservation erfolgt und Lesefehler auf nicht gewarteten Datenträgern die Daten im Laufe der Zeit vernichten).
  - Oft wird schlichtweg vergessen, ob und wo die Daten gespeichert wurden, schlimmstenfalls findet irgendwann irgendwer hochsensible Daten auf einer alten externen Festplatte in einem Rollcontainer oder einem verlorenen USB-Stick.

---
# Überblick Speicherlösungen RRZK

Neben den hier vorgestellten Speicherlösungen, die entweder vom RRZK empfohlen oder direkt zur Verfügung gestellt werden, gibt es auch noch eine ganze Reihe weiterer Speicherlösungen am RRZK. Einen Überblick über aktuelle Lösungen finden Sie [hier](https://rrzk.uni-koeln.de/daten-speichern-teilen). Außerdem führt das RRZK Informationsseiten mit den aktuell gültigen Informationen zu den vorgestellten Speicherdiensten, u.a. auch mit Informationen zu Bereitstellung, Links zu Nutzungsanträgen oder Anleitungen:

- [Sciebo Cloud](https://rrzk.uni-koeln.de/daten-speichern-teilen/sciebo)
- [SoFS Speicher](https://rrzk.uni-koeln.de/daten-speichern-teilen/online-speicher-sofs)
- [Antrag auf Nutzung des Tivoli Storage Manager (TSM)](https://rrzk.uni-koeln.de/daten-speichern-teilen/backup-system-tsm/tsm-registrierung)

---
# FYI: Medizinische Fakultät

Sollten Sie an der Medizinischen Fakultät angesiedelt sein, gibt es ggf. ein paar Besonderheiten zu beachten:

- Das P- (Patienten-) bzw. W- (oder Wissenschafts-) Netz der Medizinischen Fakultät ist durch eine Firewall vom UKLAN (Netzwerk der UzK) getrennt.
- Die Nutzung der RRZK-Dienste ist grundsätzlich möglich.
- ABER: Die Dienste sind nicht immer von allen Gebäuden/allen Anschlüssen aus erreichbar.

Sollten Sie Probleme bei der Nutzung eines bestimmten Dienstes haben, wenden Sie sich bitte an:  
Stefan Schwenke (IT-Koordinator Medizinische Fakultät)  
0221-478-30624  
[stefan.schwenke@uk-koeln.de](mailto:stefan.schwenke@uk-koeln.de)

---
# Zusammenfassung Themenblock 2: "Speicherlösungen"

In diesem Themenblock wurden unterschiedliche an der UzK zur Verfügung stehende oder empfohlene "Speicherlösungen" behandelt um einen Überblick zu geben über die Möglichkeiten, Ihre Speicherbedarfe technisch umzusetzen. Diese Speicherlösungen sind:

1. **Lokale** Speicher

    SSD, HHD, NAS
2. **Remote**speicher

    Sciebo, SoFS, TSM
3. **Archiv**lösungen

    TSM, Repositorien

Als nächsten Schritt empfehlen wir Ihnen den [Themenblock 3: Organisation Daten](./0130_organization-documentation_DE.md), in dem Anregungen für die Organisation und Dokumentation von Daten gegeben werden.

Wenn Sie noch offene Fragen dazu haben, was eigentlich überhaupt Ihre Speicherbedarfe sind, möchten wir Sie anregen sich (noch) einmal den vorangegangenen [Themenblock 1: Leitfragen Speicher](./0110_storage-key-questions_DE.md) anzusehen.
