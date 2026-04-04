# Virtual environment

#### Create

```
python3 -m venv .venv
``` 

#### Activate

```
source .venv/bin/activate
```


# Claude Code

#### Install

```
curl -fsSL https://claude.ai/install.sh | bash
```

#### Connect Claude Code to Openrouter
You can configure Claude Code using a project-level settings file. Create the subdirectory .claude inside the project directory. Create settings.json file inside that subdirectory. The file should contain:

```
{
  "env": {
    "ANTHROPIC_BASE_URL": "https://openrouter.ai/api",
    "ANTHROPIC_AUTH_TOKEN": "<your-openrouter-api-key>",
    "ANTHROPIC_API_KEY": "",
    "ANTHROPIC_MODEL": "openrouter/free"
  }
}
```

#### Luch Claude Code

```
claude
```

# Flet

#### Install Flet
```
pip install 'flet[all]'
```

#### Create flet app
```
flet create
```

#### Run the app
```
flet run
```

```
flet run --web 
```

Utile mentre si sta scrivendo il codice perchè avvia l'app all'interno del browser e, dopo aver apportato modifiche al codice, basterà aggiornare il browser per vedere l'effetto (nella maggior parte delle tipologie di modifiche, ad esempio quelle grafiche)

```
flet run --android
```

Crea un QR code che può essere scansionato tramite mobile Android (dove preventivamente è stato installata l'app di Flet)


#### Build the app
E' importante che i pacchetti utilizzati siano nel file requirements.txt nella directory principale del progetto:

```
pip freeze > requirements.txt
```

Example:

```
flet build apk \ 
--project "nome dell'app" \
--org "com.nome organizzazione" \
--requirements pytubefix \
--include-assets assets
```

Android
```
flet build apk -v
```

iOS
```
flet build ipa -v
```

macOS
```
flet build macos -v
```

Linux
```
flet build linux -v
```

Windows
```
flet build windows -v
```
