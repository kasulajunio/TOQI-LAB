# TOQI LAB Runner retrô

Ferramenta experimental para abrir ROMs locais autorizadas no navegador, usando [EmulatorJS](https://github.com/EmulatorJS/EmulatorJS) oficial, baseado em núcleos libretro. Não é um emulador de jogos modernos de PC: Minecraft e GTA V não são suportados. Não inclui nem fornece ROMs ou BIOS.

## Uso

1. Abra a página runner/ em um servidor HTTPS ou GitHub Pages, com internet.
2. Escolha o console e um arquivo que você tem direito de usar no seu aparelho.
3. Toque em Iniciar e aguarde o download do emulador e núcleo. Use os controles de tela quando disponíveis. Para trocar de jogo, use Escolher outro jogo; isso recarrega a página.

NES, Game Boy/Color, GBA, SNES, Mega Drive, Master System e Game Gear são oferecidos como alvos, não como garantia de compatibilidade. ROMs incompatíveis, compactação, recursos gráficos, navegador ou hardware podem impedir a execução. Alguns jogos podem precisar de arquivos adicionais não disponibilizados aqui. Salvos podem depender do armazenamento local do navegador e ser perdidos ao limpar dados. Teste com arquivos legais pequenos antes de depender da ferramenta.

## Dados e dependência

A página não contém rotina para enviar a ROM a servidor próprio; passa o objeto File ao EmulatorJS, conforme exemplo oficial. O código do emulador e seus núcleos são baixados do CDN de terceiros, que recebe endereço IP e dados normais de conexão; não se pode garantir como código de terceiros se comportará em versões futuras. Use apenas arquivos de jogos, nunca documentos sensíveis. O canal stable pode mudar: em verificação estava em 4.2.3; não é fixação imutável.

O projeto upstream é licenciado sob GPL-3.0: [código e licença](https://github.com/EmulatorJS/EmulatorJS), [opções](https://emulatorjs.org/docs/options/), [núcleos](https://emulatorjs.org/docs4devs/cores/) e [releases](https://github.com/EmulatorJS/EmulatorJS/releases). Os núcleos e outros componentes têm suas próprias licenças. A página baixa componentes do CDN oficial em tempo de uso; disponibilidade e mudanças do serviço estão fora do controle do TOQI LAB.

Para um possível teste livre, o autor de [Thwaite para NES](https://github.com/pinobatch/thwaite-nes) declara GPL-3.0 ou posterior e fornece uma ROM de 24 KB na [release 0.04](https://github.com/pinobatch/thwaite-nes/releases/tag/v0.04). Ela não está incluída aqui. O jogo usa efeitos intermitentes; atenção a fotossensibilidade.