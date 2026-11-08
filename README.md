🎮 Gun Duel Arena — Histórico de Versões e Atualizações
​Documento oficial de versionamento, mecânicas e evolução técnica do projeto Gun Duel Arena — jogo mobile e web de duelos aéreos com recuo vetorial, arquitetura em arquivo único (HTML/JS/Canvas), multiplayer peer-to-peer (WebRTC/MQTT) e pipeline de compilação de APK Android nativo via GitHub Actions e Capacitor.

​📌 Índice de Versões
​v1.0.0 — Fundação do Motor Aéreo e Física de Recuo
​v1.1.0 — Arena Dinâmica, Dificuldade e Economia
​v1.2.0 — Modo Arena com Níveis e Barreiras Destrutíveis
​v2.0.0 — Expansão Tática: Habilidades Ativas, Novas Armas e Upgrades
​v2.1.0 — IA Avançada, Campanha de Chefes e Sobrevivência
​v2.2.0 — Polimento Audiovisual, Replay Slow-Motion e Configurações
​v2.3.0 — Multiplayer Online P2P Serverless a Custo Zero
​v2.4.0 — Pipeline Mobile CI/CD e Build Automático de APK
​v2.5.0 — Identidade Visual Completa: Silhuetas Únicas, +30% Escala e Mapas Procedurais
​[v1.0.0] — Fundação do Motor Aéreo e Física de Recuo
​Versão base de gameplay e validação conceitual.

​🚀 Funcionalidades Principais
​Mecânica de Voo por Disparo: Cada tiro empurra a arma na direção oposta ao cano e aplica impulso vertical para sustentação aérea constante.
​Trampolim Inferior: Eliminação da morte por queda estática; armas quicam com impulso elástico ao tocar a base do mapa.
​Duelos com 10 HP: Cada round exige 10 acertos certeiros para vitória.
​Sistema de Streak Regenerativo: Acertar 5 disparos consecutivos sem sofrer dano regenera automaticamente +1 HP.
​Contagem Regressiva: Introdução do contador 3, 2, 1, DUELO! antes da liberação dos controles a cada round.
​Audio Procedural Web Audio API: Síntese de ondas senoidais, quadradas e triangulares em tempo real para disparos, impactos e quiques, sem dependência de MP3/WAV externos.

​[v1.1.0] — Arena Dinâmica, Dificuldade e Economia
​Evolução de infraestrutura de jogo e menu.
​🛠️ Modificações e Melhorias
​Modo 1 vs 1 Local: Suporte a tela dividida com toques simultâneos na tela ou teclado compartilhado (Espaço e Seta para Cima/W).
​Níveis de Dificuldade de IA:
​Recruta (Fácil): Disparo espaçado e tolerância angular permissiva.
​Veterano (Médio): Mira alinhada com sustentação aérea estável.
​Aimbot (Insano): Previsão vetorial de trajetória balística.
​Obstáculos de Cenário: Barris de TNT explosivos com detonação em área e impulsão física em ambas as armas.
​Economia e Persistência: Recompensas em moedas por rounds e vitórias salvas com segurança no localStorage.
​Limpeza de Cenário: Remoção de ruídos visuais de fundo (teia de aranha/elementos estáticos desnecessários) para foco total na legibilidade da arena.

​[v1.2.0] — Modo Arena com Níveis e Barreiras Destrutíveis
​Transição de partida avulsa para progressão por fases.
​🏰 Novas Funcionalidades
​Modo Arena (Níveis 1 ao 5+): Desbloqueio progressivo de oponentes temáticos salvos no navegador.
​Barreiras Destrutíveis com HP: Obstáculos físicos no ar que exibem rachaduras dinâmicas e estilhaçam ao esgotar a integridade, abrindo linha de tiro direta.
​Habilidades Passivas Desbloqueadas por Nível:
​Salto Turbo (Nível 1): Aumento do impulso vertical por tiro.
​Tiro Perfurante (Nível 2): Projéteis transpassam a primeira barreira destrutível.
​Onda de Choque (Nível 3): Efeito de vento que desestabiliza a mira do rival ao quicar no chão.
​Disparo Duplo (Nível 4): 35% de chance de disparo simultâneo de 2 projéteis.

