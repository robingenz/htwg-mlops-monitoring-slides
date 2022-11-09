# Monitoring

---

## Problem

<a href="https://info.algorithmia.com/hubfs/2020/Webinars/Forrester/Eight-must-haves-slides-final.pdf" target="_blank" >
    <img src="/images/problem-code-is-deterministic.png" class="mt-4 h-9/10 rounded shadow" />
</a>

<!-- 
Wenn man eine konventielle Software deployt, dann muss man sich in der Regel keine Sorgen machen, dass diese auf einmal aufhört zu funktionieren.
Natürlich werden dennoch in der Regel Updates veröffentlicht, um neue System- oder Geschäftsanforderungen zu erfüllen.
Außerdem existiert auch hier Monitoring. Aber nicht, da die Software auf einmal aufhören könnte zu funktionieren, sondern um beispielsweise die Nutzer-Anzahl oder Startzeit zu messen.
-->

---

## Problem

<a href="https://info.algorithmia.com/hubfs/2020/Webinars/Forrester/Eight-must-haves-slides-final.pdf" target="_blank" >
    <img src="/images/problem-models-performance-can-decay.png" class="mt-4 h-9/10 rounded shadow" />
</a>

<!-- 
Modelle des maschinellen Lernens verschlechtern sich mit der Zeit. Sie sind dynamisch und reagieren auf Veränderungen in der realen Welt.
Gründe dafür sind beispielsweise Veränderungen in der Umwelt oder im Verbraucherverhalten.
-->

---

## Problem

<a href="https://info.algorithmia.com/hubfs/2020/Webinars/Forrester/Eight-must-haves-slides-final.pdf" target="_blank" >
    <img src="/images/problem-models-must-be-monitored.png" class="mt-4 h-9/10 rounded shadow" />
</a>

---

<br>

> It is crucial to know not just that your ML system worked correctly at launch, but that it continues to work correctly over time.

<!-- 
Quelle: https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/aad9f93b86b7addfea4c419b9100c6cdd26cacea.pdf

**Deutsch**: Es ist von entscheidender Bedeutung, dass Ihr ML-System nicht nur beim Start korrekt funktioniert, sondern auch im Laufe der Zeit weiterhin korrekt funktioniert.
-->

<br>

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

<!-- TODO: Wie werden diese Berechnet? -> KaTeX benutzen -->

---

## Best Practices
