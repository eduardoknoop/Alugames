# ***Desafio lógica de JS no Alugames***
```js
function alterarStatus(id) {
    let gameClicado = document.getElementById(`game-${id}`);
    let imagem = gameClicado.querySelector('.dashboard__item__img');
    let botao = gameClicado.querySelector('.dashboard__item__button');

    
    if  (imagem.classList.contains('dashboard__item__img--rented')) {
        imagem.classList.remove('dashboard__item__img--rented');
    } else { 
        imagem.classList.add('dashboard__item__img--rented');
    }

    if (botao.classList.contains('dashboard__item__button--return')) {
        botao.classList.remove('dashboard__item__button--return');
        botao.textContent = 'Alugar';
    } else {
        botao.classList.add('dashboard__item__button--return');
        botao.textContent = 'Devolver';
    }

}
```
Nesse jogo, nós temos que mudar a função dos botões com base no HTML. Foi bem complicado de pegar a lógica, mas depois deu pra entender legal.

Nós usamos `document.getElementById` pra resgatar um elemento lá no HTML, pra conseguirmos atribuir esse elemento à nossa variável, assim fazendo com que a gente consiga mexer com ele à vontade durante o código.

Após isso, a gente verifica com `if else` a seguinte informação: **se o jogo está alugado** (ou seja, se a imagem contém a classe `dashboard__item__img--rented`), e quando clicarmos em **devolver**, queremos que a imagem mude, deixando ela clara. Tudo isso com base no HTML.

Então a gente **remove** essa imagem escurecida com `.classList.remove()`, e automaticamente a imagem normal (que já está atribuída à variável `imagem`) vai aparecer na tela. Ou seja, **não** precisamos criar uma nova linha adicionando `.add('dashboard__item__img')`, porque a variável `imagem` já é esse elemento. Se a gente adicionasse de novo, ia estar repetindo o mesmo código e poderia dar bug. Então é sempre bom ficar ligado nisso.

A gente segue a mesma lógica pros botões. E pra **mudar o texto do botão**, é bem simples: usamos `.textContent = 'palavra que queremos mudar'`, que vai seguir a mesma lógica anterior do `if` e do `else`.

**Entretanto, eu acho que é isso.**

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
