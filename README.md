<div align="center">

[Português](README.md) · [English](README_EN.md) · [Español](README_ES.md)

# Rodrigo Araújo — CesnnaBravo
### ETS BRAKE FADE 0.8.0

![Versão](https://img.shields.io/badge/ETS_BRAKE_FADE-0.8.0-5965F2?style=for-the-badge)
![Plataforma](https://img.shields.io/badge/Windows-x64-0078D4?style=for-the-badge)

[Site oficial](https://cb-mods-road.wswmjkwr2r.chatgpt.site/) · [Downloads](https://cb-mods-road.wswmjkwr2r.chatgpt.site/#mods) · [Discord](https://discord.gg/yFgebpcX8)

</div>

> **AVISO — ESTAMOS MIGRANDO PARA O SITE OFICIAL**
>
> A central do mod agora é o [site CB Mods](https://cb-mods-road.wswmjkwr2r.chatgpt.site/): downloads atualizados, tutoriais, cadastro, biblioteca e compra do complemento de fumaça ficam lá. Este GitHub continua como apresentação do projeto e referência para a comunidade. Para baixar a versão atual, use o site; arquivos antigos não representam necessariamente a distribuição vigente.

## O projeto

Sou Rodrigo Araújo Campos, conhecido como CesnnaBravo. Desenvolvo mods com apoio de IA, buscando acrescentar simulação e imersão às viagens.

O **ETS BRAKE FADE** simula o aquecimento, o resfriamento e a perda de eficiência dos freios, agora com dados separados para caminhão e reboques. As temperaturas, massas e potências são **estimativas do modelo**, com perfil térmico genérico; não são medições reais nem dados de fabricante.

## Novidades da 0.8.0

- Temperaturas e perda de capacidade separadas por veículo, com recuperação ao esfriar.
- Massa total estimada do conjunto, carga, velocidade e inclinação no cálculo térmico.
- Comandos originais do jogo para teclado, controle e volante: **sem calibração no plugin e sem F9**.
- Painel com temas claro/escuro, português/inglês/espanhol, áudio e avisos.
- Ajustes de aquecimento e resfriamento entre **25% e 200%**. Maior percentual significa mais rápido.
- Complemento **Brake Smoke** com fumaça no caminhão e nos reboques conectados, perfis parado/em movimento, densidade ajustável e botão de ativar/desativar.
- Conta vinculada ao painel pelo navegador e verificação de acesso à fumaça pelo servidor.
- Aviso de novas versões publicadas no site. A instalação continua manual.

### Curva de perda de eficiência

| Temperatura estimada | Ganho do freio de serviço do veículo afetado |
|---|---|
| Até 350 °C | 100% |
| 440 °C | 50% |
| 530 °C ou mais | 0% |

A queda é progressiva entre 350 e 530 °C. Caminhão e reboques são tratados separadamente. A capacidade recupera ao esfriar; estacionamento e freios auxiliares são preservados. Esta curva é um ajuste do mod, não uma especificação de freios reais.

## Base gratuita e fumaça paga

| Produto | Acesso |
|---|---|
| **ETS Brake Fade — base** | Gratuito; os freios funcionam sem login. |
| **Brake Smoke — complemento** | **R$ 15**, pagamento único pelo site. Requer conta com acesso liberado, verificação online e SCS ativo. |

A compra confirmada libera o complemento na biblioteca da conta. A vinculação no painel usa um código autorizado no site; a senha não é salva no plugin. Quem recebeu acesso manual do administrador também pode utilizar o complemento.

Sem verificação online, a fumaça fica bloqueada; os freios base continuam disponíveis. A densidade varia de **0% a 500%** e pode ser desativada pelo painel. A emissão é solicitada a partir de **420 °C** por veículo e cessa ao esfriar para **380 °C ou menos**, com dissipação gradual das partículas.

## Compatibilidade atual

**Windows x64 · ETS2 1.62.1.0 — executável reconhecido pela integração nativa.**

**American Truck Simulator: compatibilidade em preparação.** A 0.8.0 e seu complemento de fumaça ainda não devem ser usados ou comprados como compatíveis com ATS. Outras versões do jogo também exigem adaptação e validação. O suporte de versões antigas do plugin não garante o suporte do novo sistema.

## Instalar e atualizar

1. Feche o jogo e guarde o pacote anterior fora da pasta `plugins`.
2. Baixe a base atual pelo site. Copie o conteúdo de `plugins` para `Euro Truck Simulator 2\bin\win_x64\plugins`.
3. Mantenha as **duas DLLs**: `ets2_brake_fade.dll` e `cb_brake_smoke_probe.dll`, além de `cb_smoke_native.ini` e `sounds`. Apesar do nome antigo, a segunda DLL executa física e partículas; ela é necessária.
4. Retire DLLs antigas duplicadas e o diagnóstico `cb_brake_physics_probe.dll`. Preserve `brake_fade_v07.ini` para manter suas preferências.
5. Use os comandos originais do jogo. Retire a associação do eixo virtual antigo, se existir. Abra o painel com **F10** ou seu atalho salvo.
6. Para a fumaça, instale também o SCS do complemento na pasta `Documentos\Euro Truck Simulator 2\mod`, ative-o no Gestor de Mods e vincule a conta pelo painel. Use a localização de Documentos configurada no Windows.

**Tutoriais completos:** [instalar a base gratuita](https://cb-mods-road.wswmjkwr2r.chatgpt.site/install-base.html) · [instalar e ativar a fumaça](https://cb-mods-road.wswmjkwr2r.chatgpt.site/install-smoke.html)

## Suporte e próximas melhorias

Envie no [Discord](https://discord.gg/yFgebpcX8) as versões do jogo e do mod, seu equipamento, passos do problema, `game.log.txt` e `brake_fade_v07.log`. Nunca compartilhe senha ou `account.dat`.

As prioridades são estabilidade, testes em mais conjuntos e adaptação para ATS. Não há promessa de data ou compatibilidade com todas as configurações. Testes automatizados e relatos dos jogadores não substituem a validação em cada versão do jogo.

## Apoiar o desenvolvimento

A base é gratuita. Doações são opcionais e separadas da compra do complemento de fumaça.

[Buy Me a Coffee](https://buymeacoffee.com/cesnnabravo) · [Instagram](https://instagram.com/rodrigoaraujoca2/) · [Discord](https://discord.gg/yFgebpcX8)

PIX para doação — Rodrigo Araújo Campos: `c2ad1129-8267-4e80-a0b6-2e0ddb93526c`.

**Realismo • Simulação • Imersão — CesnnaBravo**
