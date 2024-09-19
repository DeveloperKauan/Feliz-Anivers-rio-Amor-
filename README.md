# Projeto de Site Romântico

Este projeto é um site romântico criado como um presente especial, contendo animações de corações, música de fundo, um contador personalizado, uma mensagem de amor e um vídeo especial. O layout é totalmente responsivo, garantindo que o conteúdo seja exibido corretamente em dispositivos de diferentes tamanhos.

## Preview
https://juliayukari.netlify.app

## Estrutura do Projeto

O projeto contém as seguintes seções principais:
- **Contador de idade e tempo de relacionamento**: Um contador que exibe a idade da pessoa e o tempo total do relacionamento.
- **Animações e Corações**: Elementos flutuantes em forma de coração que se movem pela tela.
- **Música de Fundo**: Um áudio que toca em loop automaticamente quando o site é carregado.
- **Vídeo**: Um vídeo especial, com uma legenda descritiva, que pode ser reproduzido diretamente no site.
- **Poema/Mensagem Romântica**: Um texto carinhoso dedicado à pessoa especial.

## Como Usar

### 1. Modificar as Datas (Aniversário e Início do Relacionamento)
Para atualizar o site com a data correta de nascimento e o início do relacionamento, você precisará modificar dois trechos no código JavaScript.

- **Data de nascimento (para o contador de idade)**:
  ```javascript
  const birthDate = new Date("2006-09-19T00:00:00");
  ```

  Atualize `"2006-09-19"` com a data de nascimento correta. O formato deve ser `YYYY-MM-DD`.

- **Data de início do relacionamento (para o contador de namoro)**:
  ```javascript
  const startDate = new Date("2023-06-12T00:00:00");
  ```

  Modifique `"2023-06-12"` para a data de início do relacionamento, seguindo o formato `YYYY-MM-DD`.

### 2. Substituir o Vídeo
O site contém um vídeo especial com uma legenda. Para trocar o vídeo, siga estas instruções:

- **Substituir o vídeo**:
  ```html
  <source src="balanco.mp4" type="video/mp4">
  ```

  Substitua `balanco.mp4` pelo nome do seu arquivo de vídeo. Certifique-se de que o arquivo de vídeo esteja na mesma pasta do arquivo HTML ou ajuste o caminho conforme necessário.

- **Modificar a legenda do vídeo**:
  ```html
  <div class="video-legend">O primeiro vídeo que gravamos juntos, e eu sempre fico feliz quando vejo</div>
  ```

  Edite o texto entre as tags `<div>` para alterar a legenda do vídeo.

### 3. Modificar a Música de Fundo
O site contém uma música que toca automaticamente quando carregado. Para alterar essa música:

- **Trocar o arquivo de música**:
  ```html
  <source src="amore.mp3" type="audio/mpeg">
  ```

  Substitua `amore.mp3` pelo nome do arquivo de áudio desejado. O formato deve ser `mp3`.

### 4. Alterar o Poema ou Mensagem Romântica
O poema/mensagem está em uma seção HTML dedicada. Para modificar o conteúdo:

- Localize o poema:
  ```html
  <h1>Dessa vez não tem poema</h1>
  <p>
    Me desculpa,amor<br>
    Dessa vez não tem poesia<br>
    Dessa vez não quero que tenha dor<br>
    Dessa vez não vou dizer minha ânsia<br>
    ...
  </p>
  ```

  Você pode substituir o texto dentro das tags `<p>` pelo seu próprio poema ou mensagem especial.

### 5. Customizar as Cores e Animações
O CSS controla o visual do site, como as cores e as animações dos corações. Para alterar isso:

- **Modificar as cores de fundo e dos elementos**:
  No bloco de estilos (`<style>`), há definições de cores, como este gradiente de fundo:
  ```css
  background: linear-gradient(to bottom, #fbc2eb, #a18cd1);
  ```

  Substitua as cores hexadecimais (#fbc2eb e #a18cd1) pelas cores que você desejar.

- **Ajustar as animações dos corações**:
  A animação de flutuação dos corações é controlada com a seguinte regra CSS:
  ```css
  @keyframes float {
    0% { transform: translateY(0); }
    50% { transform: translateY(-20px); }
    100% { transform: translateY(0); }
  }
  ```

  Para modificar a velocidade ou intensidade da animação, você pode ajustar os valores de `translateY` ou a duração nas definições de cada coração:
  ```css
  .heart {
    animation-duration: 3s; /* Ajuste a duração */
  }
  ```

## Dependências

O projeto usa as seguintes bibliotecas e fontes externas:
- **Bootstrap**: Para o layout responsivo.
- **Google Fonts**: Para as fontes personalizadas (`Poppins` e `Great Vibes`).
- **FontAwesome**: Para os ícones de coração.
- **AOS (Animate on Scroll)**: Para as animações de rolagem das seções.

Não é necessário instalar nada adicional, pois as bibliotecas são carregadas via CDN.

## Executar o Projeto

1. Faça o download ou clone o projeto.
2. Coloque todos os arquivos de mídia (áudio, vídeo, etc.) na mesma pasta que o arquivo HTML.
3. Abra o arquivo `index.html` em qualquer navegador.
