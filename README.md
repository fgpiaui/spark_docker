# Processo de subida do Spark em containers #

Vamos subir 1 container para spark-master, 2 containers de spark-worker e 1 container para o jupyter.
Além disso, para modularizar nossa aplicação vamos dividir nas seguintes imagens:
* cluster-base <br>
  **Imagem que vai conter o ambiente linux e as intalações bases para o spark e o jupyter**

* spark-base <br>
  **Imagem que instala o spark e seta as variáveis de ambiente**
  
* spark-master <br>
  **Imagem que executará o spark master, utilizará 2 portas, uma para acesso via browser (O WEB UI) e outra para conexão com aplicação**
  
* spark-worker <br>
  **Imagem que executa o spark-worker. Este servirá para realizar o processamento a ser feito de dados enviado pela aplicação conectada**
  
* jupyter <br>
  **Imagem que sobe o jupyter para fazer a execução da aplicação com o spark**
