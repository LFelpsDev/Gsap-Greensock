## Por que usar o Greensock ?

- Super Performance
- Compatível com todos os browser (ate o IE8)
- Pode animar qualquer coisa (CSS, SVG, Canvas, etc)
- Total Controle (pause, avance, reverta, aumente/diminua a velocidade)
- API intuitiva e fácil de aprender

### Utilizando o BrowserAsync

ele serve para criar um servidor estático, esse servidor vai permitir que conseguimos fazer um live reload

## Modulo de Basics

Método set(), ele serve para determinar quais são as propriedades do elemento assim que pagina carrega, ou seja ele não vai servir para fazer animação nenhuma

Exemplo:

```jsx
<h1 class="titulo">Titulo</h1>

<div class="box">
	<h3>Tarefas</h3>
	<img src="url" />
</div>

const titulo = document.querySelectorAll(".titulo")

gsap.set(titulo, {
	x: 100, // ira se mover 100px para a direita, se receber valor negativo ira para esquerda
  y: 100, // ira se mover 100px para baixo, se receber valor negativo ira mover para cima
  opacity: 0.4, // altera a opacidade
	color: "#123456",
})
```

Método to(), ele vai dar inicio nas animação determina o estado que  queremos que vai para o final, ele recebe 3 Parâmetros, o primeiro é o elemento que desejo animar, o segundo o time do animação, e o terceiro as propriedades de modificação 

Exemplo

```jsx
gsap.to(titulo, 2, {
      x: 200
})

gsap.to(items, 5, {
  rotation: 360, // para fazer a rotação em 360 grau
  x: 200,
	scale: 0 // ele sumira diminuindo a escala
 })
```

Método from( ), ele é bem parecido com o to( ), porem ele é ao contrario em quando o to( ) ele vai para, from() ele vem de la e volta para o formado inicial.

```jsx
gsap.from(items, 4, {
		x: -400,
    opacity: 0,
    scale: 0.2
})
```

Método fromTo(), é junção do from() e to()

Exemplo: 

```jsx
// gsap.to(items, 2, {
//     x: 200
// })

// gsap.from(items, 5, {
//     x: -200
// })

gsap.fromTo(items, 5, {
      x: -200 // from
 }, {
	   x: 200 // to
 })
```
