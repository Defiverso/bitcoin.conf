# Bitcoin Core Optimized Config (`bitcoin.conf`)

Este repositório contém um arquivo de configuração (`bitcoin.conf`) otimizado para rodar um **Node do Bitcoin Core**.

## 🛠 Como usar

### Pré-requisitos
Ter o Bitcoin Core instalado. 

### Instalação

Clone este repositório ou baixe o arquivo `bitcoin.conf` disponível aqui.

Copie o arquivo para o seu diretório de dados.

---

## 📝 Detalhes Técnicos do Arquivo

| Parâmetro | Valor | Descrição |
| --- | --- | --- |
| `dbcache` | `8000` | Aloca 8GB de RAM para o banco de dados. Ajuste para metade da sua RAM total se necessário. |
| `par` | `-1` | Usa todos os threads do CPU. Melhora a velocidade de validação de blocos antigos. |
| `txindex` | `0` | Desativado para economizar espaço. Altere para 1 apenas se precisar de histórico completo via RPC. |
| `assumevalid` | `hash` | Ignora assinaturas de blocos antigos já conhecidos como válidos, acelerando o boot. |
| `daemon` | `0` | Desativado por padrão para permitir que a interface gráfica (GUI) abra no terminal. |

---

## ⚠️ Notas Importantes

> **Memória RAM:** Se o seu computador tiver **8GB de RAM ou menos**, altere a linha `dbcache=8000` para `dbcache=2000` dentro do arquivo para evitar travamentos do sistema operacional.

> **Segurança:** As opções de RPC estão comentadas por segurança. Se precisar de acesso remoto via linha de comando ou integração com outras carteiras, defina um `rpcuser` e `rpcpassword` fortes.

## 🤝 Contribuições

Sinta-se à vontade para abrir uma Issue ou enviar um Pull Request com melhorias!