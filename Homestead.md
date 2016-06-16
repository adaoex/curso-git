# Homestead Global
=====

Instalação global via composer, da versão com suporte a PHP 7
```
composer global require laravel/homestead=3.0.2
```

Configurando comando homestead
```
$ cd ~\AppData\Roaming\Composer\vendor\laravel\homestead
$ bash init.sh
```
Criará a pasta .homestead/ na pasta do usuário


```
alias homestead='function __homestead() { (cd ~/AppData/Roaming/Composer/vendor/laravel/homestead && vagrant $*); unset -f __homestead; }; __homestead'
```

Subindo VM do Vagrant
```
homestead up
```

Parando VM do Vagrant
```
homestead halt
```


Acesso via SSH
--------------
```
homestead ssh
```

MySQL
-----
```
mysql -uhomestead -psecret
```
