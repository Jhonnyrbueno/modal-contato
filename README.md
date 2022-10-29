# Modal Contato
 O modal contato criado para a utilização do submit, sem a necessidade de um back-end com o <a href="https://formsubmit.co" alt="Formsubmit">FormSubmit</a>, acesse a página do modal para ver na prática como o funciona <a href="https://jhonnyrbueno.github.io/modal-contato/" alt="Modal Contato">Modal Contato</a>

 ## Ensirindo o modal HTML no body

Insira o código abaixo do body, para incerir o modal

 ```

<div id="modal" class="hide">
    <div class="modal">
        <div class="modal-header">
            <h1>Contato</h1>
        </div>
    </div>
</div>


```

## Para estilização do modal

```
.modal {
    width: 50%;
    display: flex;
    height: 35rem;
    flex-direction: column;
    margin-left: 2%;
}

```

### Configurando o Fade atras do modal

configurando o feito de fundo atras do modal

```

#fade {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.6);
    z-index: 5;
}

```

 ## Configurando o Formsubmit

crie uma uma nova div com classe, dentro do corpo do modal e adicione o código.

```

 <form action="https://formsubmit.co/your@email.com  ou  https://formsubmit.co/random-like-string (chave que recebe no email, para ativar o formsubit, subistituindo o email)" method="POST">
     <input type="text" name="name" required>
     <input type="email" name="email" required>
     <button type="submit">Send</button>
 </form>

```
Pode ser adicionados mais três atributos abaixo do forms ID

Para um outra página de agradecimento

````

<input type="hidden" name="_next" value=" URL DA PAGINA DE AGRADECIMENTO AQUI ">

````
Com um titulo definido quando chega um email

````

<input type="hidden" name="_subject" value=" TITULO AQUI ">

````
Três formas de templete com value= box, table ou classic

````

<input type="hidden" name="_template" value=" BOX, TABLE OU CLASSIC ">


````

## Configurando o reCaptcha em uma nova janla no estilo Pop-up

No form deve se colocar atributos, que farão esta operão de pop-up

````

<form action="https://formsubmit.co/your@email.com" method="POST">

````

Dentro do forms colocar um target e rel

````

target="print_popup"
rel="noopener noreferrer"

````

agora deve incluir uma ação de onclick

````

onsubmit="window.open('about:_blank','print_popup','scrollbar=no,width=450,height=650,top=150,left=200,resizable=no,location=no,directories=no,menubar=no,toolbar=no,status=no');"

````

## Fechamento automático após o reCaptcha

Após o reCaptcha pode esta colocando um botão na pagina de agradecimento para fechar ou voltar a página inicial, porem o usar o método de fechr aumático facilita até mesmo ao usuário. Lembrando que o .js deve ser usado em outro documento HTML acima do head para finação do submit.

````

    <script>
        setTimeout(function() {
      window.close()
         }, 500);
    </script>

````

###
        Jhonny Bueno Soluções e Desenvolvimentos
          Todos os direitos reservados © 2022

