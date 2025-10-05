# Relatório do Desafio - Configuração de Banco de Dados na Microsoft Azure

## Introdução
Dando continuidade ao meu projeto de implementação da máquina virtual e ao uso do PostgreSQL como banco de dados, este relatório documenta o processo de configuração de uma instância de Banco de Dados na plataforma Microsoft Azure. O objetivo deste desafio é criar um repositório que contenha resumos, anotações e dicas úteis sobre o uso do Azure, que servirão como material de apoio para meus estudos e futuras implementações.

## Objetivo do Projeto
O foco principal deste laboratório foi configurar uma instância de Banco de Dados PostgreSQL no Microsoft Azure, explorando as funcionalidades e recursos disponíveis na plataforma. Essa experiência me proporcionou um melhor entendimento das vantagens de utilizar serviços de nuvem para o gerenciamento de bancos de dados.

## Tecnologias Utilizadas
- **Plataforma:** Microsoft Azure
- **Banco de Dados:** PostgreSQL
- **Ferramenta de Gerenciamento:** Azure Portal

## Passo a Passo da Configuração da Instância de Banco de Dados

### 1. Acessando o Azure Portal
Comecei acessando o [Azure Portal](https://portal.azure.com) com minha conta da Microsoft. Navegando pela interface amigável, encontrei várias opções para criar e gerenciar recursos.

### 2. Criando um Banco de Dados PostgreSQL
Na barra de navegação do portal, cliquei em "Criar recurso" e busquei por "Banco de Dados PostgreSQL". Selecionei a opção “Banco de Dados PostgreSQL”.

### 3. Configurações Iniciais
Preenchi as informações necessárias para configurar a instância:

- **Nome do Servidor:** meu-banco-postgres
- **Região:** Escolhi uma região próxima para otimizar latência, como "Brazil South".
- **Versão do PostgreSQL:** Selecionamos a versão mais recente disponível.
- **Administração:** Criei um nome de usuário e senha para gerenciar o banco.

### 4. Configurando a Escalabilidade e o Desempenho
Escolhi a opção de camada de desempenho adequada para minhas necessidades de desenvolvimento, optando por um plano que equilibra custo e performance. Isso inclui:

- **Compute Units:** Escolhi uma quantidade de unidades que se adequasse ao meu uso atual.
- **Armazenamento:** Configurei 512 MB de armazenamento, com possibilidade de aumentar conforme a necessidade.

### 5. Configurando Redes e Segurança
É vital garantir a segurança dos dados. Configurei as definições de firewall para permitir apenas conexões a partir do meu endereço IP. Além disso, ativei a autenticação de duas etapas para proteger ainda mais o acesso ao banco.

### 6. Conectando-se ao Banco de Dados
Após a criação da instância, utilizei ferramentas como pgAdmin para conectar-me ao novo banco de dados. Realizei alguns testes criando tabelas e inserindo dados:

```sql
CREATE TABLE clientes (
    id SERIAL PRIMARY KEY,
    nome VARCHAR(100),
    email VARCHAR(100)
);
```
Esses testes ajudaram a garantir que a instância estava funcionando corretamente.

### Dicas e Anotações sobre o Uso do Azure
- Custo: Sempre verifique as opções de preços antes de criar instâncias, pois os custos podem variar significativamente com a configuração.
- Documentação: O Azure possui uma documentação extensa, o que é extremamente útil. Aproveite os tutoriais e guias disponíveis na plataforma.
- Segurança: Lembre-se sempre de revisar as configurações de segurança, habilitando somente o acesso necessário e utilizando autenticação forte.
- Monitoramento: Utilize a ferramenta de monitoramento do Azure para acompanhar a performance e ajustar a configuração conforme sua necessidade.

### Conclusão
A configuração da instância de Banco de Dados PostgreSQL na Microsoft Azure foi uma experiência valiosa. Aprendi não apenas a criar e gerenciar um banco de dados na nuvem, mas também sobre a importância de segurança e escalabilidade em projetos futuros. Sinto-me mais preparada para usar o Azure em meus desenvolvimentos e espero que esse repositório de anotações sirva como um guia útil para mim e para outros desenvolvedores.

### Próximos Passos
- Integrar o banco de dados configurado com minhas aplicações em desenvolvimento.
- Explorar mais sobre as funcionalidades do Azure, como backup automático e recuperação.
- Criar documentação adicional com base nas experiências adquiridas e compartilhar com a equipe.
