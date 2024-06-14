O que são Diretivas no Angular

Imagina que o Angular é como um grande jogo de construção com peças mágicas. As diretivas são essas peças mágicas que ajudam a construir e modificar as partes do jogo. Elas dizem ao Angular como mudar o visual ou comportamento de alguma coisa na tela. Então, quando você quer que algo especial aconteça no seu jogo, você usa essas diretivas. É como ter superpoderes para fazer sua página web super legal!

O que são Diretivas Estruturais

As diretivas estruturais são como magias que mudam a forma como as peças do jogo aparecem ou desaparecem. Elas podem fazer uma peça aparecer só quando uma condição especial acontece ou repetir uma peça várias vezes. Pense nelas como um truque de mágica que faz com que partes do jogo sumam ou apareçam do nada. Isso ajuda a deixar o jogo mais dinâmico e interessante!

Exemplos de Diretivas Estruturais

Um exemplo é a diretiva *ngIf, que mostra ou esconde uma peça dependendo de uma condição. Por exemplo, se a peça só deve aparecer quando você ganha pontos. Outro exemplo é *ngFor, que faz uma peça aparecer várias vezes, como quando você quer mostrar vários prêmios que você ganhou. Tem também a *ngSwitch, que mostra uma peça específica entre várias opções, como escolher qual personagem do jogo vai aparecer na tela.

<div>
  <!-- Diretiva *ngIf -->
  <p *ngIf="playerPoints > 0">Congratulations! You have {{ playerPoints }} points.</p>

  <!-- Diretiva *ngFor -->
  <h2>Your Prizes:</h2>
  <ul>
    <li *ngFor="let prize of prizes">{{ prize }}</li>
  </ul>

  <!-- Diretiva *ngSwitch -->
  <div [ngSwitch]="character">
    <p *ngSwitchCase="'warrior'">You are a brave warrior!</p>
    <p *ngSwitchCase="'mage'">You are a wise mage!</p>
    <p *ngSwitchCase="'archer'">You are a skilled archer!</p>
    <p *ngSwitchDefault>Select a character to see their description.</p>
  </div>
</div>

Explicação:
*ngIf: Mostra a mensagem de parabéns se playerPoints for maior que 0.
*ngFor: Itera sobre a lista prizes e mostra cada prêmio em um item de lista.
*ngSwitch: Mostra uma mensagem específica baseada no valor de character.
Este exemplo cobre o uso básico das diretivas estruturais *ngIf, *ngFor e *ngSwitch em Angular.

O que são Diretivas Atributos

As diretivas de atributos são como pincéis mágicos que mudam a cor ou a forma das peças do jogo. Elas não fazem as peças sumirem ou aparecerem, mas mudam como elas parecem ou se comportam. Pense nelas como um superpoder que muda as cores, tamanhos ou até mesmo o jeito que as peças se movem. É uma maneira de personalizar e deixar tudo mais bonito!

Exemplos de Diretivas Atributos

Um exemplo é a diretiva ngClass, que muda a classe CSS de uma peça, como mudar a cor de uma peça quando algo especial acontece. Outro exemplo é ngStyle, que muda o estilo direto da peça, como aumentar o tamanho dela quando você passa o mouse por cima. Também tem a ngModel, que ajuda a ligar uma peça a uma informação do jogador, como o nome do jogador aparecendo na tela quando ele digita.

<div>
  <!-- Diretiva ngClass -->
  <p [ngClass]="{'especial': eventoEspecial}">
    Este texto muda de cor durante um evento especial.
  </p>
  <button (click)="eventoEspecial = !eventoEspecial">Alternar Evento Especial</button>

  <!-- Diretiva ngStyle -->
  <p 
    [ngStyle]="{'font-size': efeitoHover ? '24px' : '16px'}" 
    (mouseover)="efeitoHover = true" 
    (mouseout)="efeitoHover = false">
    Passe o mouse sobre este texto para aumentar seu tamanho.
  </p>

  <!-- Diretiva ngModel -->
  <div>
    <label for="nomeJogador">Digite seu nome: </label>
    <input id="nomeJogador" [(ngModel)]="nomeJogador" placeholder="Nome"/>
    <p>Olá, {{ nomeJogador }}!</p>
  </div>
</div>
Explicação:
ngClass: Adiciona a classe CSS especial ao parágrafo quando eventoEspecial é verdadeiro, mudando a cor do texto.
ngStyle: Altera o tamanho da fonte do parágrafo ao passar o mouse sobre ele, utilizando eventos de mouse (mouseover e mouseout) para alternar entre dois tamanhos de fonte.
ngModel: Liga a entrada de texto ao nomeJogador, atualizando o nome exibido conforme o usuário digita.