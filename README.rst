===================
Palestras coletivas
===================

Um ambiente para você organizar eventos, trabalhos (palestras e cursos), grupos e compartilhar conhecimento (http://palestrascoletivas.com/).

E como eu instalo isso no meu Ubuntu?
=====================================

Já que a gente é hipster, vamos usar a última versão do Ruby

	rvm install ruby-2.0.0-p0

	rvm use 2.0.0

	rvm gemset create palestrascoletivas

	rvm gemset use palestrascoletivas

Moleque, na verdade a gente é muito hipster e por isso usamos o MongoDB, então instala ele lá!

	sudo apt-get install mongodb

Aproveita e instala a biblioteca para gerenciar o mongo (http://genghisapp.com/)

	gem install genghisapp

Instala também a biblioteca webkit, que é uma dependência do capybara-webkit

	sudo apt-get install libqtwebkit-dev

Baixa as dependências do projeto

	bundle install

Agora espera...

Gerar o token de segurança da aplicação

  echo "SECRET_TOKEN=`bundle exec rake secret`" > .env

Depois roda esse comando para adicionar uns dados no banco

	rake db:seed

Agora é só rodar e brincar!

	rails s

	localhost:3000

Executar os testes com a geração do relatório de cobertura, que será gravado na pasta coverage.

  bundle exec rake coverage
