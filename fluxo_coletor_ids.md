
# Fluxo Auxiliar – Coletor de IDs (Telegram Bot)

Este fluxo tem como objetivo **identificar o ID de usuário do Telegram** de pessoas que interagem com o bot auxiliar de upload, garantindo que apenas um usuário autorizado possa enviar arquivos ao repositório.

---

## 📌 Descrição Geral

- **Nome do fluxo:** `Coletor de Ids (Fluxo Auxiliar)`
- **Plataforma:** n8n
- **Finalidade:** Captura o ID de qualquer pessoa que envie mensagem ao bot, e envia uma mensagem personalizada com o ID.
- **Uso pretendido:** Permitir o cadastro desse ID como autorizado no fluxo principal de upload de arquivos para o repositório Veggi.

---

## 🔧 Como funciona

1. **Trigger:** Um nó `Telegram Trigger` escuta qualquer tipo de mensagem recebida no bot.
2. **Execução:** O ID do usuário é extraído da mensagem recebida automaticamente.
3. **Resposta:** O bot responde ao usuário com uma mensagem no formato:
   ```
   Seu ID de usuário é: 123456789
   Envie esse ID ao responsável pelo sistema para que seu acesso seja liberado.
   ```

---

## 🛡️ Segurança

Este fluxo **não restringe o uso por ID**, pois sua função é justamente identificar o ID de qualquer usuário. A restrição por ID será aplicada no **fluxo principal de upload**.

---

## 💡 Observação

- Você pode utilizar esse fluxo como base para validar novos IDs ou fazer testes.
- É recomendável manter esse bot auxiliar ativo apenas enquanto estiver cadastrando novos usuários.

---

## 🗂️ Histórico

- **Data de criação:** Agosto/2025
- **Responsável:** Nathália Vegi
- **Empresa:** Confecção Veggi
