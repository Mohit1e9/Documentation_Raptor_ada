# Installation and Setup for Ada/Raptor
<ul>
  <li>Downlaod and Install Mysql community Server:https://dev.mysql.com/downloads/mysql/</li>
  <ol>
    <li>Create account and set password for the user</li>
    <li>Create the schema for tables and views</li>
    <li>Install redis server</li>
  </ol>
  <li>Pull the code from Git repository</li>
    <ol>
      <li>clone the repo: git clone https://github.com/financialmachines</li>
      <li>set up the branch as dev branch <strong>git checkout dev</strong></li>
    </ol>
  <li>Pull the <strong>qux</strong> module from https://github.com/quxdev/qux.git</li> 
   <ol>
     <li>Place the folder in the ada directory</li>
   </ol>
  <li>Create the virtual environment</li>
   <ol>
     <li>switch to project directory ada</li>
     <li>create virtual environment <strong>python3 -m venv <em>name_of_environment</em></strong></li>
     <li>Activate the Environment</li>
   </ol>
  <li>Installing Libraries and Modules</li>
    <ol>
      <li>Upgrade the pip</li>
      <li>Install the packages and libraries <strong>pip install -r config/requirements.txt</strong></li>
    </ol>
  <li>Create .env file in the project app folder</li>
    <ol>
      <li>setup the variables for the database connectivity</li>
      <li>verify and add  </li>
        <code>            DJANGO_DEBUG=True
                          DB_DATABASE='database_name'
                          DB_USERNAME='username'
                          DB_PASSWORD='password'
                          DB_HOST='localhost'
        </code>
      </li>
    </ol>
  <li>make migration</li>
    <ol>
      <li>make migration for the already created migration <strong>python manage.py migrate</strong> </li>
      <li>Create superuser for admin to provide the subscription for engines </li>
    </ol>
  <li>Creating superuser</li>
    <ol>
      <li>open django admin panel</li>
      <li>Create groups <em>Falcon</em> and <em>Raptor</em></li>
      <li>Add these groups to superuser created</li>
    <ol>
  <li>Run the celery for task scheduling <strong>celery -A ada worker --loglevel=INFO</strong></li>
  
</ul>

    

  
