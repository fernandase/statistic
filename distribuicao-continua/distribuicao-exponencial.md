Distribuição Exponencial \(Exp[\lambda]\)
================

### Seja X uma variável aleatória contínua, X tem uma distribuição exponencial com \(\lambda > 0\) se sua função densidade probabilidade (f.d.p) for definida como:

\[ f(x, \lambda) =  \lambda\exp^{-\lambda x}, x \geq 0 \]

## Exemplos com X \~ \(Exp[\lambda = 1]\) (default)

### Cálculo da função densidade de probabilidade no ponto x = 1, com taxa de distribuicao \(\lambda\) = 1

\[ f(x, \lambda) = f(1, 1) = ?\]

``` r
quantil = 1
```

``` r
cat('f(1, 1) = ', dexp(quantil))
```

    ## f(1, 1) =  0.3678794

### Cálculo da probabilidade (f.d.a) \(P(X \leq 1)\) = ? (área sob a curva até o valor 1)

``` r
plot(dexp, 0, 6, lwd = 2, main = expression(paste('P(X', phantom()<= 1, ')')))
polygon(x = c(0, seq(0, quantil, by = 0.05), quantil), y = c(0, dexp(seq(0, quantil, by = 0.05)), 0), col = 'SlateBlue1')
legend("topright", legend = c(expression(paste(lambda, '= 1'))), 
       lty=1, col=c('black'), lwd=2, bty="n")
```

![](distribuicao-exponencial_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

``` r
cat('P(X <= 1) = ', pexp(quantil))
```

    ## P(X <= 1) =  0.6321206

### Cálculo da probabilidade (f.d.a) \(P(X \geq 1)\) = ? (área sob a curva a partir do valor 1)

``` r
plot(dexp, 0, 6, lwd = 2, main = expression(paste('P(X', phantom()>= 1, ')')))
polygon(x = c(quantil, seq(quantil, 6, by = 0.05), 6), y = c(0, dexp(seq(quantil, 6, by = 0.05)), 0), col = 'SlateBlue1')
legend("topright", legend = c(expression(paste(lambda, '= 1'))), 
       lty=1, col=c('black'), lwd=2, bty="n")
```

![](distribuicao-exponencial_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

``` r
cat('P(X >= 1) = ', pexp(quantil, lower.tail = FALSE))
```

    ## P(X >= 1) =  0.3678794

### Cálculo da probabilidade \(P(1 \leq X \leq 3)\) = ?

``` r
plot(dexp, 0, 6, lwd = 2, main = expression(paste('P(', 1 <= X,
                       phantom()<= 3, ')')), ylab = 'dexp')
polygon(x = c(quantil, seq(quantil, 3, by = 0.05), 3), y = c(0, dexp(seq(quantil, 3, by = 0.05)), 0), col = 'SlateBlue1')
legend("topright", legend = c(expression(paste(lambda, '= 1'))), 
       lty=1, col=c('black'), lwd=2, bty="n")
```

![](distribuicao-exponencial_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

``` r
cat('P(1 <= X <= 3) = ', pexp(quantil) - pexp(3))
```

    ## P(1 <= X <= 3) =  -0.3180924

### Cálculo do quantil (x) correspondente a dada probabilidade p = 95%

\[P(X <= x) = 0.95 \\
     x = ?\]

``` r
cat('P(X <= x) = 0.95\n', 'x = ', qexp(0.95))
```

    ## P(X <= x) = 0.95
    ##  x =  2.995732

### Gera uma amostra de tamanho 100 da distribuicao exponencial

``` r
x = rexp(100)
```

``` r
hist(x, probability = TRUE, main = "Histograma com curva teórica Exp[1]", col = "SlateBlue1", xlim = lim.x, ylim = lim.y) 
curve(dexp(x), add=T, lwd = 2.5)
```

![](distribuicao-exponencial_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

``` r
hist(x, freq = F, main = "Gráfico de densidade estimada", col = "SlateBlue1", xlim = lim.x, ylim  = lim.y)
lines(density(x), lwd = 2.5)
```

![](distribuicao-exponencial_files/figure-gfm/unnamed-chunk-12-2.png)<!-- -->
