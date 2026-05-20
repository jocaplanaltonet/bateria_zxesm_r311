# Script para criar o README.md linha por linha
linhas = [
    "# Monitoramento de Baterias ZTE ZXESM R311\n\n",
    "Repositório centralizado para o monitoramento de infraestrutura de baterias **ZTE ZXESM R311**. Este projeto contém as definições de templates para o Zabbix e os dashboards correspondentes para o Grafana.\n\n",
    "## 🏗 Estrutura do Repositório\n\n",
    "```text\n",
    ".\n",
    "├── grafana/             # Dashboards e assets visuais\n",
    "│   ├── dashboard.json   # Export do dashboard\n",
    "│   └── *.png            # Prints de configuração e visão geral\n",
    "├── zabbix/              # Definições de monitoramento\n",
    "│   └── 7.4/             # Templates compatíveis com Zabbix 7.4\n",
    "│       └── *.yaml       # Arquivos de importação de templates\n",
    "└── README.md            # Documentação principal\n",
    "```\n\n",
    "## 🛠 Ambientes Compatíveis\n\n",
    "| Sistema | Versão |\n",
    "| :--- | :--- |\n",
    "| **Grafana** | v13.0.1+security-01 (9bbe672d) |\n",
    "| **Zabbix** | 7.4 |\n\n",
    "## 🚀 Como utilizar\n\n",
    "### Para Zabbix (Monitoramento)\n",
    "1. Navegue até a pasta `zabbix/7.4/`.\n",
    "2. Importe o arquivo `template_BATERIA_ZXESM_R311.yaml` no seu Zabbix Server.\n",
    "3. Vincule o template aos hosts de bateria correspondentes.\n\n",
    "### Para Grafana (Visualização)\n",
    "1. Importe o arquivo JSON localizado em `grafana/`.\n",
    "2. Certifique-se de que a variável `$HOSTNAME` esteja configurada corretamente.\n\n",
    "## 📝 Documentação Detalhada\n",
    "* [Documentação do Dashboard (Grafana)](grafana/README.md)\n",
    "* [Documentação do Template (Zabbix)](zabbix/7.4/README.md)\n\n",
    "---\n",
    "*Projeto desenvolvido para otimização de monitoramento de infraestrutura de rede.*\n"
]

with open("README.md", "w", encoding="utf-8") as f:
    f.writelines(linhas)

print("README.md criado com sucesso!")
