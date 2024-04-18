Install Laragon
Install Composer
Install PHPMyAdmin

User name DB: quanlyphongtro
Version DB PHPMYADMIN: utf8mb4_0900_ai_ci

Edit file env:
    DB_DATABASE=quanlyphongtro
    DB_USERNAME=root
    DB_PASSWORD=

Run Terminal: 
    composer install
    php artisan config:cache
    php artisan serve


Error:

    PS D:\Web_QL_PhongTro_L10> composer install
    Composer could not detect the root package (laravel/laravel) version, defaulting to '1.0.0'. See https://getcomposer.org/root-version
    Installing dependencies from lock file (including require-dev)
    Verifying lock file contents can be installed on current platform.
    Your lock file does not contain a compatible set of packages. Please run composer update.

    Problem 1
        - symfony/css-selector is locked to version v7.0.3 and an update of this package was not requested.
        - symfony/css-selector v7.0.3 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.
    Problem 2
        - symfony/event-dispatcher is locked to version v7.0.3 and an update of this package was not requested.
        - symfony/event-dispatcher v7.0.3 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.
    Problem 3
        - symfony/string is locked to version v7.0.4 and an update of this package was not requested.
        - symfony/string v7.0.4 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.
    Problem 4
        - symfony/yaml is locked to version v7.0.3 and an update of this package was not requested.
        - symfony/yaml v7.0.3 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.
    Problem 5
        - symfony/string v7.0.4 requires php >=8.2 -> your php version (8.1.10) does not satisfy that requirement.
        - symfony/console v6.4.6 requires symfony/string ^5.4|^6.0|^7.0 -> satisfiable by symfony/string[v7.0.4].
        - symfony/console is locked to version v6.4.6 and an update of this package was not requested.


Fix: composer install --ignore-platform-req=php