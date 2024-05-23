# HuggingChat Fallback Skill

When in doubt, ask HuggingChat, powered by [HuggingChat Solver](https://github.com/femelo/ovos-solver-plugin-hugchat-persona).

You need to configure an `email` and `password` for your [Hugging Face](https://huggingface.co) account.

## About

Capabilities:

- Remembers what user said earlier in the conversation
- Can augment the answer with web content
- Trained to decline inappropriate requests

Limitations:

- May occasionally generate incorrect information
- May occasionally produce harmful instructions or biased content

## Configuration

Under skill settings (`.config/mycroft/skills/skill-ovos-fallback-hugchat.femelo/settings.json`) you can tweak some parameters for HuggingChat.

| Option          | Value                                                                  | Description                             |
| --------------- | ---------------------------------------------------------------------- | --------------------------------------- |
| `email`         | `your-hf-email`                                                        | Your `email` to access Hugging Face     |
| `password`      | `your-hf-password`                                                     | Your `password` to access Hugging Face  |
| `persona`       | `You are a helpful assistant who gives very short but factual answers` | Give a personality to HuggingChat       |
| `model`         | `llama-3`                                                              | LLM model to use                        |
| `enable_memory` | `true`                                                                 | Remember the last generated outputs     |
| `memory_size`   | `15`                                                                   | How many interactions to keep           |
| `web_search`    | `false`                                                                | Allow assistant to search the web       |
| `name`          | `AI assistant`                                                         | Name to give to the AI assistant        |
| `confirmation`  | `true`                                                                 | Spoken confirmation                     |

Read more about it in the OVOS technical manual, page [persona server](https://openvoiceos.github.io/ovos-technical-manual/persona_server/#compatible-projects)

The default persona is `You are a helpful voice assistant with a friendly tone and fun sense of humor. You respond in 40 words or fewer`

## Configurations

The skill utilizes the `~/.config/mycroft/skills/skill-ovos-fallback-hugchat.femelo/settings.json` file which allows you to configure it.

### Configuration for use with HuggingChat

```json
{
  "email": "{your-hf-email}",
  "password": "{your-hf-password}",
  "model": "llama-3",
  "persona": "You are a helpful voice assistant with a friendly tone and fun sense of humor",
  "enable_memory": true,
  "memory_size": 15,
  "web_search": false,
  "__mycroft_skill_firstrun": false
}
```

## Examples

- "Explain quantum computing in simple terms"
- "Got any creative ideas for a 10 year old’s birthday?"
