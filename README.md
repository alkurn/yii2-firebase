Firebase Helper for Yii2
========================

Yii2 helper for creating firebase connection on real time.

Installation
------------
The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

* Either run

```
php composer.phar require --prefer-dist alkurn/yii2-firebase "dev-master"
```
or add

```json
"alkurn/yii2-firebase":"dev-master"
```

to the require section of your application's `composer.json` file.

* Add a new component in `components` section of your application's configuration file (optional), for example:

```php
'components' => [
    'firebase' => [
            'class' => 'alkurn\firebase\Firebase',
            'credential_file' => 'uploads/firebase-credential.json',
            'database_uri' => 'https://firebase-db.firebaseio.com', // (optional)
        ], 
],
```

and in `bootstrap` section, for example:

```php
'bootstrap' => ['log','firebase'],
```

It is necessary if you want to set global helper's settings for the application.

Usage
-----
For example:

```php
$db = Yii::$app->firebase->getDatabase();
```


