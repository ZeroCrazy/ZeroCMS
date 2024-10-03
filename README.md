ZeroCMS v2
=========
[![N|Solid](https://i.imgur.com/R0MLVn3.png)](https://zerocms.codetech.es)

[![Github All Releases](https://img.shields.io/github/downloads/ZeroCrazy/ZeroCMS/total.svg)]()
[![GitHub release](https://img.shields.io/github/release/ZeroCrazy/ZeroCMS.svg?color=%23f17e3f)]()
[![License](https://img.shields.io/github/license/ZeroCrazy/ZeroCMS.svg?color=%230d7ebf)]()
![Discord](https://img.shields.io/discord/1291085167871655977?style=for-the-badge)


ZeroCMS es un sistema de gestión de contenido (CMS) de código abierto, diseñado específicamente para servidores privados de juegos en línea, con una optimización especial para **Metin2**. El proyecto ofrece múltiples funcionalidades y está pensado para administradores que buscan una solución robusta y personalizable.

## Requisitos
Antes de instalar y ejecutar ZeroCMS, asegúrate de contar con los siguientes requisitos:

- **Servidor Web**: Apache o Nginx
- **PHP**: Versión 7.4 o superior
- **Base de Datos**: MySQL 5.7 o superior
- **Extensiones PHP**: `PDO`, `cURL`, `GD`, `mbstring`
- **Composer**: Para la gestión de dependencias
Es recomendable tener configurado un entorno de servidor optimizado para garantizar el buen rendimiento de ZeroCMS.

## Instalación
1. Clona este repositorio:
   ```bash
   git clone https://github.com/ZeroCrazy/ZeroCMS.git


## Idiomas
Actualmente contamos con **3** traducciones:

  - [![N|Solid](https://flagcdn.com/16x12/es.png)](#) Spanish
  - [![N|Solid](https://flagcdn.com/16x12/us.png)](#) English
  - [![N|Solid](https://flagcdn.com/16x12/ro.png)](#) Română

Si deseas colaborar, puedes traducir el sistema a tu idioma y enviarnos la traducción.

## Configuración
**Edita el archivo `inc/config.php` con la configuración de tu base de datos y del sitio web:**

<details><summary>Ver configuración</summary>
  
```sh
<?php

    $config = [
        # Project name
        "name" => "ZeroCMS",
        # URL (replace 'default' with the theme you will use)
        "url" => "http://localhost",
        "cdn" => "http://localhost/pages/default/assets",
        "api" => "http://localhost/api",
        # Theme
        "theme" => "default",
        # Language
        "lang" => "es",
        # Database
        "database" => [
            "player" => "player",
            "common" => "common",
            "account" => "account",
            "log" => "log",
            "host" => "localhost",
            "user" => "root",
            "pass" => "",
            "sqlite_file" => dirname(__DIR__, 1) . "/inc/db/site.db"
        ],
        # Google Captcha, Analytics & AdSense
        # Leave 'public' and 'secret' empty if you do not want to use Google Captcha
        "google" => [
            "captcha" => [
                "theme" => "light",
                "public" => "CODE_HERE",
                "secret" => "CODE_HERE"
            ],
            "tag" => "G-CODE_HERE",
            "ads" => ""
        ],
        # Social URL's
        "social" => [
            "discord" => "#zerocrazy",
            "facebook" => "https://www.facebook.com/codetechES/",
            "youtube" => "",
            "instagram" => "https://www.instagram.com/ggz998/",
            "twitter" => "https://twitter.com/ZeroCrazy",
            "tiktok" => "https://www.tiktok.com/@daniel98gd",
            "twitch" => "https://www.twitch.tv/zero_crazy",
            "forum" => null
        ],
        # Mail settings
        "email" => [
            "SMTPAuth" => true,
            "SMTPSecure" => "", # ssl, tls or ""
            "host" => "mail.servername.ltd",
            "port" => 25,
            "username" => "MAIL_USERNAME",
            "password" => "MAIL_PASSWORD"
        ],
        # Payment methods
        "payments" => [
            "stripe" => [
                "mode" => "sandbox",
                "currency" => "EUR",
                "apiKey" => [
                    "live" => [
                        "public" => "",
                        "secret" => ""
                    ],
                    "sandbox" => [
                        "public" => "",
                        "secret" => ""
                    ]
                ]
            ],
            "paypal" => [
                "mode" => "sandbox",
                "clientId" => "",
                "secret" => "",
                "currency" => "EUR",
                "url" => [
                    "sandbox" => "https => //api-m.sandbox.paypal.com",
                    "live" => "https => //api-m.paypal.com"
                ]
            ],
        ]
    ];

?>
```
</details>
