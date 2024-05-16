# BREAKOUT GAME

Este código implementa um jogo inspirado no clássico "Breakout" de 1976 para ser executado em uma placa DE1-SoC. O jogo utiliza a interface VGA para exibir os elementos visuais na tela e o acelerômetro para movimentar a raquete/barra. Além disso, são utilizados botões para reiniciar, pausar e continuar o jogo, e a interrupção de sinal SIGINT (geralmente acionada pelo comando Ctrl+C) é utilizada para encerrar o jogo.

### Estrutura do Código

1. **Bibliotecas e Constantes:**
   - Inclui bibliotecas padrão do C e bibliotecas específicas para interagir com os periféricos da placa DE1-SoC.
   - Define constantes como as dimensões da tela e das estruturas do jogo.

2. **Estruturas de Dados:**
   - Define as estruturas `Projetil`, `Raquete` e `Bloco`, que representam os elementos do jogo.

3. **Funções:**
   - `catchSIGINT`: Tratamento de sinal para encerrar o jogo ao receber o sinal SIGINT.
   - `interpreta_botoes`: Interpreta o estado dos botões da placa.
   - `gera_blocos`: Gera os blocos do jogo no início.
   - Outras funções para exibir os blocos na tela e detectar colisões.

4. **Função Principal (main):**
   - Inicializa os periféricos e variáveis do jogo.
   - Entra em um loop principal que controla o fluxo do jogo.
   - Durante o jogo, lê os botões, atualiza a posição da raquete com o acelerômetro, atualiza a posição da bola, verifica colisões e exibe os elementos na tela.
   - Exibe mensagens de vitória, derrota ou fim de jogo e aguarda a ação do jogador para reiniciar o jogo.
   - Encerra os periféricos e finaliza o programa.
