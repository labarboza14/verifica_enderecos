# 🧭 Verifica Endereços — Correção automatizada de dados com Python

Este projeto foi criado com carinho e propósito: ajudar pessoas e equipes que trabalham com bases de dados endereçáveis (Excel) a **verificar, corrigir e padronizar informações como CEP, cidade, UF, bairro e logradouro** automaticamente, usando APIs públicas como o ViaCEP.

📍 Ideal para quem lida com cadastros, atendimento ao cliente, logística, pré-vendas, auditoria de dados e até análises geográficas.

---

## ✨ O que este script faz?

✅ Verifica o **CEP** de cada linha da planilha, consultando dados atualizados diretamente da API do ViaCEP.  
🔄 Caso o CEP seja inválido ou ausente, tenta buscar o endereço com base no **UF + Cidade + Logradouro**.  
🛠️ Atualiza os campos corrigidos e marca visualmente na planilha os dados alterados.  
🧽 Remove acentos e padroniza todos os textos para letras maiúsculas.  
💾 Gera automaticamente uma planilha final corrigida e um backup com timestamp.  
🎨 Realça com cor amarela as células modificadas.

---

## 🗂️ Estrutura esperada da planilha de entrada

A planilha deve conter as colunas a seguir:

| Endereço | Numero | Bairro | Cidade | UF | CEP |
|----------|--------|--------|--------|----|-----|

A planilha pode ter mais colunas, sem problema. O script irá focar nessas.

---

## ▶️ Como usar

### 1. Clone este repositório

```bash
git clone https://github.com/labarboza14/verifica_enderecos.git
cd verifica_enderecos
````

### 2. Instale as bibliotecas necessárias

Use um ambiente virtual ou instale direto:

```bash
pip install -r requirements.txt
```

Se ainda não existir o `requirements.txt`, você pode instalar manualmente:

```bash
pip install pandas openpyxl requests
```

### 3. Coloque sua planilha na raiz do projeto

Renomeie sua planilha para:

```
planilhabase.xlsx
```

Ou edite no código a variável `ARQUIVO_ENTRADA` com o nome correto do seu arquivo.

---

### 4. Execute o script

```bash
python verifica_enderecos.py
```

Você verá mensagens de progresso linha por linha.

---

### 5. Veja os resultados

Após rodar o script, serão criados dois arquivos:

* `planilha_corrigida.xlsx` → Planilha principal, corrigida e formatada
* `planilha_corrigida_YYYYMMDD_HHMMSS.xlsx` → Cópia de segurança com timestamp

Campos corrigidos são destacados em amarelo para fácil conferência.

---

## 💡 Por que este projeto existe?

Trabalhar com dados sujos é um desafio em muitas áreas. Eu mesma já vivi a dor de precisar limpar planilhas gigantes manualmente, campo por campo.

Esse projeto nasceu da vontade de **economizar tempo, evitar erros e compartilhar conhecimento** com mais gente que enfrenta os mesmos desafios.

Sinta-se à vontade para usar, adaptar e contribuir!

---

## 🤝 Contribuindo

Se você quiser melhorar esse projeto, adicionar novos recursos (como validação de número, geocodificação, logs detalhados etc.) ou simplesmente compartilhar feedback — **vai ser uma alegria te receber**!

---

## 📬 Dúvidas ou sugestões?

Fique à vontade para abrir uma [issue](https://github.com/labarboza14/verifica_enderecos/issues) ou me chamar diretamente.

---

## 🧑‍💻 Feito com Python, empatia e propósito

Com carinho,
**Gloria Barboza**
💌 [LinkedIn](https://www.linkedin.com/in/labarboza/) | 💻 [GitHub](https://github.com/labarboza14)


