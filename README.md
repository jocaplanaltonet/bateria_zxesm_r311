Monitoramento de Baterias ZTE ZXESM R311

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
🛠 Ambientes CompatíveisSistemaVersãoGrafanav13.0.1+security-01 (9bbe672d)Zabbix7.4🚀 Como utilizarPara Zabbix (Monitoramento)Navegue até a pasta zabbix/7.4/.Importe o arquivo template_BATERIA_ZXESM_R311.yaml no seu Zabbix Server.Vincule o template aos hosts de bateria correspondentes.Para Grafana (Visualização)Importe o arquivo JSON localizado em grafana/.Certifique-se de que a variável $HOSTNAME esteja configurada corretamente (consulte o README.md dentro da pasta grafana/ para detalhes de ajuste da query).📝 Documentação DetalhadaPara instruções específicas de cada componente, acesse os respectivos diretórios:Documentação do Dashboard (Grafana)Documentação do Template (Zabbix)
