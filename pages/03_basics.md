---
layout: 'cover'
class: 'text-center'
---

# Monitoring

---

## Monitoring

<!-- Frage 2: **Was bedeutet es eigentlich Modelle zu monitoren?** -->

- Erstellen und Überwachen von Metriken
    - Metriken über die Eingabedaten (**Data Monitoring**)
    - Metriken über die Ausgabedaten (**Prediction Monitoring**)
    - <span class="opacity-60">Metriken über die System-Performance (**System Monitoring**)</span>

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
    1. Verteilungsmetriken (**Distribution**) <div class="inline-block h-3 w-3 rounded-full bg-sky-800"></div> <div class="inline-block h-3 w-3 rounded-full bg-red-700"></div>
    2. Integritätsmetriken (**Integrity**) <div class="inline-block h-3 w-3 rounded-full bg-sky-800"></div>
    3. Aktivitätsmetriken (**Activity**) 
    4. Abweichungsmetriken (**Drift**) <div class="inline-block h-3 w-3 rounded-full bg-sky-800"></div> <div class="inline-block h-3 w-3 rounded-full bg-red-700"></div>
    5. Leistungsmetriken (**Performance**) <div class="inline-block h-3 w-3 rounded-full bg-red-700"></div>

<br>
<hr>
<br>

<div class="inline-block h-3 w-3 rounded-full bg-sky-800"></div> Data Monitoring<br><br>
<div class="inline-block h-3 w-3 rounded-full bg-red-700"></div> Prediction Monitoring<br><br>
<!-- <div class="inline-block h-3 w-3 rounded-full border-solid border-2 border-black"></div>  -->

<!-- TODO: Wie werden diese Berechnet? -> KaTeX benutzen -->

<!-- 
**Frage**: Was sind Metriken?

**Beispiel**: F1-Score
-> Maß für die Genauigkeit eines Modells, um binäre Klassifizierungssysteme zu bewerten
-->

---

### Verteilungsmetriken

<table>
    <tr>
        <th>Metrik</th>
        <th>Kategorisch</th>
        <th>Numerisch</th>
        <th>Boolean</th>
    </tr>
    <tr>
        <td>Anzahl einzigartiger Werte</td>
        <td>x</td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>Durchschnittswert</td>
        <td></td>
        <td>x</td>
        <td></td>
    </tr>
    <tr>
        <td>Verhältnis</td>
        <td></td>
        <td></td>
        <td>x</td>
    </tr>
</table>

<br>

**Beispiele**:
- <u>Durchschnittswert</u> berechnen: $\bar{x}=\frac{1}{n}\sum_{i=1}^n x_i$

---

### Integritätsmetriken

<table>
    <tr>
        <th>Metrik</th>
        <th>Kategorisch</th>
        <th>Numerisch</th>
        <th>Boolean</th>
    </tr>
    <tr>
        <td>% an fehlenden Werten</td>
        <td>x</td>
        <td>x</td>
        <td>x</td>
    </tr>
    <tr>
        <td>% an Ausreißern</td>
        <td></td>
        <td>x</td>
        <td></td>
    </tr>
</table>

<br>

**Beispiele**:
- <u>% an fehlenden Werten</u> berechnen: 
    - $IQR=Q3-Q1$
    - $g_o=Q3+1,5*IQR$
    - $g_u=Q1+1,5*IQR$

---

### Aktivitätsmetriken

<table>
    <tr>
        <th>Metrik</th>
        <th>Kategorisch</th>
        <th>Numerisch</th>
        <th>Boolean</th>
    </tr>
    <tr>
        <td>Anzahl an Vorhersagen</td>
        <td>x</td>
        <td>x</td>
        <td>x</td>
    </tr>
</table>

---

### Abweichungsmetriken

<table>
    <tr>
        <th>Metrik</th>
        <th>Kategorisch</th>
        <th>Numerisch</th>
        <th>Boolean</th>
    </tr>
    <tr>
        <td>Chi-Quadrat-Test</td>
        <td>x</td>
        <td></td>
        <td>x</td>
    </tr>
    <tr>
        <td>Wasserstein-Metrik</td>
        <td></td>
        <td>x</td>
        <td></td>
    </tr>
</table>

<br>

**Beispiele**:
- <u>Chi-Quadrat-Test</u> berechnen: $dist(P,Q)=\frac{1}{2}\sum_i\frac{(P(i)-Q(i))^2}{P(i)+Q(i)}$

<!-- 
P = Feature-Werte von Datum 1
Q = Feature-Werte von Datum 2
 -->
 
---

### Leistungsmetriken

<table>
    <tr>
        <th>Metrik</th>
        <th>Kategorisch</th>
        <th>Numerisch</th>
        <th>Boolean</th>
    </tr>
    <tr>
        <td>F1 Score</td>
        <td>x</td>
        <td></td>
        <td>x</td>
    </tr>
    <tr>
        <td>MSE</td>
        <td></td>
        <td>x</td>
        <td></td>
    </tr>
</table>

<br>

**Beispiele**:
- <u>MSE</u> berechnen: $l=\frac{1}{n}*\displaystyle\sum_{i=1}^{n} (\hat{y_i} - y_i)^2$

<!-- 
**F1-Score**: Kombiniert Genauigkeit und Trefferquote.

**MSE**: Mittlere quadratische Abweichung
->  Gibt an wie sehr ein Punktschätzer um den zu schätzenden Wert streut
-->

---
layout: two-cols
---

## Unstrukturierte Daten

<!-- https://www.arthur.ai/blog/data-drift-detection-part-ii-unstructured-data-in-nlp-and-cv -->

- **Problem**: Verwendung der üblichen Metriken auf Rohdaten nicht möglich
- Viele verschiedene Ansätze
- 3 Hauptaspekte:
    1. **Vektorielle Repräsentation**: Konvertierung der unstrukturierten Daten in eine Vektoreinbettung
    2. **Dichtemodell**: Definition eines Dichtemodell für den Referenzdatensatz
    3. **Scoring**: Scoring neuer Datenpunkte anhand des Referenz-Dichtmodells

<!-- 
**Vektorielle Repräsentation**:
    - Umwandlung unstrukturierter Daten in eine aussagekräftige Vektordarstellung mittels Merkmalsextraktion (siehe **PCA**)
    - Beispiele für Vektoren bei Bildern (CV): Lichteinfall, Ausleuchtung des Hintergrunds
    - Beispiele für Vektoren bei Texten (NLP): 
**Dichtemodell**: 
    - Erstellung eines Dichtemodells, das die zugrunde liegende Verteilung modellieren kann
**Scoring**: 
    - 
-->

::right::

<img src="/images/pca_iris.png" class="mt-4 h-6/10 rounded shadow float-right" />

--- 

<img src="/images/pca_eigenfaces.png" class="mt-4 h-8/10 rounded shadow" />

---

<img src="/images/pca_imdb.png" class="mt-4 h-8/10 rounded shadow" />

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
