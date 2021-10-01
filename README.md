# oci-iam-ansible
Utilizando Ansible para criar usuários na OCI e disparando e-mail de notificação com as credenciais de acesso para cada usuário criado.

Para envio de e-mail será utilizado a integração Ansible + SendGrid. É necessário criar uma conta no site [SendGrid.com](https://sendgrid.com/)  e gerar uma api de integração que será armazenada como uma variável de ambiente na console Cloud Shell OCI, logo abaixo.

**Console OCI**

\- Criar os compartimentos

- RecursosRedes

- RecursosCompute

- RecursosDB

  

**Cloud Shell OCI**

\- Atualizar as linhas abaixo, inserindo a OCID da tenancy e dos compartments: **RecursosRedes**, **RecursosCompute** e **RecursosDB**:

export PARENT_COMPARTMENT_OCID=`<inserir-ocid>`

export COMPUTE_COMPARTMENT_OCID=`<inserir-ocid>`

export REDES_COMPARTMENT_OCID=`<inserir-ocid>`

export DB_COMPARTMENT_OCID=`<inserir-ocid>`

export SENDGRID_API_KEY=`<api-key-sendgrid>`

export SENDGRID_SEND_MAIL=`<sender-sendgrid>`



**Edit playbook**

Abrir e editar o playbook tcb-bmc-iam-cria-usuarios-dba-admin.yaml alterando a variável domínio de "@thecloudbootcamp.com" para o domínio que deseja testar, por exemplo. Para testar submetendo e-mail para contas do Gmail, utilize "@gmail.com" como domínio.

dominio: "@thecloudbootcamp.com" > dominio: "@gmail.com"

A variável usuários contém a lista de usuários que contém contas no domínio gmail. Por exemplo: <u>carlos1234</u>@gmail.com, <u>meneguel1</u>@gmail.com

usuarios:
      - carlos1234
            - meneguel1