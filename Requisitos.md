# Resumo

A plataforma EnfUroped é um sistema de gestão de dados de pacientes com doenças urológicas, que permite a realização de consultas e o acompanhamento de pacientes, além de permitir que estudantes de enfermagem possam realizar estudos e pesquisas sobre doenças urológicas.

Quando alguém desejar ter uma consulta utilizando a plataforma, o responsável pelo paciente deve se cadastrar usando o site, depois de se cadastrar e logar, ele poderá cadastrar um paciente em que é resposável e agendar uma consulta de forma simples. Durante esse processo de primeira consulta, a plataforma deve escolher um enfermeiro para esse paciente de forma automática de acordo com as disponibilidades de todos os enfermeiros. O médico escolhido para atender essa nova consulta deve ser notificado e deverá aceitar essa consulta ou recusa-la em um período de 72hrs.

Caso o enfermeiro aceite a consulta, o paciente será considerado como um paciente com acompanhamento e todas as próximas consultas serão agendadas pelo enfermeiro responsável. Caso o enfermeiro recuse a consulta, o sistema atribuirá o paciente a algum administrador que deverá discutir com o paciente alguma forma de realocar a consulta para algum enfermeiro disponível.

O responsável pelo paciente poderá preencher alguns instrumentos relacionados a sua consulta antes dela acontecer, como por exemplo, o diário de eliminações que deve ser preenchido por dois dias seguidos. O enfermeiro e o paciente podem conversar entre si usando o chat da plataforma, e poder enviar documentos, como por exemplo, um relatório de uma consulta anterior.

Os estudantes cadastrados na plataforma poderão escrever artigos para o blog, esses artigos podem ser sobre doenças urológicas, ou sobre qualquer outro assunto relacionado a saúde. Os artigos podem ser publicados por qualquer estudante, mas sempre deverão ser revisados.

# Público alvo

- Enfermeiros (Atendem pacientes)
- Pacientes, familiares e cuidadores (Participam de consultas)
- Estudantes de extensão (Criam artigos)
- Administradores (São enfermeiros com permissão de administrador)

# Tecnologias

- [TypeScript](https://www.typescriptlang.org/)

<br>

- [Angular](https://angular.io/) Para o frontend
- [Express](https://expressjs.com/) Para o backend
- [PostgreSQL](https://www.postgresql.org/) Para o banco de dados
- [Prisma](https://www.prisma.io/) Para o ORM
- [Passport](http://www.passportjs.org/) Para autenticação

# Requisitos de alta prioridade

- Deve ter cadastro, login e logout de usuários tanto no frontend quanto no backend

## Responsáveis (família) e pacientes

- Deve ser possível para um usuário se cadastrar como paciente e marcar uma primeira consulta com facilidade.
- Deve ser possível para um paciente preencher os instrumentos (DVSS, ROMA IV, SOL CHUVA, DIÁRIO) antes de uma consulta.
- Deve ter um sistema de mensagens para que o paciente possa conversar com o enfermeiro responsável.
- Deve ser possível que um usuário responsável por um paciente possa cadastrar novos pacientes e marcar consultas para eles.
- Um responsável pode reativar a conta de um paciente que foi desativada por ter tido alta, esse paciente poderá marcar sua primeira consulta novamente mas seu status será de relapso.

## Enfermeiros

- Deve ser possível para um enfermeiro se cadastrar e aguardar aprovação de um administrador.
- Deve ser possível para um enfermeiro criar e editar suas disponibilidades.
- Deve ser possível para um enfermeiro aceitar ou recusar uma consulta.
- Deve ser possível para um enfermeiro enviar mensagens para algum paciente em que seja responsável.
- Deve ser possível para um enfermeiro criar consultas de retorno para um paciente em que seja responsável e que já tenha participado de sua primeira consulta.
- Deve ser possível para um enfermeiro visualizar as informações de um paciente, suas consultas passadas e seus instrumentos preenchidos.
- Um enfermeiro pode modificar os instrumentos de um paciente em até 72hrs após a consulta.
- Um enfermeiro deve conseguir dar alta para um paciente, o que desativa a conta do paciente.

## Estudantes

- Um estudante de extensão poderá de cadastrar e aguardar aprovação de um administrador.
- Um estudante pode criar artigos para o blog da plataforma.
- Ele poderá editar e excluir os artigos que criou.
  - ?? Um estudante pode criar um artigo como rascunho e publicá-lo quando quiser. ??

## Administradores

- Um administrador pode se cadastrar primeiramente como enfermeiro e depois ser promovido a administrador por outro administrador.
- Um administrador pode aprovar ou recusar o cadastro de um enfermeiro.
- Um administrador pode aprovar ou recusar o cadastro de um estudante de extensão.
- Um administrador pode excluir a conta de um enfermeiro.
- Um administrador pode excluir a conta de um estudante de extensão.
- Um administrador pode editar ou excluír um artigo.
- Um administrador pode visualizar todas as informações de um paciente, suas consultas passadas e seus instrumentos preenchidos.
- Um administrador pode visualizar todas as informações de um enfermeiro e seus pacientes.
- Um administrador pode visualizar todas as informações de um estudante de extensão e seus artigos.
- Um administrador pode alocar um paciente para um enfermeiro.
- Um administrador pode conversar com um paciente, mesmo se ele não estiver sendo acompanhado.

# Requisitos de baixa prioridade

- A plataforma deve notificar por email o administrador, enfermeiro e paciente quando algum evento importante acontecer.
- A plataforma deve implementar uma forma de os usuários recuperarem suas senhas caso esqueçam.
- A plataforma deve implementar uma forma de os usuários alterarem seus dados pessoais e senha.
- A plataforma deve implementar uma forma de os usuários efetuarem o login e permanecerem logados mesmo quando fechar o navegador.
- A plataforma deve implementar uma forma de os usuários efetuarem o logout.
- A plataforma deve ser responsiva e simples de usar, principalmente para os pacientes e responsáveis que acessam a plataforma pelo celular e não tem muito conhecimento técnico.
- A plataforma deve ser segura, não deve ser possível acessar informações de outros usuários se não for o dono da conta ou o administrador.
