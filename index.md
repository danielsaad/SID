---
layout: page
title: SID
description: Sistema Inteligente de Divulgação de Informações do IFG Formosa
---

# Sobre o SID

O Sistema Inteligente de Divulgação de Informações do IFG-Formosa (SID) surgiu da
premissa de que as informações no Câmpus encontravam-se dispostas em veículos
de divulgação estáticos e enfadonhos como:

* Memorandos;
* Postagens em murais localizados no câmpus;
* Notícias no site oficial do IFG-Formosa.

De modo a disponibilizar a divulgação de informações de maneira ágil, atrativa
e interativa, o SID foi desenvolvido utilizando conceitos de
sinalização digital.


## Arquitetura

O SID é estruturado de acordo com a arquitetura de aplicação cliente-servidor.
O módulo servidor tem acesso restrito a servidores da área de Comuicação Social
do Câmpus. Este módulo permite alimentar o SID com as divulgações a serem exibidas
pelo módulo cliente.

Por sua vez, o módulo cliente requisita ao módulo servidor as informações a serem
apresentadas no painel digital e as formata de modo adequado para apresentação.


## Implantação no Câmpus Formosa

O módulo cliente não requer muito poder computacional, logo pode ser executado
em computadores com poder de processamento mais modesto. Uma alternativa
econômicamente viável para a implantação do SID no câmpus foi adotar dispositivos
Raspberry Pi para desempenhar o papel de cliente. Estes dispositivos:
* São do tamanho de um cartão de crédito;
* Possuem acesso às redes Wi-Fi do Câmpus;
* São economicamente acessíveis;
* Acomplam-se facilmente à painéis digitais;
* Consomem pouca energia elétrica;
* Possuem poder computacional razoável e processamento gráfico dedicado.

Estas características tornam a plataforma Raspberry Pi ideal para ser utilizada
na implantação do SID.

<figure>
  <img src="/SID/img/raspberry-pi.jpg" style="margin:0px auto;display:block" alt="Raspberry Pi" width="300" height="300">
  <!-- <img src="img/raspberry-pi.jpg" width="300" height="300"> -->
</figure>


## Integração com Redes Sociais

De modo a unificar os diferentes veículos de divulgação de informação no Câmpus
Formosa, o SID possui uma integração ao Facebook. Desta forma, qualquer
evento inserido no SID para divulgação também é postado em um perfil
específico do Facebook.



<!-- {% for post in paginator.posts %}
<div class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
        <h2 class="post-title">            {{ post.title }}
        </h2>
        {% if post.subtitle %}
        <h3 class="post-subtitle">
            {{ post.subtitle }}
        </h3>
        {% endif %}
    </a>
    <p class="post-meta" style="margin-bottom:5px">Posted by {{ post.author }} on {{ post.date | date: "%B %-d, %Y" }}</p>
	<div class="notepad-index-post-tags" style="">
		{% for tag in post.tags %}<a href="{{ site.baseurl }}/search/index.html#{{ tag | cgi_encode }}" title="Other posts from the {{ tag | capitalize }} tag">{{ tag | capitalize }}</a>{% unless forloop.last %}&nbsp;{% endunless %}{% endfor %}
	</div>
</div>
<hr>
{% endfor %} -->

<!-- Pager -->
<!-- {% if paginator.total_pages > 1 %}
<ul class="pager">
    {% if paginator.previous_page %}
    <li class="previous">
        <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer Posts</a>
    </li>
    {% endif %}
    {% if paginator.next_page %}
    <li class="next">
        <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older Posts &rarr;</a>
    </li>
    {% endif %}
</ul>
{% endif %}
 -->
