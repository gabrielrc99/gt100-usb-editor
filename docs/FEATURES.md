# Melhorias do GT-100 USB Editor

**Português (Brasil)** · [English](FEATURES.en.md)

[← Página principal](../README.md) · [Baixar para Windows](../windows/README.md) · [Agradecimentos](../README.md#agradecimentos)

O GT-100 USB Editor moderniza a experiência de edição da BOSS GT-100. Esta página apresenta as melhorias que o projeto acrescenta ao trabalho com a pedaleira: uma nova interface com suporte a português, atalhos de Assign, cenas automáticas, Pseudo IR, cópia de configurações e histórico de edição.

## Interface modernizada

A nova interface reúne a cadeia de sinal e os parâmetros do efeito selecionado na mesma tela. Os estados dos blocos e os caminhos dos canais A/B aparecem visualmente, e os efeitos podem ser reorganizados por arraste.

Os knobs permitem arraste, ajuste fino com **Shift** e entrada numérica. A interface vetorial acompanha a escala de exibição do Windows. Mudanças recebidas da pedaleira atualizam o editor.

## Suporte a português do Brasil

Além do inglês, o editor oferece uma interface em **português do Brasil**, com tradução dos menus, controles e mensagens. Para trocar o idioma, abra **Settings → Language** e selecione **Português (Brasil)**. O inglês é o idioma padrão do aplicativo.

A preferência de idioma é mantida na próxima abertura. Nomes de patches e outros dados do usuário são preservados ao trocar o idioma.

## Cópia de configurações e proteção ao salvar

Copie e cole configurações de blocos compatíveis pelo menu de contexto, facilitando o reaproveitamento de ajustes. Também é possível copiar o timbre completo para outra posição de usuário.

## Assigns por atalho

Clique com o botão direito em um knob ou switch compatível e escolha **Assign → Assign 1–8**. O editor preenche o destino e seus limites, facilitando a associação daquele parâmetro a um pedal ou controlador.

A fonte, o modo e o estado do Assign continuam disponíveis para configuração. Parâmetros sem destino compatível não oferecem o atalho; recursos ocupados pelas cenas recebem proteção para evitar conflitos.

## Cenas com configuração automática

Prepare uma configuração **Padrão** e variações para **ACCEL** e **LOOP** dentro do mesmo patch. O editor compara os ajustes e organiza as funções de pedal e os Assigns necessários para alternar entre eles.

Você pode revisar os recursos utilizados e conferir o resultado antes de salvar. As cenas dependem dos controles e dos **oito Assigns físicos da GT-100**: a quantidade de diferenças entre configurações determina o que é possível gerar. Depois de gravadas no patch, as mudanças configuradas são executadas pela própria pedaleira.

## Pseudo IR

O Pseudo IR usa um **IR de gabinete em WAV como referência** e procura configurações internas da GT-100 que aproximem sua resposta de frequência. Isso permite levar a configuração para o patch sem depender de um computador durante o uso da pedaleira.

### Importar e comparar

1. Abra a página **Pseudo IR** e adicione um IR em WAV.
2. Confira o gabinete e as versões calculadas.
3. Compare o gráfico e ouça as alternativas com as amostras de guitarra do aplicativo.
4. Escolha a versão e aplique ao canal de pré-amplificador desejado.
5. Teste o timbre na pedaleira e use **Salvar…** para manter o resultado.

Cada conversão oferece quatro compromissos entre aproximação e uso de recursos:

| Versão | Blocos utilizados |
| --- | --- |
| Só gabinete | Simulação de gabinete e microfone do pré-amplificador |
| Gabinete + EQ | Gabinete e equalizador dedicado |
| Gabinete + EQ + 1 FX | Gabinete, EQ e um FX configurado como equalizador |
| Gabinete + EQ + 2 FX | Gabinete, EQ e os dois FX configurados como equalizadores |

Usar mais EQs ocupa blocos que você poderia reservar para outros efeitos. Na versão com um FX, é possível escolher **FX1** ou **FX2**. A busca pode incluir gabinetes **CUSTOM**, e oferece prioridades de ajuste de EQ.

As conversões ficam em uma biblioteca local. A comparação por áudio permite alternar entre o IR original e as versões previstas; o modo nerd expõe mais informações sobre o ajuste.

### Como interpretar o resultado

O objetivo é aproximar a **magnitude da resposta de frequência** dentro da faixa analisada. A porcentagem de proximidade compara a forma espectral após alinhar o volume; ela não é uma porcentagem de fidelidade sonora ou de percepção humana.

A GT-100 **não passa a carregar o WAV nem a executar IRs**. O patch usa seus próprios gabinetes e equalizadores. Fase, resposta temporal e comportamento dinâmico de um IR original não são reproduzidos integralmente. A audição no computador é uma previsão para ajudar na escolha; confirme o resultado com sua guitarra e seu sistema de saída. O PseudoIR segue em desenvolvimento.

## Desfazer e refazer edições

Use **Ctrl+Z** para desfazer e **Ctrl+Y** ou **Ctrl+Shift+Z** para refazer edições do patch atual. O histórico agrupa um arraste de knob em uma ação e abrange parâmetros, liga/desliga, ordem da cadeia, Assigns e outras operações de edição. Trocar ou recarregar o patch, salvar ou desconectar inicia um novo histórico.

[Voltar à página principal](../README.md)