​[v2.0.0] — Expansão Tática: Habilidades Ativas, Novas Armas e Upgrades
​Reformulação tática do combate competitivo.
​⚡ Habilidades Ativas no HUD (Touch & Teclado)
​Dash Aéreo (Q ou botão na tela): Impulso imediato na direção em que o cano está apontado (cooldown: 6s).
​Granada de Recuo (E ou botão na tela): Projétil explosivo de baixa letalidade (1 HP) com alta propulsão e desestabilização da arma inimiga (cooldown: 8s).
​Escudo Curto (R ou botão na tela): Cúpula energética ativa por 1 segundo que bloqueia 100% dos danos e projéteis (cooldown: 10s).
​Cooldowns Visuais: Animação de preenchimento vertical em tempo real e desativação com feedback cinza durante a recarga.
​🔫 3 Novas Armas no Arsenal
​Lança-Foguetes: Projétil com detonação em raio de 90 px, 2 de dano e forte empurrão.
​Serra Circular: Projétil cortante com capacidade de até 3 ricochetes antes de se extinguir.
​Arma de Gravidade: Singularidade magnética que puxa o oponente em direção ao ponto de impacto.
​📈 Sistema de Upgrades por Arma (3 Níveis cada)
​Menos Recuo (Níveis 1 a 3): Redução cumulativa de até 30% no coice.
​Mais Cadência (Níveis 1 a 3): Aceleração de até 30% na velocidade entre disparos.
​Mais Dano (Níveis 1 a 3): Chance de acerto crítico e ampliação de dano máximo.
​🎨 Personalização Visual e Cosméticos
​Skins de Armas: Clássico Toy, Camuflagem Urbana, Dourado Metálico, Neon Synthwave e Glitch Cósmico.
​Rastos de Projétil: Amarelo Padrão, Laser Azul Elétrico, Fogo Incandescente, Arco-Íris Neon e Plasma Cósmico.
​Substituição de Diálogos: Eliminação total de alert(), confirm() e prompt(); adoção de notificações flutuantes (Toast) não-bloqueantes.

​[v2.1.0] — IA Avançada, Campanha de Chefes e Sobrevivência
​Camada robusta de singleplayer e inteligência artificial.
​🧠 Perfis Comportamentais de IA
​Agressiva: Persegue o jogador, fecha distância com Dash aéreo e atira constantemente.
​Defensiva: Mantém sustentação alta e aciona Escudo imediatamente ao detectar projéteis em rota de colisão próxima.
​Imprevisível: Alterna entre giros bruscos, ricochetes de serras e arremesso repentino de granadas.
​👑 Modo Campanha com 5 Chefes Únicos
​1. Capitão Fuzileiro (12 HP): Disparos contínuos em rajadas e avanço veloz.
​2. Mestre Arquiteto (14 HP): Ergue barreiras temporárias no ar a cada 6 segundos.
​3. Dinamitador Louco (15 HP): Arena com múltiplos barris de TNT, disparos de foguetes e granadas.
​4. Franco Gravitacional (16 HP): Atrai sua arma em direção a armadilhas e ao abismo.
​5. Lorde Supremo da Arena (20 HP): Chefe final com escudo invulnerável periódico e disparos duplos de alta velocidade.
​🌊 Modo Sobrevivência por Ondas
​Ondas consecutivas com escalonamento de vida do rival (+2 HP/onda) e arsenal gradualmente mais letal.
​Registro da maior onda superada com recompensas em moedas.
​🎯 Modo Treino de Tiro
​Arena com alvos esféricos estáticos e alvos oscilantes em trajetória senoidal para calibragem de recuo sem pressão de derrota.
​📜 Missões Diárias e Ranking Local
​Pool de 13 missões com gerador determinístico (3 a 5 missões diárias renovadas à meia-noite do horário local).
​Sistema de Conquistas locais com medalhas e bonificações.
​Tabela de classificação local salvando sequências de vitórias e melhores tempos contra chefes.

​[v2.2.0] — Polimento Audiovisual, Replay Slow-Motion e Configurações
​Elevação da experiência de usuário e estabilização de framerate.
​✨ Recursos de Polimento
​Trilha Sonora Adaptativa: Síntese procedural de arpejos que acelera dinamicamente (110 BPM → 145 BPM) em tom de urgência (Danger Mode) quando qualquer jogador chega a 3 HP ou menos.
​Replay em Câmera Lenta (Killcam Slow-Mo):
​Buffer circular registrando os últimos 2 segundos de física (120 snapshots).
​Ao finalizar o round, o golpe fatal é exibido a 0.25x da velocidade com vinheta avermelhada e indicador ● REC SLOW-MOTION REPLAY.
​Vibração Tátil Háptica: Feedback no celular via navigator.vibrate com pulsos distintos para disparos leves, acertos críticos e explosões de TNT.
​Menu de Configurações:
​Ajuste de volume geral (0% a 100%).
​Ativação/desativação de vibração.
​Sensibilidade de giro da arma (0.5x a 1.8x).
​Exclusão de progresso com confirmação em duas etapas na própria interface.
​Física Normalizada com Delta Time (dt): Taxa de atualização estável independente da frequência da tela (60Hz, 90Hz, 120Hz).
​Teto Estrito de Partículas: Limite rígido de 75 partículas simultâneas (pooling discard) para garantir 60 FPS estáveis em aparelhos modestos.

