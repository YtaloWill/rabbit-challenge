# Desafio

1. Criar um endpoint para salvar na fila do RabbitMQ (fila para ser criada antes, não precisa criar no momento da requisição).

*(criar um consumidor que rode o tempo inteiro, procurando por mensagens novas)*

* Caso a fila não exista ou a mensagem esteja fora do padrão, retornar erro

2. Criar um consumidor que siga o padrão prefetch + ack, caso a mensagem não funcione, enviar para fila morta

* O consumidor irá rodar o tempo inteiro esperando por mensagens na fila, e ao entrarem, irá processar

* Criar um consumidor de fila morta que irá tentar novamente e logar o erro caso a mensagem não processe de jeito nenhum

3. Conectar em um banco Mysql local e salvar a informação do consumidor no banco, em uma tabela com o mesmo padrão da mensagem JSON

## Fase bônus:

1. Usar async await

2. Escrever um script de teste que rode antes de subir o servidor para testar se a fila existe ou não, e o banco/tabela existem ou não