Install Laragon <br>
Install Composer <br>
Install PHPMyAdmin <br>
<br>
User name DB: quanlyphongtro <br>
Version DB PHPMYADMIN: utf8mb4_0900_ai_ci <br>
<br>
Edit file env: <br>
    DB_DATABASE=quanlyphongtro <br>
    DB_USERNAME=root <br>
    DB_PASSWORD= <br>
<br>
Run Terminal: <br>
    composer install<br>
    php artisan config:cache<br>
    php artisan serve<br>
<br>
<br>
Error:<br>
<br>
    PS D:\Web_QL_PhongTro_L10> composer install<br>
    Composer could not detect the root package (laravel/laravel) version, defaulting to '1.0.0'. See https://getcomposer.org/root-version<br>
    Installing dependencies from lock file (including require-dev)<br>
    Verifying lock file contents can be installed on current platform.<br>
    Your lock file does not contain a compatible set of packages. Please run composer update.<br>
<br>
    Problem 1<br>
        - symfony/css-selector is locked to version v7.0.3 and an update of this package was not requested.<br>
        - symfony/css-selector v7.0.3 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.<br>
    Problem 2<br>
        - symfony/event-dispatcher is locked to version v7.0.3 and an update of this package was not requested.<br>
        - symfony/event-dispatcher v7.0.3 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.<br>
    Problem 3<br>
        - symfony/string is locked to version v7.0.4 and an update of this package was not requested.<br>
        - symfony/string v7.0.4 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.<br>
    Problem 4<br>
        - symfony/yaml is locked to version v7.0.3 and an update of this package was not requested.<br>
        - symfony/yaml v7.0.3 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.<br>
    Problem 5<br>
        - symfony/string v7.0.4 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.<br>
        - symfony/console v6.4.6 requires symfony/string ^5.4|^6.0|^7.0 -> satisfiable by symfony/string[v7.0.4].<br>
        - symfony/console is locked to version v6.4.6 and an update of this package was not requested.<br>
<br>
<br>
Fix: composer install --ignore-platform-req=php<br>
