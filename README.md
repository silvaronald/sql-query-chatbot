# Chatbot para consultas a banco de dados com LLM

Este projeto consiste na implementação de um chatbot para auxiliar no processo de análise de dados. Seu propósito é interpretar perguntas formuladas em linguagem natural, traduzi-las para consultas SQL, executar essas consultas em bancos de dados locais e fornecer respostas claras e bem estruturadas.

Os passos que compõem o fluxo da aplicação são:
- Transformação de perguntas feitas em linguagem natural em consultas SQL por meio de LLMs
- Verificação da sintaxe SQL e a segurança das consultas 
- Restrição de operações que modificam o banco de dados (ex.: INSERT, UPDATE, DELETE)
- Caso a _query_ gerada pela LLM esteja em desconformidade com os requisitos, será feito um novo _prompt_ pedindo sua correção 
- Execução em um banco de dados local
- Explicação da LLM sobre a consulta executada aliada a uma possível explicação dos resultados obtidos