​[v2.3.0] — Multiplayer Online P2P Serverless a Custo Zero
​Conectividade multijogador sem servidor dedicado e sem custos mensais.
​🌐 Arquitetura P2P Implementada
​Canal de Dados WebRTC (RTCDataChannel): Comunicação peer-to-peer direta entre navegadores sem intermediários para posições, tiros e habilidades a 20 Hz com interpolação linear local.
​Sinalização Serverless com MQTT Nativo: Cliente MQTT 3.1.1 puro em JavaScript (MiniMqttClient), utilizando broker público WebSocket seguro (wss://broker.emqx.io:8084/mqtt) apenas nos primeiros segundos para troca de SDP (Offer/Answer) e candidatos ICE.
​STUN Público Google: Uso de stun:stun.l.google.com:19302 para NAT Traversal gratuito.
​Salas com Código de 4 Dígitos: Sistema de pareamento simples (Criar Sala Privada / Entrar com Código).
​Timeouts de Segurança: Limpeza de buffers e retorno suave ao menu em caso de desconexão ou desistência do oponente.

​[v2.4.0] — Pipeline Mobile CI/CD e Build Automático de APK
​Empacotamento completo para ecossistema Android nativo.
​📱 Automação e Empacotamento
​Capacitor 6: Empacotamento do arquivo HTML/JS consolidado em aplicação nativa Android.
​GitHub Actions Workflow (build-apk.yml):
​Execução automatizada em máquina virtual Ubuntu.
​Setup de Node 20, Java 17 e Android SDK nativo.
​Script Python com Pillow integrado na esteira de compilação para gerar todos os tamanhos de ícone mipmap (mdpi, hdpi, xhdpi, xxhdpi, xxxhdpi) a partir de resources/icon.png.
​Resolução definitiva de erros de cabeçalho corrupto (too many text chunks) e dependência desnecessária de telas de splash.
​Geração de artefato compilado pronto para download (GunDuelArena-debug.apk).

​[v2.5.0] — Identidade Visual Completa: Silhuetas Únicas, +60% Escala e Mapas Procedurais
​Versão atual estável de produção.
​🔍 Detalhamento das Alterações
​1. Silhuetas Distintas e Reconhecíveis por Classe de Arma
​Todas as armas receberam renderização vetorial única preservando o acabamento chunky/toy:
​Pistola Básica: Modelo clássico com slide compacto, ressalto frontal e duas ranhuras diagonais (//).
​Magnum .44: Cano longo reforçado com ressalto superior, tambor cilíndrico ranhurado com câmaras aparentes e cabo anatômico curvado.
​Escopeta Pump: Cano duplo largo e espesso, telha inferior de armar (pump) estriada e coronha compacta.
​Fuzil Automático: Perfil alongado, quebra-chamas estriado na boca, mira militar elevada, coronha retangular e carregador curvo (banana mag).
​Canhão Laser: Carcaça futurista angular com dissipadores de calor em aleta no topo e núcleo energético central translúcido.
​Lança-Foguetes (RPG): Tubo cilíndrico pesado, cone de exaustão traseiro, punho duplo e ogiva de foguete saliente na ponta.
​Disparador de Serra: Carcaça mecânica com guia e disco denteado giratório exposto na frente.
​Arma de Gravidade: Receptor central com esfera pulsante violeta cercada por pontas magnéticas bifurcadas frontais.
​2. Aumento de 30% na Escala das Armas
​Escala de Desenho: Aplicação de ctx.scale(this.squashX * 1.3, this.squashY * 1.3).
​Caixa de Colisão Proporcional: Raio de colisão física aumentado de 22 px para 28 px.
​Muzzle Distance Recalibrada: Distância de saída das balas ajustada para 36 px, garantindo emissão correta na ponta dos canos ampliados.
​Cúpula de Escudo Aumentada: Raio da bolha energética ampliado para 46 px para cobertura total da arma.
​3. Geração Procedural e Aleatória de Mapas
​A arena agora reconstrói layouts aleatórios a cada round ou partida nos modos Solo, Sobrevivência, Campanha e Local/Online, alternando entre 5 arquétipos dinâmicos:
​SPLIT_ISLANDS: Ilhas suspensas com alturas assimétricas e vão central livre para duelos aéreos.
​VERTICAL_BUNKER: Plataforma intermediária central com coberturas laterais protegidas.
​FLOATING_CROSS: Três plataformas escalonadas em padrão piramidal.
​STAGGERED_PLATFORMS: Três a quatro barreiras geradas aleatoriamente em largura e altura.
​CENTRAL_FORTRESS: Grande ilha central acompanhada de coberturas superiores elevadas.
​Distribuição Dinâmica de TNT: Barris explosivos distribuídos aleatoriamente entre as plataformas disponíveis a cada round.
​Modo Treino Preservado: Arena de treino mantém pista estável com alvos móveis e fixos.
​4. Estabilidade do Motor
​Polyfill de roundRect incorporado no canvas para total retrocompatibilidade com WebViews antigas do Android.
​Suporte a densidade de pixels (devicePixelRatio até 2x) para nitidez sem distorção em telas móveis de alta densidade.
​Sistema de pausa com botão ⏸, atalhos Esc/P e suspensão de contexto WebAudio durante segundo plano.
​📂 Estrutura do Projeto para Compilação de APK