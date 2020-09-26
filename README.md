# Import_Files
 ▲ This repository is for storing a program that imports, standardizes and informs basic characteristics of the files. Such as, number of records, number of columns, data type of each field, number of null values ​​per column, etc.

Esse algoritimo na dta de hoje ainda está em desenvolvimento. Já funciona em excelencia para os objetivos de seu desenvolvimento, porém, não necessariamente prevê erros de digitação ou processos diferentes do fluxo de desenvolvimento do mesmo, o que pode gerar alguns bugs. Caso ocorra algum erro, apenas execute novamente. Em caso de maiores dúvidas mandar e-mail para: gabrielelias.vidacomercial@gmail.com.

OBS: Caso, após várias execuções ou depois de um erro (bug), o importador demore ou não reexecutar, basta reiniciar o kernel e executando em seguida o importador de arquivos.

O objetivo desse algoritmo é importar arquivos excel com uma ou várias planilhas(é possível escolher um ou mais(necessário instanciar novos objetos) planilhas para importar, padronizar as colunas para que seja possível analisar facilmente os dados, informar as características(atributos) da base de dados, tais como quantidade de registro, quantidade de colunas, quantidade de valores nulos por coluna e tipo de dados de cada coluna. Uma vez feito tudo isso, é gerado análise exploratória dos dados selecionados para importação.

1 - Esse Importador de arquivos, precisará ser configurado um endereço de uma pasta padrão( do computador do usuário), aonde deve ser colocado todos os arquivos que se deseja importar. 

 1.1 Uma vez executado, o importador de arquivos irá na pasta padrão e listará todos os arquivos disponíveis na pasta padrão (vide item 1). 
 1.2 O Importador de arquivos perguntará ao usuário qual desses arquivos ele deseja importar.
 1.3 O usuário precisará digitar( ou copir e colar) o nome do arquivo desejado na caixa de entrada de dados.
   
   1.3.1 - Se o o nome do arquivo for digitado incorretamente / se o arquivo não estiver na pasta padrão, o importador apresentará o seguinte erro: FileNotFoundError: [Errno 2] No such file or directory: 'IUGDUIOÇODP'.
   1.3.3 - Como a importação do arquivo é a parte fundamental da execução do programa ele vai paralisar completamente a execução, sendo necessário corrigir o problema e depois reexecutar o importador.
   1.3.3 - Na data de 26/09/2020 ainda não há tratamento para esse erro previsto em código. O erro sempre vai acontecer até que o arquivo esteja na past e/ou seja digitado o nome correto do arquivo.
   
  1.4 - Uma vez digitado/colado o nome correto do arquivo desejado o Importador verificará se existe mais de uma planilha dentro desse arquivo. Se houver, será listado em tela quantos e quais são as planilhas existentes no arquivo excel. O usuário poderá selecionar, copiando e colando ou digitando, a planilha que ele deseja importar.
    
    1.4.1 - Só é possível importar uma planilha por vez, para importar várias planilhas de um mesmo arquivo será necessário realizar ajuste no código.
    1.4.2 É possível importar mais de uma planilha criando criando novas instancias de importação. Dessa forma pode-se importar de consecutivamente varias planilhas de um mesmo arquivo.
    
 1.5 - Uma vez selecionado o arquivo e a planilha,  base de dados existente nessa planilha será importada automaticamente. 
 1.6 - Se houver apenas uma planilha no arquivo, essa planilha será importada automaticamente, sem precisar de ação do usuário.
 1.7 - Uma vez importado a base, será informado suas características(atributos) principais, tais como:
       
       1.7.1 - quantidade de linhas e de colunas existentes na base.
       1.7.2 - Resultado da padronização das colunas.
   
              1.7.2.1 - Para cada coluna existente na base será atribuido o seguinte padrão.
       
                         1.7.2.1.1 - Todas as letras estarão em minusculas.
                         1.7.2.2.2 - Todos os espaços serão substituídos sublinhado (tracinho inferior).
               
                                     1.7.2.2.2.1 - Caso haja mais de um espaço ou vários, serão subistutuidos pelo mesmo número de espaços em sublinhados(tracinho inferior).

       1.7.3 - Quantidade de valores nulos por coluna.
       1.7.4 - Tipos de dados de cada coluna (string, categórica, datas, int, floar e etc) 
 
 2 - Após a importação, é solicitado ao usuário entrar com um nome(titulo) para análise, esse nome serve como título no relatório gerado pelo importador.
 2.1 - O relatório gerado pelo importador é um relatório de análise exploratório dos dados onde e possível visualizar uma quantidade enorme de informações sobre a base, tais como correlações, tamanho da base, tipo dos dados, quantidade de valores nulos, valores que mais se repetem por coluna e etc.
 2.2 - O nome digitado pelo usuário servirá como título e como nome do arquivo .html que será baixado automáticamente para a pasta padrão escolhida (vide item - 1).
 
