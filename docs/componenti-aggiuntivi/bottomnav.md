---
layout: docs
title: BottomNav
description: Componente di navigazione per dispositivi mobile
group: componenti-aggiuntivi
toc: true
---

BottomNav è un componente pensato per la navigazione su dispositivi mobile il cui aspetto ricalca quello di alcune popolari app.

Il componente, di altezza fissa, è ancorato la fondo della pagina e ne occupa tutta la larghezza.

<style>
  /* Style override for Documentation purposes */
  .bd-example {
    max-width: 375px;
    height: 240px;
    margin: 0 5px 20px;
    padding: 0;
    border-top-style: dashed;
    position: relative;
  }
  .bd-example  .bottom-nav {
    position: absolute;
  }
</style>

## Esempio

È composto da un tag `<nav>` con classe `.bottom-nav` e contiene un elenco con tanti elementi quanti sono i link richiesti.

Ogni link `<a>` contiene un icona con classe `.icon` e una label contenuta in uno `<span>` con classe `.bottom-nav-label`.

Il link `<a>` attivo possiede una una classe `.active`.

{% capture example %}
<nav class="bottom-nav">
  <ul>
    <li>
      <a href="#" class="active">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-comment"></use></svg>
        <span class="bottom-nav-label">messaggi</span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-camera"></use></svg>
        <span class="bottom-nav-label">immagini</span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-file"></use></svg>
        <span class="bottom-nav-label">documenti</span>
      </a>
    </li>
  </ul>
</nav>
{% endcapture %}{% include example.html content=example %}

I link occupano automaticamente tutto lo spazio disponibile. Qui di seguito un esempio con 4 link.

{% capture example %}
<nav class="bottom-nav">
  <ul>
    <li>
      <a href="#" class="active">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-comment"></use></svg>
        <span class="bottom-nav-label">messaggi</span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-camera"></use></svg>
        <span class="bottom-nav-label">immagini</span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-file"></use></svg>
        <span class="bottom-nav-label">documenti</span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-star-outline"></use></svg>
        <span class="bottom-nav-label">preferiti</span>
      </a>
    </li>
  </ul>
</nav>
{% endcapture %}{% include example.html content=example %}

### Badge

Aggiungere uno `<span>` con classe `.bottom-nav-badge` all'interno dell'icona per visualizzare dei badge con indicazioni numeriche relative, ad esempio, al numero di messaggi non letti.

{% capture callout %}
I badge sono nascosti agli screen reader. Per garantire l'accessibilità è necessario aggiungere uno `<span>` con classe `.sr-only` all'interno della label che contenga un testo esplicativo.
{% endcapture %}{% include callout.html content=callout type="accessibility" %}

{% capture example %}
<nav class="bottom-nav">
  <ul>
    <li>
      <a href="#">
        <div class="badge-wrapper"><span class="bottom-nav-badge">1</span></div>
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-comment"></use></svg>
        <span class="bottom-nav-label">messaggi<span class="sr-only"> - 1 da leggere</span></span>
      </a>
    </li>
    <li>
      <a href="#" class="active">
        <div class="badge-wrapper"><span class="bottom-nav-badge">2</span></div>
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-camera"></use></svg>
        <span class="bottom-nav-label">immagini<span class="sr-only"> - 2 da vedere</span></span>
      </a>
    </li>
    <li>
      <a href="#">
        <div class="badge-wrapper"><span class="bottom-nav-badge">88</span></div>
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-file"></use></svg>
        <span class="bottom-nav-label">documenti<span class="sr-only"> - 88 da esaminare</span></span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-star-outline"></use></svg>
        <span class="bottom-nav-label">preferiti</span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-settings"></use></svg>
        <span class="bottom-nav-label">preferenze</span>
      </a>
    </li>
  </ul>
</nav>
{% endcapture %}{% include example.html content=example %}

### Alert

Aggiungere uno `<span>` con classe `.bottom-nav-alert` all'interno dell'icona per identificare una sezione che richiede attenzione o presenta nuovi contenuti.

{% capture callout %}
Gli alert sono nascosti agli screen reader. Per garantire l'accessibilità è necessario aggiungere uno `<span>` con classe `.sr-only` all'interno della label che contenga un testo esplicativo.
{% endcapture %}{% include callout.html content=callout type="accessibility" %}

{% capture example %}
<nav class="bottom-nav">
  <ul>
    <li>
      <a href="#" class="active">
        <div class="badge-wrapper"><span class="bottom-nav-alert"></span></div>
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-comment"></use></svg>
        <span class="bottom-nav-label">messaggi<span class="sr-only"> - nuovo contenuto disponibile</span></span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-camera"></use></svg>
        <span class="bottom-nav-label">immagini</span>
      </a>
    </li>
    <li>
      <a href="#">
        <div class="badge-wrapper"><span class="bottom-nav-alert"></span></div>
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-file"></use></svg>
        <span class="bottom-nav-label">documenti<span class="sr-only"> - nuovo contenuto disponibile</span></span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-star-outline"></use></svg>
        <span class="bottom-nav-label">preferiti</span>
      </a>
    </li>
    <li>
      <a href="#">
        <svg class="icon"><use xlink:href="{{ site.baseurl }}/dist/svg/sprite.svg#it-settings"></use></svg>
        <span class="bottom-nav-label">preferenze</span>
      </a>
    </li>
  </ul>
</nav>
{% endcapture %}{% include example.html content=example %}
