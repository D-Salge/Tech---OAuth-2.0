# Tech - Autenticação com OAuth 2.0 via GitHub

![Linguagem Principal](https://img.shields.io/github/languages/top/D-Salge/Tech---OAuth-2.0?style=for-the-badge)

Projeto desenvolvido com Django para demonstrar a implementação de um sistema de autenticação social (OAuth 2.0) utilizando o **GitHub** como provedor. O sistema permite que usuários façam login em uma aplicação de forma segura, sem a necessidade de criar uma nova senha, utilizando suas credenciais do GitHub.

O projeto também implementa as melhores práticas de segurança, como o uso de variáveis de ambiente para proteger as chaves da API (`client_id` e `secret`).

---

### ✨ Funcionalidades

* Login de usuário através da sua conta do GitHub.
* Autenticação segura e simplificada com o protocolo OAuth 2.0.
* Gerenciamento de sessão para usuários autenticados.
* Proteção de chaves sensíveis (`client_id`, `secret`) utilizando variáveis de ambiente com `python-decouple`.

---

### 🚀 Tecnologias Utilizadas

Este projeto foi construído utilizando as seguintes tecnologias:

* **[Python](https://www.python.org/)**
* **[Django](https://www.djangoproject.com/)**: Framework web principal.
* **[django-allauth](https://django-allauth.readthedocs.io/)**: Biblioteca para lidar com autenticação social.
* **[python-decouple](https://pypi.org/project/python-decouple/)**: Para gerenciamento de variáveis de ambiente.
* **HTML / CSS**: Para a estrutura e estilização das páginas.

---

### 🏁 Como Começar (Guia de Instalação)

Siga os passos abaixo para executar o projeto em sua máquina local.

#### Pré-requisitos

* [Python 3.9+](https://www.python.org/downloads/)
* [Git](https://git-scm.com/)

#### Passo a Passo

1.  **Clone o repositório:**
    ```sh
    git clone [https://github.com/D-Salge/Tech---OAuth-2.0.git](https://github.com/D-Salge/Tech---OAuth-2.0.git)
    ```

2.  **Navegue até o diretório do projeto:**
    ```sh
    cd Tech---OAuth-2.0
    ```

3.  **Crie e ative um ambiente virtual:**
    * No Windows:
        ```sh
        python -m venv venv
        .\venv\Scripts\activate
        ```
    * No macOS ou Linux:
        ```sh
        python3 -m venv venv
        source venv/bin/activate
        ```

4.  **Instale as dependências do projeto:**
    ```sh
    pip install -r requirements.txt
    ```

5.  **Configure as Variáveis de Ambiente:**
    * Este projeto precisa de credenciais do GitHub para funcionar. Crie um **[OAuth App no GitHub](https://github.com/settings/developers)** para obter seu `client_id` e `secret`.
    * Durante a configuração do OAuth App no GitHub, use o seguinte URL de callback: `http://127.0.0.1:8000/accounts/github/login/callback/`
    * Renomeie o arquivo `.env.example` para `.env`:
        ```sh
        # No Windows (PowerShell)
        Rename-Item .env.example .env

        # No macOS ou Linux
        mv .env.example .env
        ```
    * Abra o arquivo `.env` e preencha com as credenciais que você obteve do GitHub:
        ```ini
        # .env
        GITHUB_CLIENT_ID=SEU_CLIENT_ID_AQUI
        GITHUB_SECRET_KEY=SUA_SECRET_KEY_AQUI
        ```

6.  **Aplique as migrações do banco de dados:**
    ```sh
    python manage.py migrate
    ```

7.  **Inicie o servidor de desenvolvimento:**
    ```sh
    python manage.py runserver
    ```

8.  **Pronto!** Abra seu navegador e acesse [http://127.0.0.1:8000/](http://127.0.0.1:8000/).

---

### 🎮 Como Usar a Aplicação

1.  Na página inicial, clique no link **"Login com GitHub"**.
2.  Você será redirecionado para a página de autorização do GitHub.
3.  Faça login com sua conta do GitHub e autorize a aplicação.
4.  Após a autorização, você será redirecionado de volta para a aplicação, já autenticado.

---

### 📬 Contato

**Daniel Salge**

* **GitHub**: [D-Salge](https://github.com/D-Salge)
