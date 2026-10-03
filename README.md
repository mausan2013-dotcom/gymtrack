# GymTrack — app de treino (PWA para iPhone)

## Arquivos
- `index.html` — o app inteiro (funciona sozinho)
- `manifest.webmanifest`, `sw.js`, `icon-*.png` — instalação e uso offline (só fazem efeito em hospedagem própria com HTTPS)
- `versao-original/` — cópia da versão da Adapta antes das mudanças

## Versão 2.0 — etapa 1 (02/10/2026)
- Sem dados inventados: o app começa vazio e oferece remover os exemplos que a versão anterior gravou
- Perfil editável (altura, peso inicial, meta, data alvo, treinos/semana, descanso padrão), IMC e ritmo necessário
- Sequência em semanas (meta de treinos por semana), contagem de segunda a domingo
- Recordes por 1RM estimado (Epley) e só com séries marcadas como feitas
- "Última vez" pega o treino mais recente de verdade
- Timer de descanso pelo horário de término: continua certo com a tela bloqueada e após fechar o app
- Planos ligados ao histórico por id (renomear não quebra a sequência)
- Finalizar treino: avisa séries não marcadas e mostra resumo (duração, séries, volume, recordes)
- Backup: exportar/importar JSON (no iPhone abre "Salvar em Arquivos")
- PWA: ícone, tela cheia, aviso de instalação, pedido de armazenamento persistente, offline

## Versão 2.1 — etapa 2 (02/10/2026)
- Séries pré-preenchidas com a carga e as reps da última sessão de cada exercício (inclui aquecimentos)
- Sugestão de progressão (dupla progressão): bateu as reps alvo em todas as séries → sobe a carga; botão "Aplicar"
- Tipos de exercício: com carga, peso corporal (carga extra opcional) e por tempo (segundos)
- Tipos de série: aquecimento (A), drop (D), até a falha (F) — aquecimento fica fora de recordes, volume e progressão
- Passo do +/− conforme o equipamento: halteres 2 kg, máquinas 5 kg, leg press 10 kg, barras 2,5 kg
- Menu ⋯ por exercício: nota fixa, descanso próprio (salvo no plano), mover, remover
- Biblioteca com ~55 exercícios e busca (sem acento); criar exercício novo com músculo e tipo
- Editor de planos com tipo, descanso e autocompletar pela biblioteca
- Tela sempre acesa durante o treino (iOS 16.4+)
- Recordes por tipo (1RM estimado, reps ou segundos); notas entram no backup

## Compatibilidade
Usa as mesmas chaves de armazenamento da versão anterior (`gymtrack_*_v1`).
Publicada no mesmo endereço (domínio da Adapta), lê os dados existentes sem precisar migrar.
Em outro endereço, os dados antigos não aparecem: exporte o backup lá e importe no novo.

## Próximas etapas
3. Volume semanal por músculo, gráficos de 1RM e período
4. Restante da lista (biblioteca de exercícios, fotos, modo claro, Apple Saúde...)

## Publicação
- Endereço: https://mausan2013-dotcom.github.io/gymtrack/
- Repositório: github.com/mausan2013-dotcom/gymtrack (cópia local em ~/Developer/gymtrack)
- Para publicar mudanças: `publica-gymtrack "o que mudou"` no Terminal
