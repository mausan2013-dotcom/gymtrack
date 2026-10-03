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

## Compatibilidade
Usa as mesmas chaves de armazenamento da versão anterior (`gymtrack_*_v1`).
Publicada no mesmo endereço (domínio da Adapta), lê os dados existentes sem precisar migrar.
Em outro endereço, os dados antigos não aparecem: exporte o backup lá e importe no novo.

## Próximas etapas
2. Carga/reps da última vez pré-preenchidas, sugestão de progressão, tipos de exercício e de série
3. Volume semanal por músculo, gráficos de 1RM e período
4. Restante da lista (biblioteca de exercícios, fotos, modo claro, Apple Saúde...)
