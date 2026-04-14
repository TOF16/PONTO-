# PONTO — Banco de Horas (Técnicos e Analistas)

Sistema web completo para controle de banco de horas: **cadastro de colaboradores**, **registro de ponto**, **cálculo automático de horas extras**, **dashboard com filtros** e **exportação CSV**.

## Versão simples (sem Node e sem banco)
Se você quer algo bem simples para usar imediatamente, abra o arquivo:
- `SIMPLIFICADO.html`

Ele roda direto no navegador, salva os dados no próprio navegador e exporta CSV (também tem backup/importação em JSON).

## Requisitos
- Node.js 20+
- Docker (para o PostgreSQL)

## Subir o banco (PostgreSQL)

```bash
docker compose up -d
```

## Backend (Express)

```bash
cd backend
npm install
npm run db:migrate
npm run dev
```

API em `http://localhost:4000`.

## Frontend (React + Vite)

```bash
cd frontend
npm install
npm run dev
```

App em `http://localhost:5173`.

## Regras implementadas
- **Jornada padrão**: 7h20 de trabalho com **1h de intervalo** (descontada automaticamente no cálculo).
- **Período de apuração**: do dia **15** até o dia **16** do mês seguinte.
- **Domingo**: permite **apenas 1 colaborador** com registro no dia.

