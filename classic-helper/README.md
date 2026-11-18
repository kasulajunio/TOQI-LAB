# Classic Helper — experimental

Controles de toque experimentais para o [Minecraft Classic oficial](https://classic.minecraft.net/), com jogo carregado apenas no site oficial. Não inclui nem hospeda o código do jogo. Não é afiliado à Mojang ou Microsoft.

## Situação dos testes

No navegador remoto de desktop, o arquivo bookmarklet foi acionado como link javascript na página oficial e os botões apareceram; movimento e câmera alteraram a posição e a orientação no jogo, e Bloco + alterou o item selecionado. Uma versão anterior equivalente dos controles também foi testada no navegador remoto: pulo, quebra e colocação de bloco. A execução como favorito no Chrome Android e o multitouch em celular físico NÃO foram testados. A tela inicial, o inventário, os menus e compatibilidade com mudanças futuras no jogo não foram validados em Android. Isto é um experimento, não garantia de jogo funcional no telefone.

## Página de configuração

Use https://kasulajunio.github.io/TOQI-LAB/classic-helper/ para copiar o favorito, ver o passo a passo e testar eventos de toque nesta página (não no jogo). O código legível está em [helper.js](helper.js); o favorito autônomo gerado em [bookmarklet.txt](bookmarklet.txt). A página não ativa nada automaticamente: o favorito precisa ser executado na aba do jogo depois de o mundo carregar.

A revisão acrescenta posicionamento explícito ao grupo superior, rótulos de acessibilidade, layout compacto em telas baixas e solta teclas ao sair ou ocultar a aba. Os eventos continuam sintéticos; não confundir os testes em navegador remoto com teste em um Android físico.

## Como tentar no Chrome Android, sem instalar aplicativo

1. Abra [bookmarklet.txt](bookmarklet.txt) no GitHub e copie a linha inteira, incluindo `javascript:`. Confira que o endereço do arquivo é do repositório `kasulajunio/TOQI-LAB`. Se a visualização truncar, use Raw e selecione o texto completo.
2. No Chrome, salve qualquer página como favorito pelo menu ⋮ e estrela. Abra ⋮ > Favoritos, encontre o favorito e toque em ⋮ > Editar. Troque o nome para `Classic Helper`; substitua todo o campo URL pela linha copiada; confira que começa exatamente com `javascript:` e salve. Não cole o código diretamente na barra de endereço: o Chrome pode remover esse prefixo.
3. Abra https://classic.minecraft.net/ no Chrome e ative ⋮ > Para computador / Site para computador. Recarregue se necessário. Tente iniciar o mundo e espere ele aparecer. O modo para computador pode não contornar todas as verificações de dispositivo ou outros requisitos; se a página continuar exibindo o aviso de teclado, o helper não o resolve.
4. Com o mundo oficial aberto na mesma aba, toque na barra de endereço, digite `Classic Helper` e escolha a sugestão correspondente ao favorito. Não aperte a sugestão de pesquisa. O favorito deve executar o código na aba atual, não abrir o GitHub. Se o Chrome ou a política do site bloquear o bookmarklet, não há solução garantida aqui.
5. Setas à esquerda: andar; setas à direita: câmera; segure para continuar. `Pular` pula. `Alternar modo` troca entre quebrar e colocar, e `Ação` aplica o modo ao bloco sob a mira. `Bloco +` avança pela barra rápida. `Inventário` tenta abrir o inventário; interação com menus ainda é limitada. `Fechar X` remove o painel; para restaurar completamente o estado do jogo, recarregue a página (isso pode perder o mundo em andamento). Reaplique o favorito após recarregar.

## Segurança e limitações

Um bookmarklet roda com as permissões da página aberta; examine o código antes de usá-lo. Este código original só aceita o endereço HTTPS classic.minecraft.net, cria botões e envia eventos locais; não foi projetado para pedir senhas nem transmitir dados. Nunca execute um favorito de fonte desconhecida em serviços bancários ou contas. Não insira senha neste helper.

O jogo exige tecnologias do navegador como WebGL e pode exigir recursos adicionais. A tentativa de apontar usa eventos sintéticos e se apoia em comportamento interno atual do jogo, inclusive a detecção de touchmove para dispensar pointer lock: isso pode quebrar ou ser bloqueado no futuro. Controles personalizados do jogo, menus, tela pequena, desempenho, travamentos, modo computador e gestos simultâneos podem impedir o uso. `Bloco +` assume a posição inicial da barra e pode ficar dessincronizado após seleção por outros meios. Esse projeto não modifica a conta, não instala aplicativo, não republica o jogo e não garante persistência do mundo.
