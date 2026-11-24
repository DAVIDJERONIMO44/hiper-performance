# HIPER PERFORMANCE 1.1 — PUBLICAÇÃO

PWA estático, offline, sem autenticação nem servidor. **Este repositório NÃO deve conter fichas pessoais, links originais, nem backups.**

## Publicar pelo GitHub Pages
1. Extraia o ZIP `HIPER-PERFORMANCE-v1.1-PUBLICACAO.zip`.
2. Envie os arquivos **diretamente para a raiz** da branch `main` do repositório `DAVIDJERONIMO44/hiper-performance` (não envie a pasta contêiner).
3. Acesse Settings > Pages > Deploy from a branch > `main` / `(root)` > Save.
4. Abra `https://davidjeronimo44.github.io/hiper-performance/`.
5. Na primeira abertura, importe localmente `HIPER-PERFORMANCE-FICHAS.json` pelo botão **Importar fichas privadas**. Não publique esse arquivo no GitHub. A importação só precisa ser feita uma vez por instalação/dispositivo/navegador.
6. Instale no Android (Chrome > menu > Instalar aplicativo) ou no iPhone (Safari > Compartilhar > Adicionar à Tela de Início).
7. Após a primeira abertura com internet, teste a abertura do PWA em modo avião e faça um backup pela área Histórico.

## Persistência, privacidade e atualização
- Um único banco IndexedDB `hiper-performance`, versão 2, com lojas `state` (registros) e `programs` (fichas privadas). Atualizações da aplicação não apagam dados locais nem exigem nova importação de fichas.
- Backups em JSON exportam **fichas e histórico juntos**, para recuperação em outros dispositivos. Guardar em local privado. Restauro substitui os dados do aplicativo após confirmação.
- Limpar dados do site, usar navegação anônima, trocar de navegador/dispositivo, ou remover dados pelo sistema operacional pode apagar a instalação local. Faça backup periodicamente.
- Para futuras fases, importe um novo arquivo privado validado; não é necessário alterar o aplicativo nem perder o histórico.
- Os dados e links importados nunca são enviados automaticamente para o GitHub. Abrir manualmente um vídeo externo é uma ação de navegação do usuário.
- A versão 1.1 mantém as quatro fichas da Fase 01. Fases posteriores ficam bloqueadas enquanto não forem validadas.

## Homologação
Os testes automatizados cobrem a importação, recuperação da sessão, persistência, importação única, backup/restauração, navegação offline, rotação e preservação dos dados após atualização de arquivos. Teste em aparelho real antes de substituir a ficha física.

## Histórico de decisões
- 1.0: versão protótipo com fichas e links dentro da publicação.
- 1.1: separação obrigatória dos dados privados, importação IndexedDB, backup autocontido, base de publicação `/hiper-performance/`, atualização do Service Worker sem limpar o banco.
- Sem Supabase, Resend, login, backend, domínio pago ou custos contratados.
