# REINHART: Interactive World

Protótipo de RPG narrativo autoral, construído com React + TypeScript + Tailwind CSS + Vite.

## Rodar no Codex / terminal

1. Abra esta pasta em seu ambiente de desenvolvimento.
2. Instale Node.js 20+.
3. Execute `npm install`.
4. Execute `npm run dev`.
5. Abra o endereço local informado pelo Vite (geralmente http://localhost:5173).
6. Para compilar: `npm run build`.

## Incluído

- Dashboard com contadores reais, jornadas recentes e seis continentes iniciais.
- Editor de personagens com dados iniciais de Reinhart e upload de retrato de até 2 MB.
- Editor de continentes/regiões com estado rascunho ou cânone oficial.
- Editor de episódios com prólogos e etiqueta oficial/alternativo/rascunho.
- Jornadas com histórico de ações, seleção de personagens e episódios, inventário, missões, atributos e memórias editáveis.
- Salvamento local por IndexedDB e exportação/importação de backups JSON.
- Layout responsivo com tema medieval preto e dourado.

## Limitações e segurança

- **IA ainda não está ligada**: ações são registradas, mas não há respostas narrativas geradas por modelo. Não são produzidas respostas fictícias.
- **Sem backend, autenticação nem sincronização**: dados ficam no navegador local. Não há proteção apropriada para hospedagem pública com dados privados.
- Uploads são salvos como data URLs no IndexedDB e no backup; há limites conforme o navegador.
- Combate automatizado, streaming de IA, NPCs autônomos, memória semântica, Supabase e permissões do usuário são próximas etapas.
- Não publique material privado sem implementar autenticação, políticas de segurança e endpoints protegidos.

## Próxima fase de integração segura de IA

Criar API autenticada no servidor, guardar secrets somente no servidor, conectar provedor compatível com API, montar contexto a partir do cânone, resumo da jornada, últimas mensagens e estado dos NPCs, validar atualizações estruturadas e gravar eventos transacionais em PostgreSQL. Nunca armazenar a chave do provedor em frontend/localStorage.
