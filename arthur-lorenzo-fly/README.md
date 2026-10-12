# Arthur Lorenzo Fly

Jogo 2D em pixel art para celular, jogado deitado. Um avião atravessa 17 fases (do céu de sol até o espaço, com três chefões e três fases bônus) desviando de pássaros, raios, prédios, lava, meteoros e cavernas, e pousa num aeroporto no fim de cada fase. As estrelas pegas viram dinheiro para comprar aviões, rastros e melhorias no hangar.

![Menu do jogo](imagens/capturas/01-menu.png)

## Jogar

| Onde | Como |
|---|---|
| **Qualquer celular (Android ou iPhone)** | Abra **https://ac-costa-games.github.io/arthur-catarina/arthur-lorenzo-fly/** no navegador. Para ter um ícone de app, use "Adicionar à tela inicial" (Chrome: menu ⋮; iPhone/Safari: botão Compartilhar). |
| **App Android (APK)** | No celular, abra **https://github.com/AC-Costa-games/arthur-catarina/releases**, toque em `arthur-lorenzo-fly.apk` na versão mais recente do Arthur Lorenzo Fly e instale. Se o Android pedir, autorize "instalar apps desconhecidos". |

## O que tem nesta pasta

| Caminho (dentro de `arthur-lorenzo-fly/`) | Conteúdo |
|---|---|
| `index.html` | O jogo inteiro em um único arquivo (HTML + CSS + JavaScript). É também a página do site. |
| `android/` | Projeto Android que empacota o jogo como app (tela cheia, deitado, com ícone). |
| `../.github/workflows/arthur-lorenzo-fly-apk.yml` | Automação, na raiz do repositório, que gera o APK no GitHub e publica em **Releases**. |
| `imagens/sprites/` | Todos os desenhos do jogo em pixel art, no tamanho original. |
| `imagens/sprites-grandes/` | Os mesmos desenhos ampliados 8 vezes, para ver ou editar. |
| `imagens/avioes-cartoon/` | Os três aviões em estilo cartoon (PNG e SVG), primeira versão dos desenhos. |
| `imagens/icone/` | Ícone do app. |
| `imagens/capturas/` | Fotos de tela do jogo. |

O jogo não carrega nenhum arquivo de imagem. Todos os desenhos são gerados pelo próprio código (listas de "pixels" dentro do `index.html`). As imagens da pasta `imagens/` são cópias exportadas desses desenhos, para consulta e edição.

## Atualizar o jogo

1. Edite o `index.html` e envie para o GitHub.
2. O site atualiza sozinho em cerca de 1 minuto.
3. O APK novo é gerado em cerca de 3 minutos (aba **Actions**) e aparece em **Releases**. A automação copia o `index.html` para `android/app/src/main/assets/` antes de compilar.

## Jogadores e fases

Na abertura, escolha quem vai voar: **Arthur** ou **Catarina**. Cada um tem seu mapa, suas estrelas, seu avião e seu recorde. O modo (fácil ou normal) muda no botão do mapa.

| Fase | O que muda |
|---|---|
| 1. Céu de sol | Fase de aprendizado: pássaros, balões e montanhas. |
| 2. Chuva | Nuvens de tempestade **piscam antes de soltar um raio**: espere passar. O vento empurra o avião para baixo. |
| 3. Neve | **Gelo nas asas:** sem acelerar, o avião fica pesado. Montanhas mais altas e uma caverna. |
| 4. Noite | Escuro de verdade: **só o farol ilumina**. Morcegos e uma caverna. |
| 5. ⚔ Dirigível Pirata | **Chefão.** Joga barris e dispara o canhão (uma linha vermelha avisa onde o tiro vai passar). |
| 6. Ventania | Colunas de vento: **azul empurra para cima, laranja para baixo**. Pipas no céu. |
| 7. Floresta | **Árvores gigantes**, papagaios e um mar de pinheiros ao fundo. |
| 8. ★ Chuva de Estrelas | **Fase bônus** à noite: estrelas caindo devagar; as **douradas valem 5**. |
| 9. Deserto | **Tempestade de areia** a cada 18 s (com aviso), urubus, cactos e uma caverna. |
| 10. Mar | Tudo depois da praia é água. Navios com mastro, gaivotas e **pouso no porta-aviões**. |
| 11. Cidade | Pôr do sol, **prédios** para passar por cima e helicópteros. |
| 12. Vulcão | **O chão brilha antes da bola de lava subir.** Cinzas, brasas e uma caverna. |
| 13. ⚔ Dragão de Fogo | **Chefão.** Leque de bolas de fogo, tiro mirado e brasas caindo do céu. |
| 14. ★ Arco-íris | **Fase bônus**, sem obstáculos: arcos de estrelas para pegar. |
| 15. Apocalipse | Cidade em ruínas sob o céu vermelho. **Um X vermelho no chão avisa onde o meteoro vai cair.** |
| 16. ★ Terra dos Doces | **Fase bônus** cor-de-rosa com pirulitos: **cada bala vale 3 estrelas**. |
| 17. ⚔ Espaço | Última fase: o avião vira **ônibus espacial**. Planetas, meteoros e satélites; no fim, a **nave alienígena** (laser mirado, leque de plasma e bombas verdes) e o pouso na base da Lua. |

**Chefões:** o avião não atira. Durante a luta aparecem **foguetes** no caminho; cada foguete que você pega é lançado no chefão. O Dirigível aguenta 5 golpes, o Dragão 6 e a Nave Alienígena 7 (todos 3 no modo fácil). Depois da vitória aparece o aeroporto. Nas fases só de chefão, a 2ª estrela é vencer sem perder nenhum avião.

