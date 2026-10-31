<div align="center">

[Português](README.md) · [English](README_EN.md) · [Español](README_ES.md)

# Rodrigo Araújo — CesnnaBravo
### Mods para Euro Truck Simulator 2 e American Truck Simulator

![Versão](https://img.shields.io/badge/ETS_BRAKE_FADE-0.7.3.1-5965F2?style=for-the-badge)
![Plataforma](https://img.shields.io/badge/Windows-x64-0078D4?style=for-the-badge)
![Status](https://img.shields.io/badge/STATUS-BETA-F5A623?style=for-the-badge)

[Download oficial](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link) · [Discord](https://discord.gg/yFgebpcX8) · [Instagram](https://instagram.com/rodrigoaraujoca2/) · [Apoiar](https://buymeacoffee.com/cesnnabravo)

</div>

## Sobre o projeto

Sou Rodrigo Araújo Campos, conhecido como CesnnaBravo. Desenvolvo mods e plugins DLL para ETS2 e ATS, com inteligência artificial como ferramenta de apoio. Meu foco é acrescentar mecânicas de simulação, dificuldade e imersão.

O **ETS BRAKE FADE** simula a temperatura dos freios e a redução de eficiência causada pelo superaquecimento. Frenagens prolongadas e repetidas acumulam calor; o resfriamento recupera a eficiência térmica gradualmente. Carga, velocidade, desgaste do chassi e inclinação estimada influenciam o modelo.

A temperatura exibida é **calculada pelo mod**, não uma medição real dos discos ou tambores. Não existe nesta versão um sistema de excesso de peso nem um sistema independente de desgaste/manutenção dos freios.

## Novidades da 0.7.3.1

- **Painel claro ou preto**, com tema salvo automaticamente e interface em português, inglês e espanhol.
- **Ajustes térmicos:** temperatura de início do ruído, taxa de aquecimento e taxa de resfriamento.
- **Monitor de freios:** temperatura simulada, eficiência, carga e inclinação estimada.
- **Teclado, controle e volante na mesma DLL**, selecionáveis no painel.
- **ETS2 e ATS:** identificação do jogo e calibração armazenada na pasta correspondente.
- **Identificação nas configurações do jogo:** `ETS BRAKE FADE 0.7.3.1`. O identificador interno foi preservado para manter associações existentes.
- **Verificador de atualizações**, com suporte a versões de três ou quatro números. O aviso depende de uma versão superior publicada no servidor; a instalação continua manual.

### Correções incluídas

| Área | Correção |
|---|---|
| Carregamento no Windows | Runtime C++ incorporado à DLL, removendo as dependências externas do Visual C++ envolvidas no caso relatado de erro `0000007E`. |
| Painel térmico | Sliders desenhados pelo próprio painel para corrigir barras vazias; suporte a arraste, teclado e reabertura. |
| Barra do freio no jogo | Leitura do pedal/S nas opções enquanto a condução está pausada, sem atualizar a simulação térmica. |
| Calibração | Validação de conclusão, curso, sentido e valores; arquivos inválidos não são tratados como calibrados. |
| Pedais | Persistência dos eixos Slider 1/2 e tentativa de recuperação após perda de leitura. |
| Salvamento | Gravação temporária antes de substituir a calibração e diagnóstico quando não é possível salvar. |
| ATS | Calibração separada do ETS2 e seleção da janela pelo processo que carregou o plugin. |
| Entrada e inicialização | Ressincronização do eixo, F9 limitado à janela do jogo e diagnóstico de falha nos eventos essenciais do SDK. |
| Simulação | Tratamento de valores de telemetria inválidos para evitar corromper a temperatura e a saída do freio. |

**A fumaça nos freios não faz parte desta atualização.** O experimento está adiado e desativado na distribuição normal.

## Download

Use a [pasta oficial de downloads](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link) e confira se o ZIP corresponde à **0.7.3.1**. A pasta pode conter versões anteriores. O site está em preparação; o link acima continua sendo a referência para o download.

## Instalação — Windows 64 bits

1. Feche o jogo e guarde uma cópia da DLL anterior fora da pasta `plugins`.
2. Extraia o pacote. Copie **`ets2_brake_fade.dll`** e **`sounds`** para a pasta correspondente:

```text
Euro Truck Simulator 2\bin\win_x64\plugins
American Truck Simulator\bin\win_x64\plugins
```

3. Crie `plugins` se não existir. Mantenha **somente uma DLL do Brake Fade** em cada instalação.
4. Preserve `brake_fade_v07.ini` para manter suas preferências. Se testou a fumaça, retire `cb_brake_smoke_probe.dll` e substitua o host experimental pela DLL normal.
5. Abra o jogo, carregue o perfil/save e entre na condução. Abra o painel com **F10** ou seu atalho salvo.

O nome `ets2_brake_fade.dll` é o mesmo nos dois jogos; ele não indica exclusividade do ETS2. Este plugin é instalado na pasta do executável, não como arquivo `.scs` no Gerenciador de Mods.

## Teclado, controle e volante

| Atalho padrão | Função |
|---|---|
| F10 | Abrir/fechar o painel. Pode ser alterado. |
| F7 | Avançar a calibração de controle/volante. Pode ser alterado. |
| F9 | Pulso para associar o eixo virtual ao freio do jogo. Fixo. |
| S | Freio no modo Teclado. Fixo. |
| Esc | Fechar o painel ou cancelar a captura de um atalho. |

### Teclado

Selecione **Teclado** no painel. Segure **S** para frear e solte para liberar. Não precisa de controle nem de calibração.

Nas configurações do jogo, associe o **eixo virtual** ao freio: selecione o campo **Eixo do freio** e pressione F9. Remova a atribuição digital original de S ao freio para ela não aplicar frenagem em paralelo e contornar o fade.

Durante a condução, o plugin ignora S fora da janela do jogo ou com o painel aberto. Ao retornar de uma pausa ou trocar de modo, solte S antes de pressionar novamente.

### Controle, volante e pedais

Selecione **Controle/volante** e confira o atalho salvo. Na condução, com o painel fechado:

1. Solte o freio completamente; pressione e solte o atalho de calibração.
2. Pressione **somente o freio** até 100%, segure e pressione o atalho novamente.
3. Solte completamente o freio e pressione o atalho pela terceira vez.
4. Confira a conclusão e o salvamento em **Diagnóstico**.
5. Selecione **Eixo do freio** nas opções do jogo e use F9 para associar o eixo virtual.

Confira a polaridade: a barra deve ficar em repouso com o freio solto e aumentar ao pressionar. **Mantenha Normal/Invertido se já funciona corretamente no seu perfil.** Nunca associe o eixo do Brake Fade à direção.

Arquivos antigos sem confirmação de calibração concluída exigem uma nova calibração uma única vez. Configurações válidas da revisão de estabilidade podem ser reaproveitadas. A compatibilidade depende de o driver expor um eixo analógico legível; não há garantia para todos os equipamentos.

### Onde ficam os arquivos?

| Arquivo | Local |
|---|---|
| Preferências e atalhos | `brake_fade_v07.ini`, junto da DLL. |
| Log do plugin | `brake_fade_v07.log`, junto da DLL. |
| Calibração ETS2 | `Documentos\Euro Truck Simulator 2\BrakeFade\wheel_config.ini` |
| Calibração ATS | `Documentos\American Truck Simulator\BrakeFade\wheel_config.ini` |

O caminho acompanha a pasta Documentos configurada no Windows. ETS2 e ATS têm calibrações separadas. Se uma versão antiga do ATS salvou na pasta do ETS2, calibre novamente no ATS; não é necessário apagar o arquivo do ETS2.

## Personalizar os freios

Na aba **Ajustes térmicos**:

| Ajuste | Faixa | Padrão |
|---|---|---|
| Temperatura de início do ruído | 50–500 °C | 100 °C |
| Taxa de resfriamento | 25–200% | 100% |
| Taxa de aquecimento | 25–200% | 100% |

**Maior taxa = mais rápido; menor taxa = mais demorado.** Os percentuais são taxas, não tempos em segundos. O ruído exige frenagem e movimento e cresce gradualmente após o limiar.

100% preserva o ajuste de resfriamento lento. No teste do modelo, sem frear, a queda de 500 °C para 150 °C levou cerca de **6min30s parado** e **3min43s a 80 km/h**. São referências da simulação em tempo ativo, não medições de um caminhão real; frenagens e outras configurações mudam o resultado.

O botão **Tema: claro / Tema: preto** fica na parte inferior da barra lateral. Volume, idioma, avisos e simulação também são ajustáveis. As preferências são salvas automaticamente.

## Solução de problemas e suporte

- **Não aparece painel nem aviso:** confira `game.log.txt`. O erro `unable to load: 0000007E` ocorre antes de o plugin iniciar. Use o pacote atualizado; ele incorpora o runtime C++ e remove as dependências externas do Visual C++ da compilação anterior. Se persistir, envie um novo log.
- **Não freia:** confira o modo escolhido, a calibração e a associação do eixo virtual ao freio. Teste a barra nas opções do jogo.
- **Direção brusca em A/D:** confira as associações e o tipo de controle do jogo. O eixo virtual do mod deve atuar somente no freio.
- **Calibração não salva:** confira o diagnóstico e envie o log. Uma calibração pode funcionar na sessão e precisar ser refeita após reiniciar se o salvamento falhou.
- **Sem áudio:** confira volume, simulação ativada, saída do Windows e a pasta `sounds`. As camadas WAV usam PCM de 16 bits, mono ou estéreo. O som procedural pode funcionar mesmo sem os WAVs.
- **Sem aviso sobreposto:** teste janela ou janela sem bordas. Tela cheia exclusiva pode impedir a exibição.

No [Discord](https://discord.gg/yFgebpcX8), informe versão do mod e do jogo, equipamento, modo de entrada e passos para reproduzir. Envie `game.log.txt` e `brake_fade_v07.log` da tentativa afetada. O log do jogo normalmente fica em Documentos na pasta do ETS2/ATS, ou no `-homedir` personalizado.

A compilação x64 e **oito testes automatizados** passaram, incluindo carregamento da DLL, identificação ATS/ETS2, dependências, calibração, idiomas, entrada, física térmica e painel. Houve confirmação de usuários para as correções relatadas; isso não garante ausência de bugs em todas as configurações.

## Tutoriais em vídeo

[Tutorial 1](https://www.youtube.com/watch?v=pR7P1BxTyl8) · [Tutorial 2](https://www.youtube.com/watch?v=25W1FI4E_3o&t=205s)

Os vídeos podem mostrar versões anteriores. Para atalhos, instalação e calibração da 0.7.3.1, siga este README.

## Histórico resumido

| Versão | Principais mudanças |
|---|---|
| **0.7.3.1** | Temas claro/preto, ajustes térmicos, monitor, correções de painel/calibração/entrada, suporte ATS revisado e carregamento sem dependências externas do Visual C++. |
| 0.7 | Teclado e controle/volante unificados, painel redesenhado, três idiomas, atalhos e diagnóstico. |
| 0.6 | Áudio dinâmico e transições suaves. |
| 0.5 | Ajustes no resfriamento e influência de carga/desgaste do chassi. |
| 0.4 | Avisos de temperatura, calibração e configurações salvas. |
| 0.3 | Ampliação do suporte a dispositivos de entrada. |

## Próximas melhorias — em estudo

- Continuar corrigindo falhas com base nos logs e relatos da comunidade.
- Ampliar testes com volantes, pedais e controles no ETS2 e ATS.
- Refinar diagnóstico, interface e comportamento térmico com o retorno dos jogadores.
- Retomar a pesquisa de fumaça nos freios depois da etapa de estabilidade. O protótipo atual é diagnóstico; **não emite partículas visuais**.

Estes itens não são recursos já disponíveis nem promessas de data ou compatibilidade. A prioridade atual é estabilidade.

Versões antigas que reconhecem apenas três números não detectam automaticamente a atualização `0.7.3.1`; essa migração é manual. O verificador desta versão reconhece três ou quatro números e não instala DLLs sozinho.

## Apoiar o desenvolvimento

O mod é gratuito. Doações são opcionais e não são necessárias para baixar ou usar.

[Buy Me a Coffee](https://buymeacoffee.com/cesnnabravo)

PIX — chave aleatória, Rodrigo Araújo Campos:

```text
c2ad1129-8267-4e80-a0b6-2e0ddb93526c
```

[Instagram](https://instagram.com/rodrigoaraujoca2/) · [Discord](https://discord.gg/yFgebpcX8) · [GitHub](https://github.com/RodrigoAraujo34/RodrigoAraujo34)

**Realismo • Simulação • Imersão — CesnnaBravo**
