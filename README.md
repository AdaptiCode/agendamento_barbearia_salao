# Demo — Agendamento para barbearia e salão

Projeto demonstrativo da Adapti Code (HTML único, sem dependências além das fontes do Google). Simula o fluxo de agendamento; nada é salvo e todos os dados são fictícios.

Publicar: qualquer hospedagem estática. Mantenha `noindex` em demos e prévias.

---

## 🎛️ Prévia personalizada para o cliente

Esta demo tem um editor embutido para montar, em minutos, uma prévia com a cara do negócio do cliente.

1. Abra a demo publicada com **`?editar`** no final do endereço (ex.: `https://seu-dominio/?editar`). O editor só aparece para você; o visitante comum não vê nada. Para desligar: `?editar=0`.
2. Troque **logo, nome, subtítulo, cor, WhatsApp, Instagram, endereço, horários de atendimento, serviços e equipe**. Os horários mudam de verdade os dias e os horários disponíveis no agendamento.
3. Em **Prévia para o cliente**, informe o nome do cliente e a validade. A prévia mostra uma faixa "PRÉVIA · não é a entrega final" (contrato, cláusula 5.3) e esconde os avisos de demonstração.
4. Envie ao cliente:
   - **Copiar link**: gera um endereço com tudo que você configurou (sem precisar publicar nada novo).
   - **Baixar HTML**: arquivo único com a prévia, pronto para hospedar ou enviar.

O que você edita fica salvo só no seu navegador; use **Restaurar** para voltar ao padrão da demo.

### Ordem do agendamento

- **Barbearia e salão:** profissional primeiro, depois o serviço (só os que aquele profissional faz) e o horário.
- **Dentista e estética:** serviço primeiro, depois o profissional (só quem faz aquele serviço) e o horário.
- Nos dois casos há **"Sem preferência"** (fica com o primeiro profissional livre) e o **horário vem por último**, calculado pela duração do serviço e pela agenda de quem atende.
- Dá para inverter a ordem no editor, em *Serviços e equipe → Ordem do agendamento*.

### Formato dos campos de texto (um por linha)

- Serviços: `Nome | duração | preço` (ex.: `Corte | 30 min | R$ 45`)
- Equipe: `Nome | especialidade | serviços que faz | foto (link) | WhatsApp`. Em "serviços que faz", separe por vírgula usando os mesmos nomes da lista de serviços; vazio = faz todos. Foto e WhatsApp são opcionais; sem foto aparece a inicial do nome.
- Sem nenhuma pessoa na equipe, a etapa de profissional some.

### Confirmação pelo WhatsApp do profissional

Se o profissional tiver WhatsApp cadastrado (ou, na falta dele, o WhatsApp do negócio no editor), o botão **Confirmar e enviar no WhatsApp** abre a conversa com ele já com a mensagem pronta (cliente, telefone, serviço, profissional, data, horário, observações e um código `AG-…`). Com "Sem preferência", vale o número de quem foi atribuído ao horário. O agendamento só chega ao profissional quando o cliente toca em enviar no WhatsApp. Sem nenhum número configurado (demo pura), nada é aberto e a tela final só mostra a mensagem de exemplo.