**Marcadores de progressão:** bandeiras quadriculadas no caminho, a 1/3 e 2/3 da fase, **logo antes de cada caverna e no meio dela**, e no começo da luta com o chefão. A bandeira fica verde quando você passa. Se os aviões acabarem, o botão **CONTINUAR DO MARCADOR** volta para a última bandeira, com 3 aviões de novo e as estrelas que você tinha ali.

Cada fase termina num **aeroporto**. Perto dele, aparece uma **linha verde** até a pista: solte o A e desça por ela. As luzes ao lado da pista ficam brancas quando o avião está alto e vermelhas quando está baixo. Se passar da pista sem pousar, o avião arremete e tenta de novo.

Estrelas de cada fase: ⭐ chegar ao aeroporto, ⭐ pegar 60% das estrelas do caminho (40% no fácil) e ⭐ pouso perfeito (tocar a pista devagar). Terminar uma fase libera a próxima. O **Voo livre** é o modo sem fim, com as estações mudando e cavernas.

## Hangar (loja)

Cada estrela pega em qualquer fase (ou no voo livre) vai para a carteira do jogador, que aparece no botão **HANGAR** do mapa. Para comprar, toque no item e **toque de novo para confirmar**. Itens comprados podem ser usados a qualquer hora.

| Seção | Itens e preços |
|---|---|
| Aviões: clássicos | Vermelho, azul e amarelo (grátis) |
| Aviões: países | Brasil, Argentina, EUA, Japão, França, Itália, Portugal e Alemanha (★ 40) |
| Aviões: militares (caças) | Camuflado, Marinha e Deserto (★ 90), Noturno (★ 110) |
| Aviões: futuristas (jatos) | Neon (★ 150), Cromado (★ 180), Galáxia (★ 220), Dourado (★ 300) |
| Rastros | Arco-íris e Bolhas (★ 30), Corações (★ 40), Estrelinhas (★ 50), Fogo (★ 60) |
| Melhorias | Ímã de estrelas (★ 120) e Avião extra: 4 aviões por fase (★ 150) |

**Modo fácil** (pensado para 4 anos): só o analógico, sem botões. O avião acelera e decola sozinho, não explode (só pisca e segue), as fases têm 55% do tamanho e o pouso é feito pelo piloto automático.

## Controles e pontos

- **Analógico (esquerda):** sobe e desce. Na pista, empurre para cima para decolar.
- **A (vermelho):** segure para acelerar. Soltou, o avião desacelera; muito devagar, ele perde força para subir.
- **B (amarelo):** o piloto salta de paraquedas antes da batida. O avião sem piloto explode, e você segue no próximo avião. Cada partida tem 3 aviões.
- Bater sem saltar encerra a partida.
- **No computador:** setas ou W/S sobem e descem, Espaço ou J acelera, K ou B salta, P pausa.

**Pontos:** 1 por metro, 25 por estrela, 100 por piloto salvo e 150 por caverna atravessada. O recorde fica salvo no aparelho.

## Como o código está organizado (`index.html`)

1. **Estilo (CSS):** cores em variáveis no `:root`, HUD, analógico (`.stick`), botões A/B (`.gp`) e painéis (menu, fim de jogo, pausa, "gire o celular").
2. **Constantes no topo do script:** `GY` (linha do chão), `RUNWAY` (tamanho da pista), `LIFT_SPEED`, `SEASON_LEN` (700 m por estação), `DAY_LEN` (90 s por dia), `LIVES` (3 aviões).
3. **Sprites:**
   - `PLANE_OPS` e `PILOT_OPS` desenham o avião 30×20.
   - `PLANES` define as três cores (vermelho, azul, amarelo).
   - `BIRD`, `BAT`, `BALLOONS`, `STAR`, `SUN` e `MOON` são os outros desenhos.
   - Cada letra nas listas de pixels é uma cor da paleta.
4. **Céus e estações:**
   - `SKY_DAY`, `SKY_DUSK` e `SKY_NIGHT` são os degradês do céu.
   - `SEASONS` guarda as cores de grama, colinas, árvores e montanhas de cada estação.
5. **Som:** objeto `Snd`, com sons gerados na hora pelo Web Audio (motor, estrela, salto, explosão, estação).
6. **Obstáculos:**
   - `spawnAt` cria montanhas, pássaros, balões e estrelas.
   - `makeCave` cria cavernas, com `caveCenter`, `caveAt` e `caveSpike` para o túnel e as estalactites.
   - `collide` testa as batidas.
7. **Explosões e partículas:** `explode`, `feathers` e `sparkle`.
8. **Salto de paraquedas:** `eject`, `updateEject` e `respawn`.
9. **Lógica principal:** `update(dt)` cuida da física, velocidade, decolagem e colisões. `updateWeather` faz neve, folhas, pétalas e vaga-lumes.
10. **Desenho:** `draw()` desenha, em ordem, céu, sol/lua/estrelas, montanhas ao fundo, colinas com árvores, cenário, chão, cavernas e montanhas, obstáculos, avião, luz da noite e partículas.
11. **Interface e controles:**
    - `showBanner` mostra os avisos grandes e `showOver` a tela de fim.
    - O analógico e os botões usam multitoque com pointer events; o teclado também funciona.

## Ideias para as próximas versões

- Chefões ou chuva de meteoros em certas distâncias.
- Loja de aviões, desbloqueados com as estrelas.
- Combustível que precisa ser recolhido no caminho.
- Músicas de fundo diferentes para cada estação.
- Placar de recordes com o nome do jogador.
