## Active Directory Authentication

The intent of this repository is to Login Active Directory Users into laravel application without saving them in database.

## Installation

#### 1. Clone Repo From Gitlab

```bash
git clone https://github.com/muzammilaskari/LDAP-AD-Authentication-Laravel.git
```

#### 2. Switch to the repo folder
```bash
cd LDAP-AD-Authentication-Laravel
```
   
#### 3. Install all the dependencies using composer
```bash
composer install
```

#### 4. Copy the .example.env file to .env
```bash
cp .env.example .env
```

#### 5. Make the required configuration changes in the .env file
Update following constants in .env
```bash
LDAP_SCHEMA=OpenLDAP
LDAP_HOSTS=ldap.forumsys.com
LDAP_BASE_DN=dc=example,dc=com
LDAP_USER_ATTRIBUTE=uid
LDAP_USER_FORMAT=uid=%s,dc=example,dc=com
LDAP_ACCOUNT_PREFIX=uid=
LDAP_ACCOUNT_SUFFIX=,dc=example,dc=com
LDAP_CONNECTION=default
```

#### 6. Generate a new application key
```bash
php artisan key:generate
```

#### 9. Set Permissions for laravel log
```bash
sudo chown -R $USER:www-data storage
sudo chown -R $USER:www-data bootstrap/cache

chmod -R 775 storage
chmod -R 775 bootstrap/cache
```
