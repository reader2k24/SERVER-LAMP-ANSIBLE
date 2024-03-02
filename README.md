<h1>Установка и настройка сервера с MySQL, Nginx и PHP</h1>

<p>Этот Ansible playbook предназначен для установки и настройки сервера с базой данных MySQL, веб-сервера Nginx и интерпретатора PHP.</p>

<h2>Использование</h2>

<ol>
  <li>Убедитесь, что у вас установлен Ansible и на вашем управляемом хосте настроен SSH-доступ.</li>
  <li>Склонируйте репозиторий с этим playbook:</li>
</ol>

<pre><code>git clone https://github.com/your_repository.git
</code></pre>

<ol start="3">
  <li>Отредактируйте файл <code>hosts</code> и укажите IP-адреса или доменные имена целевых серверов.</li>
  <li>Запустите playbook:</li>
</ol>

<pre><code>ansible-playbook -i hosts playbook.yml
</code></pre>

<h2>Описание задач</h2>

<h3>Установка MySQL</h3>

<ul>
  <li>Устанавливаются необходимые зависимости и пакет wget.</li>
  <li>Скачивается и устанавливается MySQL APT репозиторий.</li>
  <li>Импортируется GPG-ключ для репозитория MySQL.</li>
  <li>Добавляется официальный репозиторий MySQL.</li>
  <li>Устанавливается пакет mysql-server.</li>
</ul>

<h3>Установка и инициализация Nginx и PHP</h3>

<ul>
  <li>Устанавливается Nginx.</li>
  <li>Устанавливается PHP и необходимые расширения.</li>
  <li>Копируется конфигурационный файл для сайта и настраивается перезапуск Nginx при изменении.</li>
  <li>Создается папка для файлов веб-сайта.</li>
  <li>Создается файл phpinfo.php для вывода информации о PHP.</li>
</ul>

<h3>Вывод результата команды phpinfo()</h3>

<ul>
  <li>Выполняется команда phpinfo(), результат выводится в отладочной информации.</li>
</ul>

<h2>Поддержка</h2>

<p>Если у вас возникли проблемы или вопросы по использованию playbook, не стесняйтесь создавать Issue в репозитории.</p>

<h2>Лицензия</h2>

<p>MIT License</p>
