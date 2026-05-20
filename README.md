# Monitoramento de Baterias ZTE ZXESM R311

Repositório centralizado para o monitoramento de infraestrutura de baterias **ZTE ZXESM R311**. Este projeto contém as definições de templates para o Zabbix e os dashboards correspondentes para o Grafana.

## 🏗 Estrutura do Repositório

```text
.
├── grafana/             # Dashboards e assets visuais
│   ├── dashboard.json   # Export do dashboard
│   └── *.png            # Prints de configuração e visão geral
├── zabbix/              # Definições de monitoramento
│   └── 7.4/             # Templates compatíveis com Zabbix 7.4
│       └── *.yaml       # Arquivos de importação de templates
└── README.md            # Documentação principal
```

## 🛠 Ambientes Compatíveis

| Sistema | Versão |
| :--- | :--- |
| **Grafana** | v13.0.1+security-01 (9bbe672d) |
| **Zabbix** | 7.4 |

## 🚀 Como utilizar

### Para Zabbix (Monitoramento)
1. Navegue até a pasta `zabbix/7.4/`.
2. Importe o arquivo `template_BATERIA_ZXESM_R311.yaml` no seu Zabbix Server.
3. Vincule o template aos hosts de bateria correspondentes.

### Para Grafana (Visualização)
1. Importe o arquivo JSON localizado em `grafana/`.
2. Certifique-se de que a variável `$HOSTNAME` esteja configurada corretamente.

## 📝 Documentação Detalhada
* [Documentação do Dashboard (Grafana)](grafana/README.md)
* [Documentação do Template (Zabbix)](zabbix/7.4/README.md)

---
*Projeto desenvolvido para otimização de monitoramento de infraestrutura de rede.*
