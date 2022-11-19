---
layout: 'cover'
class: 'text-center'
hideInToc: True
---

# Monitoring

---

# Monitoring

<!-- Frage 2: **Was bedeutet es eigentlich Modelle zu monitoren?** -->

- Erstellen und Überwachen von Metriken
    - Metriken über die Trainingsdaten (**Data Monitoring**)
    - Metriken über die Vorhersagen (**Prediction Monitoring**)
    - Metriken über die System-Performance (**System Monitoring**)

<!-- 
**Data Monitoring**: Eingabedaten (z. B. Nutzerverhalten) überwachen, um außergewöhnliche Änderungen frühzeitig festzustellen

**Prediction Monitoring**: Ausgabedaten überwachen, um außergewöhnliche Änderungen frühzeitig festzustellen (Warum wurde Vorhersage X getroffen?)

**System Monitoring**: Performance der Applikation (+ Hardware) überwachen, um außergewöhnliche Änderungen durch das Model frühzeitig festzustellen (Besonders wichtig für Anbieter wie Netflix, die Inhalte per ML On-Demand generieren)
-->

---

## Metriken

<!-- 
https://www.evidentlyai.com/blog/ml-monitoring-metrics
https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/aad9f93b86b7addfea4c419b9100c6cdd26cacea.pdf
https://martinfowler.com/articles/cd4ml.html#ModelMonitoringAndObservability
-->

- Quantitative Messwerte
- Verschiedene Arten von Metriken
    1. Verteilungsmetriken (**Distribution**)
    2. Integritätsmetriken (**Integrity**)
    3. Aktivitätsmetriken (**Activity**)
    4. Abweichungsmetriken (**Drift**)
    5. Leistungsmetriken (**Performance**)

<!-- TODO: Wie werden diese Berechnet? -> KaTeX benutzen -->

<!-- 
**Frage**: Was sind Metriken?

**Beispiel**: F1-Score
-> Maß für die Genauigkeit eines Modells, um binäre Klassifizierungssysteme zu bewerten

**Frage**: Welche Metriken gibt es?
1. Verteilungsmetriken (z. B. Durchschnittswert, Standardabweichung)
1. Integritätsmetriken (z. B. % an fehlenden Werten, % an Ausreißern)
1. Aktivitätsmetriken (z. B. Anzahl an Vorhersagen)
1. Abweichungsmetriken (z. B. Wasserstein-Metrik)
1. Leistungsmetriken (z. B. MSE, ROC, F1 Score)
-->

---

## Unstrukturierte Daten

### Beispiel: Computer Vision

<!-- https://www.arthur.ai/blog/data-drift-detection-part-ii-unstructured-data-in-nlp-and-cv -->

### Beispiel: NLP

<!-- https://www.arthur.ai/blog/data-drift-detection-part-ii-unstructured-data-in-nlp-and-cv -->

---

## Systemanforderungen

<a href="https://christophergs.com/machine%20learning/2020/03/14/how-to-monitor-machine-learning-models/" target="_blank">
    <img src="/images/monitoring-system.png" class="mt-4 h-9/10 rounded shadow" />
</a>

<!-- 
Die 3 **Schlüsselkomponenten**:
    1. Datenverarbeitung und Speicher
    2. Visualisierung
    3. Alarmierung
-->
