1. Estrutura HTML do Formulário de Cadastro
O arquivo cad_form.html contém a interface para o formulário de cadastro de usuários, onde os visitantes podem se cadastrar para utilizar o sistema VariableSong.
1.1. Cabeçalho (Head)
Meta Tags:
Define o charset como UTF-8 para compatibilidade de caracteres.
Define o viewport para garantir que o layout seja responsivo em dispositivos móveis.
Link CSS:
Estilo do formulário é importado através do arquivo acesso/css/style_cad_form.css.
Título da Página:
Define o título da página como "Formulário de Cadastro".
1.2. Corpo (Body)
Container de Imagem:
Exibe uma imagem ilustrativa (undraw_playlist_re_1oed.svg) relacionada a playlists de música.
Formulário Principal:
Ação do formulário é configurada para enviar dados via método POST ao arquivo PHP banco.php, onde as informações serão processadas.
Inclui os seguintes campos de entrada de dados:
Primeiro Nome: Campo de texto obrigatório.
Sobrenome: Campo de texto obrigatório.
Email: Campo de texto obrigatório com validação de formato.
Telefone: Campo de texto obrigatório com máscara de entrada.
Senha e Confirmação de Senha: Campos de senha obrigatórios, onde a senha é digitada duas vezes para validação.
Gênero: Opções de gênero representadas por botões de rádio (Feminino, Masculino, Não-binário, Outros).
Botões:
Cadastrar: Envia os dados para o banco de dados.
Já tenho cadastro: Redireciona usuários já cadastrados para outra página de login (tenho_cad.html).
2. CSS do Formulário de Cadastro
O arquivo style_cad_form.css controla o layout e o design da página de cadastro.
2.1. Variáveis de Cores:
Color Palette: Definida em :root para facilitar o uso consistente de cores.
Ex: --color-light-50, --color-dark-100, e um gradiente aplicado como fundo do site.
2.2. Estilos Gerais:
Reseta margens e preenchimentos e define a fonte padrão como 'Noto Sans'.
O layout da página usa flexbox para centralizar os elementos.
2.3. Formulário e Inputs:
Campos de Entrada:
Estilos aplicados aos inputs para torná-los mais atraentes visualmente, com bordas arredondadas e sombras.
Efeito Hover e Foco: Os campos mudam de cor quando o usuário interage com eles.
Botões:
Definições de estilo para os botões, incluindo hover effects para melhorar a experiência do usuário.
3. Página de Confirmação de Cadastro
O arquivo tenho_cad.html é uma página que confirma que o usuário já efetuou o cadastro com sucesso e contém um formulário de login para que o usuário possa entrar no sistema.
3.1. Cabeçalho (Head)
Semelhante à página de cadastro, mas com link para style_tenho_cad.css.
3.2. Corpo (Body)
Imagem: Contém uma imagem de ilustração.
Texto de Boas-vindas: Mensagem para o usuário, explicando que o cadastro foi efetuado com sucesso e que agora ele pode fazer login para usar o sistema.
Formulário de Login:
Campos para o usuário inserir o email e senha.
Botão para submeter os dados para o sistema de login.
4. Página de Avaliação de Músicas
O arquivo avaliacao-1.html permite que os usuários façam avaliações de músicas no sistema, incluindo a opção de atribuir estrelas.
4.1. Cabeçalho (Head)
Link para o arquivo de estilo style_avaliacao.css e uma biblioteca externa de ícones (Font Awesome) para exibir as estrelas de avaliação.
4.2. Corpo (Body)
Formulário de Avaliação:
Inclui campos para o nome da música, artista e um texto de avaliação.
Estrelas de Avaliação: O usuário pode clicar em estrelas para avaliar de 1 a 5, com o JavaScript controlando a interação.
Botão de Enviar: Submete a avaliação ao sistema.
4.3. JavaScript para Avaliação com Estrelas
Função de Click:
Um script em JavaScript manipula a interação com as estrelas. Quando uma estrela é clicada, ela e todas as anteriores são preenchidas com cor (dourado), representando a avaliação do usuário.
5. CSS da Página de Avaliação
O arquivo style_avaliacao.css cuida da aparência da página de avaliação, aplicando os mesmos princípios de layout e design da página de cadastro.
6. Código PHP para Processamento do Cadastro
O arquivo PHP processa os dados do formulário enviado.
6.1. Lógica do Código PHP:
Verifica se o botão de cadastrar foi acionado (isset($_POST['cadastrar'])).
Coleta os dados enviados via POST (nome, sobrenome, email, telefone, senha, gênero).
Validação de Senhas: Verifica se as senhas informadas coincidem.
Conexão com Banco de Dados: (a ser continuada) define as credenciais de acesso ao banco de dados local onde as informações serão armazenadas.
7. Possíveis Melhorias
Validação no Lado do Cliente: Implementar validação mais robusta usando JavaScript.
Mensagens de Erro/Confirmação: Exibir mensagens amigáveis ao usuário para indicar sucesso ou erros no processo de envio.
Essa documentação visa orientar sobre o funcionamento geral do código apresentado, desde o formulário de cadastro até a avaliação de músicas, além de fornecer uma visão sobre a estrutura CSS e PHP usadas no sistema VariableSong.
