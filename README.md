# AutoLoginForce

O programa fornecido é escrito em Python e usa a biblioteca Selenium para automatizar interações com um navegador da web, especificamente o Google Chrome. Aqui está o que é necessário para utilizar o programa:

1. Bibliotecas necessárias:
   - Selenium: É a principal biblioteca usada para automatizar o navegador. Pode ser instalada usando o comando `pip install selenium`.
   - ChromeDriver: É o driver necessário para interagir com o Google Chrome. O programa assume que o ChromeDriver esteja localizado em "/home/sandro/AutoLoginForce/chromedriver". Certifique-se de ter o ChromeDriver compatível instalado. Você pode baixá-lo a partir do site oficial do ChromeDriver: https://sites.google.com/a/chromium.org/chromedriver/downloads.

2. Configurações:
   - URL: Substitua a variável `url` pelo endereço URL da página onde você deseja testar as senhas.
   - IDs dos campos de entrada: Substitua as variáveis `input_id` e `input_pw` pelos IDs dos campos de usuário e senha, respectivamente, na página que você está testando. Esses IDs são usados para localizar os elementos de entrada do formulário na página.
   - Arquivo de palavras-chave: Substitua o caminho para o arquivo de palavras-chave na variável `file_path`. Certifique-se de que o arquivo de palavras-chave esteja no formato adequado, onde cada palavra-chave esteja em uma nova linha.
   - Número de threads: Defina o número desejado de threads na variável `num_threads`. Isso determina quantas partes a lista de palavras-chave será dividida para processamento paralelo.
   
3. Funcionamento:
   - O programa divide a lista de palavras-chave em partes iguais, dependendo do número de threads especificado.
   - Em seguida, ele cria threads e atribui partes diferentes da lista de palavras-chave a cada thread.
   - Cada thread executa a função `test_passwords`, que automatiza a interação com o navegador, inserindo cada senha da lista de palavras-chave e realizando ações adicionais, se necessário.
   - Após o término das threads, você pode verificar se a senha foi encontrada definindo a variável `password_found` como `True`.
   
Lembre-se de fazer as alterações necessárias no código para adaptá-lo ao seu caso específico, como o caminho do ChromeDriver, a URL da página e os IDs dos campos de entrada. Certifique-se de que todas as bibliotecas necessárias estejam instaladas corretamente antes de executar o programa.
