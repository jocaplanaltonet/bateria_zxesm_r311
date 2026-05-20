# Template Zabbix: Bateria ZXESM R311

Este diretório contém a definição do template utilizado para o monitoramento de baterias **ZTE ZXESM R311** via SNMP, compatível com **Zabbix 7.4**.

## 📋 Visão Geral
Este template automatiza a coleta de dados de saúde, carga e estados operacionais das baterias, permitindo que a equipe de infraestrutura identifique falhas e antecipe ações de manutenção.

## 📊 Principais Métricas Monitoradas
* **Tensão e Corrente:** Monitoramento contínuo da tensão de entrada/saída e corrente operacional.
* **Estado de Saúde (SOH) e Carga (SOC):** Métricas em tempo real sobre a degradação e capacidade restante da bateria.
* **Temperatura:** Monitoramento térmico para prevenção de falhas por superaquecimento.
* **Identificação:** Coleta automática do número de série do dispositivo via SNMP.

## ⚠️ Triggers (Alertas)
O template inclui triggers configuradas para notificar eventos críticos, como:
* **Tensões fora do padrão:** Alertas para níveis de tensão alta ou baixa.
* **Proteções acionadas:** Monitoramento de estados críticos (Sobretensão, Subtensão, Aquecimento).
* **Níveis de Carga:** Alertas escalonados por percentual (100%, 75%, 50%, 25%, 5%).
* **Gestão de Garantia:** Alerta automático disparado 30 dias antes do vencimento da garantia (baseado na data de ativação).

## ⚙️ Macros de Configuração
As macros abaixo podem ser ajustadas no nível do Host para customizar o comportamento dos alertas:

| Macro | Valor Padrão | Descrição |
| :--- | :--- | :--- |
| `{$TEMPLATE_THRESHOLD100}` | 100 | Bateria 100% carregada |
| `{$TEMPLATE_THRESHOLD25}` | 25 | Bateria com 25% da carga |
| `{$STATUS_3}` | 3 | Estado: Bateria Off-line |

## 🛠 Requisitos de Instalação
1. **SNMP:** Certifique-se de que o dispositivo esteja configurado com a *Community* SNMP correta no Zabbix.
2. **Importação:**
   - Acesse **Configuração** > **Templates** > **Importar**.
   - Selecione o arquivo `template_BATERIA_ZXESM_R311.yaml`.
   - Clique em **Importar**.
3. **Associação:** Vincule este template aos hosts correspondentes em sua infraestrutura.

## 📁 Estrutura do Arquivo
* `template_BATERIA_ZXESM_R311.yaml`: Arquivo principal com a configuração completa de Itens, Triggers, Gráficos e Macros.
