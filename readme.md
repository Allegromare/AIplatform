# Virtual environment

### Create

```

python3 -m venv .venv

``` 

### Activate

```

source .venv/bin/activate

```


# Claude Code

### Install

```curl -fsSL https://claude.ai/install.sh | bash```

### Connect Claude Code to Openrouter
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
### Luch Claude Code

```claude```
