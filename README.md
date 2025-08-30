# eventos-academicos
Projeto extraordinário saber desenvolvimento web II

Sistema de Gerenciamento de Eventos Acadêmicos
Um sistema web completo desenvolvido em Laravel para gerenciamento de eventos acadêmicos, com controle de usuários, inscrições e administração de eventos.

✨ Funcionalidades
👤 Sistema de Autenticação
Cadastro e login de usuários

Controle de sessões com cookies de "Lembrar-me"

Differentiação entre usuários comuns e administradores

🎯 Gestão de Eventos
Administradores: Criar, editar, visualizar e excluir eventos

Usuários: Visualizar lista de eventos disponíveis

Busca e filtro de eventos

Controle de vagas e datas

📝 Sistema de Inscrições
Inscrição em eventos com controle de duplicidade

Área do usuário para gerenciar inscrições

Cancelamento de inscrições

Controle de status (confirmada, pendente, cancelada)

👨‍💼 Área Administrativa
Visualização de lista de inscritos por evento

Dashboard com estatísticas e eventos recentes

Controle completo sobre todos os eventos

🛠️ Tecnologias Utilizadas
Backend: PHP 8.1+, Laravel 10+

Frontend: HTML5, CSS3, JavaScript, Bootstrap 5

Banco de Dados: MySQL

Autenticação: Session-based com cookies

Padrão: MVC (Model-View-Controller)

📋 Requisitos do Sistema
PHP 8.1 ou superior

Composer

MySQL 5.7+ ou MariaDB 10.3+

Apache ou Nginx

Extensões PHP: BCMath, Ctype, Fileinfo, JSON, Mbstring, OpenSSL, PDO, Tokenizer, XML
________________________________________________________________________________________________

Instalação e Configuração
1. Clone o repositório:
git clone https://github.com/Schm1ttz/eventos-academicos.git
cd eventos-academicos


2. Instale as dependências:
composer install


3. Configure o ambiente:
cp .env.example .env
php artisan key:generate


4. Configure o banco de dados
Edite o arquivo .env:
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=eventos_academicos
DB_USERNAME=root
DB_PASSWORD=


5. Execute as migrations:
php artisan migrate


7. Inicie o servidor:
php artisan serve
Acesse: http://localhost:8000


8. Criar usuário administrador:
php artisan tinker

$user = new App\Models\User();
$user->name = 'Administrador';
$user->email = 'admin@admin.com';
$user->password = bcrypt('password123');
$user->tipo = 'admin';
$user->save();
exit



