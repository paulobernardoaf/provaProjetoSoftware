# provaProjetoSoftware

<div>
  <p>
    <br> <a href="https://imgur.com/elaNCwe"><img src="https://i.imgur.com/elaNCwe.png" title="source: imgur.com" /></a> <br>
  </p>
  </div>
  
## 1. Funcionalidades

* #### Criação e Associação de Usuários

	<div>
		<p>
			Permite criar um novo usuário sendo ele:
			<ul>
				<li>Aluno de Graduação</li>
				<li>Aluno de Mestrado</li>
				<li>Aluno de Doutorado</li>
				<li>Professor</li>
				<li>Pesquisador</li>
				<li>Profissional</li>
					<ul>
						<li>Desenvolvedor</li>
						<li>Testador</li>
						<li>Analista</li>
					</ul>
			</ul>
			<br>
			E associar esse usuário em um projeto ou atividade.
		</p>
	</div>

* #### Alterar Status de um Projeto

	<div>
		<p>
			Permite que o status de um projeto seja alterado seguindo as regras:
			<ul>
				<li>O coordenador deve poder iniciar uma criação apenas se constarem todas as informações básicas.</li>
				<li>O coordenador deve poder alterar o status para “Concluído”, se existir a descrição do projeto e atividades.</li>
			</ul>
		</p>
	</div>

* #### Consultas

	<div>
		<p>
			Permite que sejam realizadas as seguintes consultas:
			<ol>
				<li>Consulta por Usuário</li>
				<li>Consulta por Projeto</li>
				<li>Consulta por Atividade</li>
			</ol>
			<br>
			Onde cada tipo de consulta mostra as respectivas informações sobre o que foi requisitado.
		</p>
	</div>

* #### Relatório

	<div>
		<p>
			Permite que seja realizado um reĺatório onde todas as informações sobre um determinado projeto ou atividade sejam mostradas.
		</p>
	</div>

## 2. Classes:

* #### Usuario:

	<div>
		<p>
			<b>Motivação:</b> Necessidade de criar um usuário para guardar as informações. <br>
			<b>Solução:</b> Classe Usuario onde contem as informações necessárias.
			Vantagens: Melhor organização e manutenção. 
			<br>
			Possui subclasses:
				<ul>
					<li>Aluno de Graduação</li>
					<li>Aluno de Mestrado</li>
					<li>Aluno de Doutorado</li>
					<li>Professor</li>
					<li>Pesquisador</li>
					<li>Profissional</li>
						<ul>
							<li>Desenvolvedor</li>
							<li>Testador</li>
							<li>Analista</li>
						</ul>
				</ul> <br>
			onde cada subclasse possui atributos que pertecem somente a elas.
		</p>
	</div>

* #### Sistema:

	<div>
		<p>
			<b>Motivação</b>: Necessidade de criar uma classe onde todas as informações estão salvas. (Como se fosse um banco de dados) <br>
			<b>Solução</b>: Classe Sistema onde contem todos os projetos, atividades e usuários. <br>
			<b>Vantagens</b>: Dados disponíveis para as consultas.<br>
		</p>
		<p>
			Possui métodos:
			<ul>
				<li>
					<b>consultarUsuario(ID)</b>
					<ul>
						<li>Recebe como parâmetros o ID do usuário a ser consultado e mostra todas as informações do usuário pesquisado.</li>
					</ul>
				</li>
				<li>
					<b>consultarProjeto(ID)</b>
					<ul>
						<li>Recebe como parâmetros o ID do projeto a ser consultado e mostra todas as informações do projeto pesquisado.</li>
					</ul>
				</li>
				<li>
					<b>consultarAtividade()</b>
					<ul>
						<li>Recebe como parâmetros o ID da atividade a ser consultada e mostra todas as informações da atividade pesquisada.</li>
					</ul>
				</li>
				<li>
					<b>relatorio()</b>
					<ul>
						<li>Nesse método é possível escolher sobre o que será o relatório:
							<ul>
								<li>Usuário</li>
								<li>Projeto</li>
								<li>Atividade</li>
							</ul>
						</li>
						E será mostrado todas as informações de acordo com a escolha.
					</ul>
				</li>
				<li>
					<b>adicionarUsuario()</b>
					<ul>
						<li>
							Cria um novo usuário e o adiciona ao sistema.
						</li>
					</ul>
				</li>
				<li>
					<b>associarUsuarioEmProjeto()</b>
					<ul>
						<li>
							Nesse método é possivel escolher um projeto e um usuário, onde será adicionado ao projeto escolhido o usuário selecionado.
						</li>
					</ul>
				</li>
				<li>
					<b>associarUsuarioEmAtividade()</b>
					<ul>
						<li>
							Nesse método é possivel escolher uma atividade e um usuário, onde será adicionado ao atividade escolhida o usuário selecionado.
						</li>
					</ul>
				</li>
				<li>
					<b>adicionarProjeto()</b>
					<ul>
						<li>
							Método onde é criado um novo projeto.
						</li>
					</ul>
				</li>
				<li>
					<b>adicionarAtividade()</b>
					<ul>
						<li>
							Método onde é criada uma nova atividade.
						</li>
					</ul>
				</li>
			</ul>
		</p>
	</div>

* #### Informacoes:

	<div>
		<p>
			<b>Motivação</b>: Necessidade de criar uma classe onde os atributos compartilhados entre Projeto e Atividade estivessem disponíveis.<br>
			<b>Solução</b>: Classe Informações onde contém:
				<ul>
					<li>ID</li>
					<li>Descrição</li>
					<li>Data/Hora de Início</li>
					<li>Data/Hora de Término</li>
					<li>Coordenador</li>
					<li>Profissionais</li>
					<li>Status</li>
				</ul>
				<br>
			<b>Vantagens</b>: Melhor manutenção e organização do código<br>
		</p>
	</div>


* #### Projeto:

	<div>
		<p>
			<b>Motivação</b>: Necessidade de criar uma classe onde as informações de um projeto estivessem salvas. <br>
			<b>Solução</b>: Classe Projeto onde contém:
				<ul>
					<li>Atividades</li>
				</ul>
				<br>
			<b>Vantagens</b>: Melhor manutenção e organização do código<br>
		</p>
		<p>
			Possui métodos:
			<ul>
				<li>
					<b>alterarStatus()</b>
					<ul>
						<li>
							Esse método possibilita a mudança do status do projeto.
						</li>
					</ul>
				</li>
				<li>
					<b>modificarProjeto()</b>
					<ul>
						<li>Esse método permite alterar as informações do projeto que não esteja concluído.</li>
					</ul>
				</li>
				<li>
					<b>listarParticipantes()</b>
					<ul>
						<li>
							Esse método mostra todos os participantes que pertencem ao projeto.
						</li>
					</ul>
				</li>
			</ul>
		</p>
	</div>

* #### Atividade:

	<div>
		<p>
			<b>Motivação</b>: Necessidade de criar uma classe onde as informações de uma atividade estivessem salvas. <br>
			<b>Solução</b>: Classe Projeto onde contém:
				<ul>
					<li>Tarefas</li>
				</ul>
				<br>
			<b>Vantagens</b>: Melhor manutenção e organização do código.<br>
		</p>
		<p>
			Possui métodos:
			<ul>
				<li>
					<b>modificarAtividade()</b>
					<ul>
						<li>Esse método permite alterar as informações da atividade.</li>
					</ul>
				</li>
				<li>
					<b>listarParticipantes()</b>
					<ul>
						<li>
							Esse método mostra todos os participantes que pertencem a atividade.
						</li>
					</ul>
				</li>
			</ul>
		</p>
	</div>
