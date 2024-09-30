# Bewerbung_R-Code
Eine Reihe von Skripten, die auf verschiedenen Datenverarbeitungs- und Analyseverfahren basieren, die mit dem Datensatz der Comparative Study of Electoral Systems, Module 5, durchgeführt wurden. Die durchgeführten Analysen drehen sich um ethnische und kulturelle nationale Identitätstypologien.

## File 1: Data cleaning and wrangling
Das R.Markdown-Skript transformiert den ursprünglichen CSES Module 5 Full Release-Datensatz, um seine Lesbarkeit und Nutzbarkeit zu verbessern. Zu diesem Zweck benennt es zunächst die Variablen um und kodiert fehlende Werte als solche (Abschnitt 2, Data cleaningAnschließend werden aus den verfügbaren Variablen abgeleitete Variablen erstellt, die in weiteren Analysen verwendet werden können (Abschnitt 3, Data wrangling). Schließlich wird der Datensatz mit einem anderen zusammengeführt, der die Einwanderungsrate jedes Landes enthält (Abschnitt 5, Merge additional datasets). Die abschließenden Verfahren stellen sicher, dass nur relevante Analysevariablen ausgewählt werden und ein neuer Datensatz df_nationalism gespeichert wird.

## File 2: Data analysis via single and multilevel regression
Das R.Markdown-Skript (in Arbeit) zielt darauf ab, eine Reihe von ein- und mehrstufigen Regressionsanalysen durchzuführen. Es ist Teil einer größeren laufenden Studie zur Erforschung nationaler Identitätstypologien.

Als unabhängige Variablen konzentriert es sich auf:
- Demographische Kernvariablen (Ebene-1, Individuum): Alter (agerange), Bildung (edulvl) und Quintileinkommen (quintinc).
- Einwanderungsrate (Ebene-2, Land) (immigrate).

Als abhängige Variablen werden genutzt:
- Differenz zwischen ethnischen und kulturellen Werten der nationalen Identität (eth_vs_cult).
- Gesamtwert der nationalen Identität (nationalidentity).

In einem dritten Schritt wird die Auswirkung von Einwanderung, eth_vs_cult und nationaler Identität auf die Ablehnung von Multikulturalismus getestet.

Das Skript umfasst die Durchführung erster deskriptiver Analysen und Visualisierungen zur Untersuchung der Daten.

## File 3: Factor analyses
Das R.Markdown-Skript repliziert die in der Masterarbeit „Ethnic and cultural national identity types: a longitudinal analysis“ durchgeführte Arbeit, die darauf abzielt, ethnische und kulturelle nationale Identitäten als zwei differenzierte Typologien mittels Faktorenanalyse (über CFA und SEM) zu etablieren sowie das Vorhandensein von Messungsinvarianz für eine gegebene Stichprobe verschiedener Länder zu verschiedenen Zeitpunkten mittels MG-CFA festzustellen.

In einem ersten Schritt nutzt das Forschungsdesign die kategoriale/geordnete konfirmatorische Faktorenanalyse (CFA) und die Strukturgleichungsmodellierung (SEM) für jede Gruppe (Land-Jahr).

In einem zweiten Schritt wird die kategoriale/geordnete MG-CFA verwendet, um die Messinvarianz der Methoden und Ergebnisse zu bewerten Ethnische und kulturelle nationale Identitätstypen: ein Längsschnittanalysemodell bis zur skalaren Ebene und Extraktion vergleichbarer Gruppenmittelwerte für jeden latenten Faktor, um H2 zu adressieren.

Zusätzlich beinhaltet das Skript die Analyse fehlender Werte und die Implementierung der missRanger NA-Imputationstechnik, sowie verschiedene Visualisierungen der Ergebnisse

## File 4: Shiny app
Das R.Markdown-Skript richtet eine Shiny-App zur Visualisierung von Daten aus dem CSES-Modul 5 zur nationalen Identität ein. Die App ermöglicht die Auswahl einer nationalen Identitätsvariable (z. B. Geburtsort, Sprache), eines Prädiktors (z. B. Bildung, Alter) und die Filterung nach Ländern. Die App generiert zwei Diagramme: eines mit der Häufigkeitsverteilung der ausgewählten Variable und ein weiteres, das die Auswirkung des gewählten Prädiktors auf diese Variable zeigt, mit einem Streudiagramm und einer Regressionslinie zur Veranschaulichung der Beziehung. Die App kombiniert eine interaktive Benutzeroberfläche und serverseitige Logik, um diese Visualisierungen zu erstellen.
