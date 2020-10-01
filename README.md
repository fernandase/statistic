<img src="https://www.r-project.org/logo/Rlogo.svg" style="float:left; margin:10px 20px; display:inline-block" width="120" height="120"/>

<img src="https://d33wubrfki0l68.cloudfront.net/0ab849ed51b0b866ef6895c253d3899f4926d397/85aff/wp-content/uploads/2014/04/ggplot2.png" style="float:left; margin:10px 20px display:inline-block" width="110" height="120"/>

Repositório de aplicação estátistica inferencial em R com modelos
probabilísticos discretos e contínuos. Para cada tipo de modelo
probabilístico (discreto, contínuo) tem-se:

-   Um diretório denominado **distribuicao- + \[continua\] ou
    \[discreta\]**. Cada diretório possui:

-   Um arquivo denominado **probabilidade- + \[continua\] ou
    \[discreta\]** com o plot de cada distribuição com diferentes
    valores de parâmetro utilizando a função **plot** e o pacote
    **ggplot2**;

-   Um arquivo **Markdown** de cada distribuição de probabilidade
    denominado **distribuicao- +\[nome\_da\_distribuição\]** com o
    histograma com a curva teórica de cada distribuição, gráfico de
    densidade estimada e o uso das quatro funções de distribuição do R:

    -   Função densidade de probabilidade (f.d.p) \[contínua\] ou função
        probabilidade \[discreta\]: prefixo **d +
        \[nome\_da\_distribuição\]**;
    -   Função distribuição acumulada (f.d.a): prefixo **p +
        \[nome\_da\_distribuição\]**;
    -   Quantil correspondente a dada probabilidade: **q +
        \[nome\_da\_distribuição\]**;  
    -   Gerador aleatório de uma amostra da distribuição: **r +
        \[nome\_da\_distribuição\]**;

-   Um arquivo **.pdf** com exercícios resolvidos em R de questões
    retiradas do portal [PortalAction](http://www.portalaction.com.br/)
    e do livro [Estatística Aplicada
    (inferência)](https://www.academia.edu/37027227/Livro_pdf_Estat%C3%ADstica_aplicada_infer%C3%AAncia_Prof_MSc_Uanderson_Rebula).

<img src="https://d33wubrfki0l68.cloudfront.net/d99b4c92f610627d61009f09c5db0f7f806fbec3/648bb/wp-content/uploads/2014/04/rmarkdown.png" style="float:left; margin:10px 20px" width="110" height="120"/>

Todos os arquivos foram gerados no R Markdown.

<!--
<img src="https://d33wubrfki0l68.cloudfront.net/0ab849ed51b0b866ef6895c253d3899f4926d397/85aff/wp-content/uploads/2014/04/ggplot2.png" style="float:left; margin:10px 20px" width="120" height="120"/>
-->
