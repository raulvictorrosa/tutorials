<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Criar BKP por linha de comando em SSH</title>
<link rel="stylesheet" href="https://stackedit.io/res-min/themes/base.css" />
<script type="text/javascript" src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>
</head>
<body><div class="container"><h2 id="criar-bkp-por-linha-de-comando-em-ssh">Criar BKP por linha de comando em SSH</h2>

<pre class="prettyprint"><code class="language-sh hljs ruby hljs "><span class="hljs-comment"><span class="hljs-comment"># Lista arquivos da pasta onde você está</span></span>
<span class="hljs-variable"><span class="hljs-variable">$ </span></span>ls

<span class="hljs-comment"><span class="hljs-comment"># Acessa a pasta desejada</span></span>
<span class="hljs-variable"><span class="hljs-variable">$ </span></span>cd <span class="hljs-regexp">nomepasta</span>

<span class="hljs-comment"><span class="hljs-comment"># Cria o .tar para backup</span></span>
<span class="hljs-variable"><span class="hljs-variable">$ </span></span>tar <span class="hljs-string">-cvf </span><span class="hljs-regexp">nomedoarquivo</span><span class="hljs-constant">.tar </span><span class="hljs-regexp">nomedoarquivooroginal</span>

<span class="hljs-comment"><span class="hljs-comment"># Move o arquivo</span></span>
<span class="hljs-variable"><span class="hljs-variable">$ </span></span>mv <span class="hljs-regexp">nomedoarquivo</span><span class="hljs-constant">.tar </span><span class="hljs-regexp">pastadestino</span>

<span class="hljs-comment"><span class="hljs-comment"># Remove o arquivo desejado</span></span>
<span class="hljs-variable"><span class="hljs-variable">$ </span></span>rm <span class="hljs-string">-rf </span><span class="hljs-regexp">nomedoarquivo</span><span class="hljs-constant">.tar </span></code></pre></div></body>
</html>