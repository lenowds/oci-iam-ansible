# oci-iam-ansible
Utilizando Ansible para criar usuários na OCI e disparando e-mail de notificação com as credenciais de acesso para cada usuário criado.

**Console OCI**

\- Criar os compartimentos

- RecursosRedes

- RecursosCompute

- RecursosDB

  

**Cloud Shell OCI**

\- Atualizar as linhas abaixo, inserindo a OCID da tenancy e dos compartments: **RecursosRedes**, **RecursosCompute** e **RecursosDB**:

export PARENT_COMPARTMENT_OCID=<inserir-ocid>

export COMPUTE_COMPARTMENT_OCID=<inserir-ocid>

export REDES_COMPARTMENT_OCID=<inserir-ocid>

export DB_COMPARTMENT_OCID=<inserir-ocid>

export SENDGRID_API_KEY=<api-key-sendgrid>

export SENDGRID_SEND_MAIL=<sender-sendgrid>