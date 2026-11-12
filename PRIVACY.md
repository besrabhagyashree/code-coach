# Privacy

Code Coach runs on your PC. It has no server, account system or analytics of its own.

## What leaves your PC

**Only when you press a shortcut or a Code Coach button**, Code Coach sends one request to **Anthropic's API**
using **your** API key. The request contains:

- a screenshot of the window you were working in (usually your browser with the problem and your code),
- that window's title,
- what you asked for (e.g. "Hint level 2", or the question you typed),
- the earlier messages in the current problem's conversation.

The first time you ask about a problem, one more request (with the same screenshot) creates its journal summary.

These requests are handled under Anthropic's terms and privacy policy for API use:
<https://www.anthropic.com/legal/privacy>.

**Nothing is sent to the author of Code Coach**, and Code Coach does not monitor your screen in the background.

## What stays on your PC

| Data | Location |
|---|---|
| API key | Windows Credential Manager, entry `CodeCoach/AnthropicAPIKey` |
| Settings | `%APPDATA%\CodeCoach\settings.json` |
| Problem journal | `%APPDATA%\CodeCoach\journal\` |
| Logs | `%APPDATA%\CodeCoach\logs\` |

Screenshots are not saved to disk.

## Tips

- Close or cover anything private before pressing a shortcut. The screenshot includes whatever is visible in the
  captured window.
- To remove everything: in Settings click **Remove key**, then delete `%APPDATA%\CodeCoach`.
