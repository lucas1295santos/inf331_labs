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
> Escreva aqui o código da sua composição de componentes Web, seguindo a mesma abordagem da tarefa anterior.