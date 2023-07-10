# Trabalhando com grade do Bootstrap

## Instruções

### Introdução

Neste exercício, você praticará a criação de uma página da Web usando a Grade de Bootstrap.

### Objetivo

Crie um menu de comida de duas colunas para o Little Lemon.

### Objetivos

- Configure o contêiner Bootstrap.
- Exiba o logotipo Little Lemon no centro superior da página da Web usando o Bootstrap.
- Exiba o menu de alimentos em duas colunas usando o Bootstrap Grid.

## Instruções

1. Abra o arquivo `índice.html`.

2. Adicione um elemento `div` dentro do elemento `body`. Essa `div` será o contêiner do Bootstrap. 

    ```html
    <body>
        <div class="container">
        </div>
    </body>
    ```

3. Adicione o atributo de classe a esse elemento com o valor `container`.

    ```html
    <body>
        <div class="container">
        </div>
    </body>
    ```

4. Adicione três elementos `div` ao elemento de contêiner Bootstrap. Cada um desses elementos `div` será uma linha Bootstrap. Adicione o atributo de classe a esses elementos com o valor `row`.

    ```html
    <body>
        <div class="container">
            <div class="row">
            </div>
            <div class="row">
            </div>
            <div class="row">
            </div>
        </div>
    </body>
    ```

5. A primeira linha conterá o logotipo do Limãozinho. Adicione um elemento `div` à primeira linha.

6. Adicione o atributo de classe a esse elemento com o valor `col-12`. Isso ocupará 12 espaços de coluna.

    ```html
    <body>
        <div class="container">
            <div class="row">
                <div class="col-12">
                </div>
            </div>
            <div class="row">
            </div>
            <div class="row">
            </div>
        </div>
    </body>
    ```

7. Adicione outro elemento `div` ao elemento `col-12`. 

8. Adicione o atributo de classe a esse elemento com o valor `text-center`. Isso permitirá que você centralize o logotipo.

    ```html
    <body>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="text-center">
                    </div>
                </div>
            </div>
            <div class="row">
            </div>
            <div class="row">
            </div>
        </div>
    </body>
    ```

9. Adicione um elemento `img` no elemento `text-center` com a classe `img-fluid` aplicada a ele.

    ```html
    <body>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="text-center">
                        <img src="logo.png" class="img-fluid">
                    </div>
                </div>
            </div>
            <div class="row">
            </div>
            <div class="row">
            </div>
        </div>
    </body>
    ```

10. Na segunda linha, adicione outro elemento `div` com a classe `col-12`.

    ```html
    <body>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="text-center">
                        <img src="logo.png" class="img-fluid">
                    </div>
                </div>
            </div>
            <div class="row">
            </div>
            <div class="row">
            </div>
        </div>
    </body>
    ```

11. Adicione um elemento `div` à coluna e aplique a classe `text-center`.

    ```html
    <body>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="text-center">
                        <img src="logo.png" class="img-fluid">
                    </div>
                </div>
            </div>
            <div class="row">
            </div>
            <div class="row">
            </div>
        </div>
    </body>
    ```

12. Dentro do elemento, adicione um elemento `h1` com o texto "Nosso Menu".

    ```html
    <body>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="text-center">
                        <img src="logo.png" class="img-fluid">
                    </div>
                </div>
            </div>
            <div class="row">
            </div>
            <div class="row">
            </div>
        </div>
    </body>
    ```

13. Adicione dois elementos `div` na linha final. 

14. Adicione um atributo de classe a cada elemento com o valor `col-12 col-lg-6`.

    ```html
    <body>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="text-center">
                        <img src="logo.png" class="img-fluid">
                    </div>
                </div>
            </div>
            <div class="row">
            </div>
            <div class="row">
            </div>
        </div>
    </body>
    ```

15. Adicione os seguintes elementos no primeiro elemento `col-12 col-lg-6`:

    - Um elemento `h2` contendo o texto "Falafel".
    - Um elemento de parágrafo contendo o texto "Grão de bico, ervas, especiarias".
    - Um elemento `h2` contendo o texto "Fried Calamari".
    - Um elemento de parágrafo contendo o texto "Lula, leitelho".

16. Adicione os seguintes elementos no segundo elemento `col-12 col-lg-6`:

    - Um elemento `h2` contendo o texto "Salada de Massa".
    - Um elemento de parágrafo contendo o texto "Alface, legumes, mussarela".
    - Um elemento `h2` contendo o texto "Salada Grega".
    - Um elemento de parágrafo contendo o texto "Pepinos, cebola, queijo feta".

17. Salve o arquivo.

18. Clique em 'Go live', que está no canto inferior direito do seu editor.

19. Quando o servidor estiver em funcionamento, você verá a porta exposta.

20. Agora clique em "pré-visualização do navegador" e digite a URL como `http://localhost:<porta exposta>`.

21. Selecione a barra de ferramentas do dispositivo e escolha "Macbook 15" como o dispositivo.

22. Verifique se a página da Web exibe o menu "Little Lemon" em duas colunas. Sua página da Web deve ser semelhante à captura de tela fornecida.

23. Certifique-se de fechar o servidor clicando no número da porta exposta (por exemplo, 5500) depois de concluir o laboratório.

24. Parabéns! Você concluiu o exercício de criação de uma página da Web usando a Grade de Bootstrap.

## Dicas

- Certifique-se de adicionar suas colunas aos elementos de linha.
- Lembre-se de que o Bootstrap usa um sistema de grade de 12 colunas.
- Revise as lições "Usando estilos de bootstrap" e "Grade de bootstrap".

