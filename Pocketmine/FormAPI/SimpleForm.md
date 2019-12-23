# SimpleForm

Erstmal musst du use jojoe77777\FormAPI importieren.

Dann hier ein Beispiel:
```php
   public function openHelpUI($player) { // Erstellen der Function
        $form = new SimpleForm(function (Player $player, int $data = null){
 
            $result = $data;
            if($result === null){
                return true;
            }
            switch($result){
                case 0: // Damit defenieren wir was der Button macht
                    break;
            }
 
        });
 
        $form->setTitle("Titel");
        $form->setContent("Beschreibung");
        $form->addButton("Schließen");
        $form->sendToPlayer($player);
        return $form;
    }
```

Um jetzt darauf zuzugreifen musst du das nutzenn:
```php
$this->openHelpUI($player);
```
