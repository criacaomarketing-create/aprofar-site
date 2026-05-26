# Roadmap APROFAR — Próximos passos

Lista de tudo que ficou para o futuro, depois de fechar o básico do básico (site no ar + formulário funcional).

---

## ✅ Já entregue

- Site público redesenhado e no ar (https://aprofar.vercel.app/)
- Deploy automático via GitHub + Vercel
- Formulário de contato funcional via Formspree (recebe e-mails)
- Botão flutuante de WhatsApp
- Design responsivo (celular, tablet, desktop)
- Mensagem de sucesso bonita ao enviar o formulário
- Anti-spam (honeypot)

---

## 🎯 Fase 1 — Finalizar o site público (próximas 2 semanas)

Polimento e dados reais. Tudo aqui é trabalho de **conteúdo**, não de programação.

### Conteúdo real
- [ ] Trocar estatísticas provisórias do hero (30+, 1.000+, 100%) pelos números reais
- [ ] Atualizar textos de missão / visão / valores
- [ ] Confirmar e atualizar endereço, telefone, e-mail
- [ ] Trocar número provisório do WhatsApp pelo real (no código, procurar `5511999999999`)
- [ ] Apontar links de redes sociais reais (Instagram, LinkedIn, Facebook) no rodapé
- [ ] Revisar todos os textos com a diretoria

### Identidade visual
- [ ] Logo real da APROFAR (substituir o "A" provisório)
- [ ] Favicon (ícone da aba do navegador) — usar logo em PNG 32x32
- [ ] Imagem de preview (Open Graph) — aparece quando alguém compartilha o link no WhatsApp
- [ ] Confirmar paleta de cores oficial (atual: verde + azul)

### Domínio
- [ ] Comprar domínio (registro.br → aprofar.org.br, ~R$ 40/ano)
- [ ] Apontar para Vercel (Settings → Domains)
- [ ] HTTPS automático configurado pela Vercel

### Conformidade
- [ ] Página de Política de Privacidade (obrigatória pela LGPD)
- [ ] Aviso de cookies (se usar Analytics)
- [ ] Termos de uso

### Métricas
- [ ] Google Analytics 4 instalado
- [ ] Configurar evento "formulário enviado" no Analytics

---

## 🗂️ Fase 2 — Gestão interna (1 a 3 meses)

A parte que a cliente realmente precisa: organização da operação interna. **Não fica no site público** — fica em ferramentas internas privadas.

### Organização do Drive (pré-requisito de tudo)
- [ ] Criar estrutura de pastas no Drive da APROFAR:
  ```
  APROFAR/
  ├── 01-Associados/        (uma pasta por farmácia)
  ├── 02-Obrigações/        (anuidade, VISA, bombeiros, Anvisa)
  ├── 03-Institucional/
  └── 04-Modelos e Formulários/
  ```
- [ ] Migrar arquivos atuais para essa estrutura

### Planilha de controle (Google Sheets)
- [ ] Aba "Farmácias": CNPJ, razão social, responsável, contato, endereço
- [ ] Aba "Obrigações": cada linha = uma obrigação ligada a uma farmácia, com data de vencimento
- [ ] Formatação condicional: verde (em dia), amarelo (vence em 30 dias), vermelho (vencido)
- [ ] Dashboard: "vence neste mês" / "atrasados" / "total de associados"
- [ ] Compartilhar com diretoria/secretaria — acesso restrito

### Coleta de dados
- [ ] Google Forms para cadastro de novos associados (com upload de documentos)
- [ ] Formulário do site (Formspree) integrado ao processo

### Calendário compartilhado
- [ ] Google Calendar específico da APROFAR
- [ ] Eventos automáticos de vencimento (via Google Apps Script ligado à planilha)
- [ ] Lembrete por e-mail 30/15/7 dias antes

### Treinamento
- [ ] Documentar como usar a planilha e o Drive (passo a passo curto)
- [ ] Treinar a pessoa que vai operar (1-2h de tutorial gravado)

---

## 🔐 Fase 3 — Conectar mundos público + interno (3 a 6 meses)

Quando a fase 2 estiver azeitada, dá pra criar pontes controladas.

### Migrar dados
- [ ] Avaliar mudança de Google Sheets para **Airtable** (mais robusto pra esse caso)
- [ ] Migrar histórico

### Portal do Associado
- [ ] Botão "Área do Associado" no site (login com e-mail + senha)
- [ ] Cada farmácia vê **só os próprios documentos**
- [ ] Histórico de pagamentos da anuidade
- [ ] Solicitação de 2ª via online
- [ ] Atualização de cadastro pela própria farmácia

### Comunicação automatizada
- [ ] E-mail de boas-vindas para novos associados (ferramenta: Mailchimp ou Brevo)
- [ ] Newsletter mensal
- [ ] Aviso automático de vencimento via WhatsApp (Z-API ou Twilio)

### Conteúdo
- [ ] Página de Blog/Notícias no site
- [ ] Página de Eventos com calendário público
- [ ] Galeria de fotos de eventos passados

---

## 🚀 Fase 4 — Sistema próprio (6 meses+, só se necessário)

Para quando a associação crescer ou precisar de funções muito específicas. Aqui sai do "sem código" e entra desenvolvimento real.

- [ ] Sistema de cobrança integrado (Asaas, Pagar.me, Mercado Pago)
- [ ] Boleto/PIX de anuidade emitido automaticamente
- [ ] Emissão de 2ª via de documentos com selo digital
- [ ] Assinatura digital de contratos (ClickSign, D4Sign)
- [ ] App mobile para associados
- [ ] Dashboard analítico com métricas da associação
- [ ] Integração com sistemas governamentais (e-VISA, etc.)

---

## 💡 Ideias soltas para investigar

- Convênios e descontos exclusivos visíveis na área do associado
- Sistema de votação eletrônica para assembleias
- Cursos online (LMS tipo Moodle ou Kajabi)
- Marketplace de fornecedores para os associados
- Programa de indicação ("indique uma farmácia e ganhe…")
- Chatbot no site para dúvidas frequentes
- Página em inglês para parcerias internacionais (provavelmente desnecessário)

---

## ❓ Perguntas pendentes para a cliente

1. Quantas farmácias associadas hoje?
2. Qual o orçamento previsto para o projeto completo?
3. Quem vai operar o sistema interno no dia a dia?
4. Tem prazo apertado por algum evento/assembleia?
5. A pessoa que estava fazendo o site antes — alguém tem contato? O que ela já entregou?
6. Têm logo em alta resolução (vetor, SVG ou PDF)?
7. Qual o e-mail oficial da associação?
8. Querem manter o nome de domínio antigo (se existir) ou criar um novo?

---

## 📌 Decisões importantes a tomar com a cliente

- **Escopo do projeto:** só site institucional OU sistema completo?
- **Orçamento:** quanto a APROFAR pode investir (mensal e total)?
- **Prazo:** entrega faseada ou tudo de uma vez?
- **Operação:** quem mantém depois de entregue?
- **Suporte:** vai ter contrato de manutenção? Por quanto?

---

*Última atualização: 26/05/2026*
