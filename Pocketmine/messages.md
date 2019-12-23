Messages senden: So geht´s!

Im ersten schritt müssen wir erstmal einen Command Registrieren. Das macht Ihr in der plugin.yml so:
```php
commands:
  codingschule:
    description: CodingSchule Beispiel
    usage: /cs
    aliases:
      - cs
```

Dannach erstellst du eine neue Funktion in der Main mit dem Namen
```php
"onCommand". Das geht wiefolgt:
public function onCommand(CommandSender $sender, Command $command, string $label, array $args): bool{}
```

Nachdem du diese Funktion erstellt hasst musst du ja auch noch wissen wie der Command lautet, das ganze macht man so:
```php
if ($command->getName() === "codingschule"){}
```

Jetzt musst du noch in die if deine Naricht eintargen die gesendet werden soll, das ganze machst du so:
```php
$sender->sendMessage("$msg");
```

Zuletzt musst du noch ein "return true" am Ende der Funktion hinpacken. 
Glückwunsch! Jetzt hast du einen Command Registriert welcher dir eine Naricht schickt wenn du diesen ausführst.

Falls du es nochmal in voller länge sehen willst, hier ist der Code:
```php
public function onCommand(CommandSender $sender, Command $command, string $label, array $args): bool{
        if ($command->getName() === "codingschule"){
            $sender->sendMessage("$msg");
        }
        return true;
    }
 ```
