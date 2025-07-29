# 🚀 Apache DevLake + GitHub Codespaces

Este repositório oferece uma configuração pronta de Apache DevLake com Grafana em um ambiente GitHub Codespaces, permitindo que você comece a analisar métricas de desenvolvimento de software em minutos.

## 📋 Índice
- [Sobre o Projeto](#-sobre-o-projeto)
  - [O que são métricas DORA?](#o-que-são-métricas-dora)
- [Pré-requisitos](#️-pré-requisitos)
- [Como Usar](#-como-usar)
- [Configurar DevLake](#️-configurar-devlake)
- [Visualizando Métricas](#-visualizando-métricas)
- [Desenvolvimento Local](#-desenvolvimento-local)
- [Solução de Problemas](#-solução-de-problemas)
- [Recursos Adicionais](#-recursos-adicionais)

## 🔍 Sobre o Projeto

Apache DevLake é uma plataforma de análise de dados que coleta, integra e analisa dados de ferramentas de desenvolvimento de software para gerar métricas DORA e outros insights. Este projeto automatiza a configuração do DevLake e Grafana em um ambiente Codespaces ou em sua máquina local.

### O que são métricas DORA?

As métricas DORA (DevOps Research and Assessment) são quatro indicadores-chave que ajudam a medir o desempenho de equipes de desenvolvimento:

1. **Lead Time for Changes**: Tempo médio entre o primeiro commit e a implantação em produção
2. **Deployment Frequency**: Frequência com que implantações são feitas em produção
3. **Change Failure Rate**: Percentual de implantações que resultam em falha
4. **Time to Restore**: Tempo médio para restaurar o serviço após uma falha

Este projeto configura um ambiente completo para coletar, analisar e visualizar essas métricas a partir de seus repositórios GitHub.

## ⚙️ Pré-requisitos

- Conta GitHub
- Acesso a GitHub Codespaces (disponível em todos os planos, incluindo o gratuito)
- Token de acesso pessoal do GitHub com permissões read:org, read:user, repo

## 📊 Visualizando Métricas

Após a configuração e coleta de dados, você pode visualizar as métricas DORA no Grafana:

1. Acesse o Grafana em http://localhost:3002
   - Usuário padrão: `admin`
   - Senha padrão: `admin`

2. Navegue até o dashboard "DORA Metrics Overview"
   - Este dashboard inclui visualizações das quatro métricas DORA principais:
     - Lead Time for Changes (tempo de entrega)
     - Deployment Frequency (frequência de implantação)
     - Change Failure Rate (taxa de falha de mudanças)
     - Time to Restore (tempo para restauração)

3. O dashboard é atualizado automaticamente à medida que o DevLake coleta novos dados

### Acesso às Interfaces

Independente da opção escolhida, acesse:
- **DevLake UI**: http://localhost:8080 - Interface principal para configuração
- **DevLake Config UI**: http://localhost:4000 - Interface de configuração simplificada  
- **Grafana**: http://localhost:3002 - Dashboards e visualizações (admin/admin)
- **MySQL**: localhost:3306 - Banco de dados (usuário: merico, senha: merico)

## �🔧 Solução de Problemas

- **Portas não acessíveis**: Verifique se as portas estão encaminhadas corretamente no Codespaces (Painel inferior > PORTS)
- **Falha na inicialização**: Verifique os logs do docker compose executando `docker compose logs` no terminal
- **Token do GitHub não configurado**: Certifique-se de adicionar um token válido no arquivo `.env`
- **Serviços não iniciam**: Verifique logs específicos com `docker compose logs devlake` ou `docker compose logs grafana`
- **Dashboard não aparece no Grafana**: Verifique se o datasource MySQL está configurado corretamente

## 📚 Recursos Adicionais

- [Documentação oficial do Apache DevLake](https://devlake.apache.org/docs/)
- [Guia de métricas DORA](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance)
- [GitHub Codespaces docs](https://docs.github.com/pt/codespaces)
- [Como criar um token do GitHub](https://docs.github.com/pt/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
- [Documentação dos dashboards DORA](https://devlake.apache.org/docs/Dashboards/DORA)

### Como iniciar este exercício

Simplesmente copie o exercício para sua conta.

[![](https://img.shields.io/badge/Copiar%20Exercício-%E2%86%92-1f883d?style=for-the-badge&logo=github&labelColor=197935)](https://github.com/new?template_owner=dev-pods&template_name=dora-metrics-with-devlake-for-github&owner=%40me&name=metricas-dora-com-devlake-para-github&description=Exercício:+Configuração+pronta+de+Apache+DevLake+com+Grafana+em+um+ambiente+GitHub+Codespaces&visibility=public)
