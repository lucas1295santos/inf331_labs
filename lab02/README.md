# Lab 02

## Tarefa sobre catálogo de componentes

[notebook resolvido](notebooks/components-01-catalog-resolvido.ipynb)

## Tarefa Web Components 1
~~~html
<!-- Btn mundo -->
<dcc-trigger id="btn_mundo"
             label="Mundo"
             action="noticia/mundo/politica"
             divert="divert"
             value="American Elections - new pool presents surprising results">
</dcc-trigger>
<!-- Btn Brasil P -->
<dcc-trigger id="btn_brasil_p"
             label="Brasil P"
             action="noticia/brasil/politica"
             divert="divert"
             value="Saiba tudo sobre o novo imposto">
</dcc-trigger>
<!-- Btn Brasil E -->
<dcc-trigger id="btn_brasil_e"
             label="Brasil E"
             action="noticia/brasil/esporte"
             divert="divert"
             value="Gols da décima terceira rodada do Brasileirão">
</dcc-trigger>
<!-- Btn Bahia -->
<dcc-trigger id="btn_bahia"
             label="Bahia"
             action="noticia/bahia/esporte"
             divert="divert"
             value="Vitória do Vitória na Arena Vitoriosa">
</dcc-trigger>
<!-- Character doctor -->
<dcc-lively-talk duration=3
                 delay=0
                 character="doctor"
                 speech="">
                 <subscribe-dcc topic="noticia/+/politica"></subscribe-dcc>
</dcc-lively-talk>
<!-- Character nurse -->
<dcc-lively-talk duration=0
                 delay=0
                 character="nurse"
                 speech="">
                 <subscribe-dcc topic="noticia/brasil/#"></subscribe-dcc>
</dcc-lively-talk>
<!-- Character patient -->
<dcc-lively-talk duration=0
                 delay=0
                 character="patient"
                 speech="">
                 <subscribe-dcc topic="noticia/#"></subscribe-dcc>
</dcc-lively-talk>
~~~

## Tarefa Web Components 2
~~~html
<!-- Btn next science -->
<dcc-trigger label="Next science" action="next/science">
</dcc-trigger>
<!-- Btn next design -->
<dcc-trigger label="Next design" action="next/design">
</dcc-trigger>
<!-- Rss feed science -->
<dcc-rss publish="news/science" source="https://www.wired.com/category/science/feed">
  <subscribe-dcc topic="next/science" role="step"></subscribe-dcc>
</dcc-rss>
<!-- Rss feed design -->
<dcc-rss publish="news/design" source="https://www.wired.com/category/design/feed">
    <subscribe-dcc topic="next/design" role="step"></subscribe-dcc>
</dcc-rss>
<!-- Aggregator science -->
<dcc-aggregator publish="aggregate/science" quantity="3">
  <subscribe-dcc topic="news/science"></subscribe-dcc>
</dcc-aggregator>
<!-- Character doctor -->
<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="News ">
  <subscribe-dcc topic="aggregate/science"></subscribe-dcc>
</dcc-lively-talk>
<!-- Character nurse -->
<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="nurse"
                 speech="News ">
  <subscribe-dcc topic="news/science"></subscribe-dcc>
</dcc-lively-talk>
<!-- Character patient -->
<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="patient"
                 speech="News ">
  <subscribe-dcc topic="news/design"></subscribe-dcc>
</dcc-lively-talk>
~~~