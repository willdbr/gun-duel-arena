# AeroGuns 🚀🔫

**AeroGuns** é um jogo arcade frenético de duelo tático 2D, onde a física de recuo (*recoil*) e a gravidade são as ferramentas principais de movimentação e combate. Desenvolvido em **HTML5 Canvas** e **JavaScript** num ficheiro único e portado nativamente para **Android** através de **Capacitor**, o jogo é compilado automaticamente via **GitHub Actions**.

---

## 🎮 Modos de Jogo

* **Duelo Solo:** Enfrente bots com perfis táticos dinâmicos (Agressiva, Defensiva e Imprevisível) e 3 níveis de dificuldade (Fácil, Médio e Insano).
* **Modo Campanha (6 Chefes):** Enfrente chefes com truques exclusivos:
  1. *Capitão Fuzileiro:* Rajada contínua e dashes ofensivos.
  2. *Mestre Arquiteto:* Criação periódica de barreiras defensivas.
  3. *Dinamitador Louco:* Foguetes pesados e chuva de barris TNT.
  4. *Franco Gravitacional:* Vórtice atrator que puxa a arma para o chão.
  5. *Lorde Supremo da Arena:* Escudo supremo e lasers duplos.
  6. *Franco-Atirador Sombra:* Camuflagem fantasma após o dash e tiros perfurantes.
* **Sobrevivência:** Ondas contínuas com vida e armamento inimigo escalonados, contando com **cartas aleatórias de reforço de arsenal** gratuitas entre as ondas.
* **Modo Treino:** Prática com alvos fixos e móveis senoidais com feedback de acertos.
* **1 vs 1 Local:** Ecrã dividido para dois jogadores disputarem no mesmo dispositivo.
* **Multiplayer Online P2P (Custo Zero):** Conexão direta entre jogadores via WebRTC com troca de sinalização através de broker MQTT seguro.

---

## ⚡ Arsenal e Habilidades

### Armas Disponíveis
* **Pistola Básica:** Ágil e equilibrada com ranhuras duplas.
* **Magnum .44:** Impacto pesado com tambor cilíndrico ranhurado.
* **Escopeta Pump:** Dispersão em cone com 3 bagos e choque cinético.
* **Fuzil Automático:** Cadência contínua com coronha tática.
* **Canhão Laser:** Feixes de alta velocidade e núcleo energético visível.
* **Lança-Foguetes (RPG):** Projétil com cone traseiro e dano em área.
* **Serra Circular:** Lâminas denteadas compactas com 3 ricochetes nativos.
* **Arma de Gravidade:** Pontas bifurcadas e esfera magnética violeta.

### Habilidades Ativas
* **Dash (Tecla Q):** Impulso cinético rápido na direção apontada pela arma.
* **Granada (Tecla E):** Projétil temporizado que causa concussão e dano em área.
* **Escudo (Tecla R):** Campo de força esférico que anula todo o dano recebido por 1 segundo.

---

## 🛠️ Histórico de Versões e Atualizações

### v1.0 — Fundação do Motor
* Implementação do motor de física com sub-stepping e taxa delta normalizada para 60 FPS.
* Sistema de colisões elásticas contra paredes, teto e trampolim inferior de alta restituição.
* Sintetizador sonoro procedural adaptativo via Web Audio API com modo de perigo (*Danger Mode* quando HP <= 3).

### v1.5 — Modos Avançados & Multiplayer P2P
* Integração de IA tática (perfis Agressiva, Defensiva e Imprevisível).
* Sistema de replay dos últimos 2 segundos em câmara lenta (*Slow-Mo Killcam*).
* Arquitetura P2P sem custos de servidor utilizando WebRTC e sinalização leve MQTT.
* Sistema de missões diárias com persistência local em `localStorage`.

### v2.0 — Portabilidade Mobile & Pipeline CI/CD
* Empacotamento para Android utilizando Capacitor 6.
* Configuração da pipeline de integração e compilação contínua no GitHub Actions para geração do `.apk`.
* Polyfill robusto de `roundRect` para compatibilidade total com o Android WebView.
* Suporte nativo para taxas de densidade de píxel elevada (DPR retina) e áreas seguras (*safe-area-inset*).

### v2.5 — Reformulação Visual, Balanceamento & Mecânicas
* **Escala das Armas:** Aumento da escala visual das armas para 1.6x (+60%) com ajuste no raio de colisão (`radius: 35`) e ponto de disparo (`muzzleDist: 45`).
* **Mapas Procedurais Balanceados:** Geração focada em apenas **uma barreira central** (sólida, móvel ou de vidro destrutível) acompanhada de barril TNT, eliminando bloqueios de passagem aérea.
* **Mecânicas Especiais:**
  * Dano crítico de 3 HP direto com aviso dourado e vibração tátil.
  * 20% de hipótese aleatória de ricochete triplo para qualquer tiro disparado.
  * Janela de seleção de upgrade gratuito entre ondas no Modo Sobrevivência.
* **Polimento da Interface:**
  * Remoção de emojis dos botões de navegação.
  * Título reposicionado próximo ao topo do ecrã.
  * Simulação contínua e suave em segundo plano (*Attract Mode*) no menu principal.
  * Botão "Sair do Jogo" com diálogo de confirmação e encerramento seguro.
* **Edição de Desenvolvimento (Dev Build):** Painel interno com Modo Deus (Invencibilidade), Cooldown Zero, Instakill, Cadência Insana, Flutuação Lunar e visualizador de hitboxes em tempo real.
