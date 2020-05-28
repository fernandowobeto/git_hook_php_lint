IMPLEMENTACAO PHP LINT NO GITLAB
================================
1) Instalação do php no servidor do gitlab
2) Criação da pasta "custom_hooks" em /var/opt/gitlab/git-data/repositories/GRUPO/REPOSITORIO.git
3) Criação do arquivo "pre-receive" com o código a ser executado no recebimento dos dados via push dentro da pasta "custom_hooks" acima criada
4) Definição do git como dono da pasta e arquivo com "chown -R git:root custom_hooks"
5) Permissão de execução do arquivo "pre-receive" acima criado

A cada push de conteudo para o servidor o arquivo pre-receive sera executado e qualquer saida nao zero abortara o push.
