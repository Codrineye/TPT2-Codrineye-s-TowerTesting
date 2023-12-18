# Tower Testing full auto script

`v1.0.0`
This script was made to improve your tower testing experience by adding idling compatability so you can leave your game running in the background, and some qol improvements such as an autorestart, an auto exit and a hotkey that lets you open the stats menu so you can see your resources/s and your wave acceleration factor

## Requirements
- 8 Script slots
- 5 Impulses
- 2 Condition
- 41 Actions
- A seperate script that's made to make your blueprint work

## What does it do?

This AI cycles through another difficulty as soon as you die, and you can cycle through every regeon if you want.

## Usage
To Start the script press x. To stop the script press x again. You can press it with any window open, it waits until you're in town to activate. You see if it's active or not by looking at "Remain_In_Regeon".
As soon as you die or you exit tower testing, it takes you to another difficulty and when you go past impossible it cycles back to easy.
If you want the script to cycle through your regeons too, you just press "w" to toggle the switch. When the switch is true "Regeon_Cycling = true" every time it passes impossible it goes to the new regeon.
You can press 'r' to restart, press 'e' to exit and press 't' to show stats when in tower testing.
When you stop the script, it unsets everything so you'll need to press w again.

## Specifications
I've tested this program with winAI2.23 and winRP1.12+ that you can find here: https://discord.com/channels/488444879836413975/1094013225915396127/1094013225915396127. The script is dellayed intentionally so that the scripts made for your blueprint can complete its logic.

### Bundle Import:
```
KENvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpJbnN0YW50IFJlc3RhcnQBAAAABWtleS5yAAAAAAEAAAANdG93ZXIucmVzdGFydA==;JUNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpJbnN0YW50IEV4aXQBAAAABWtleS5lAAAAAAEAAAAKdG93ZXIuZXhpdA==;HkNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpTdGF0cwEAAAAFa2V5LnQBAAAAE2dhbWUuaXNUb3dlclRlc3RpbmcCAAAADGdlbmVyaWMud2FpdAhjb25zdGFudAOamZmZmZnJPw1nZW5lcmljLmNsaWNrDnZlYy5mcm9tQ29vcmRzEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlCmRvdWJsZS5taW4Oc2NyZWVuLndpZHRoLmQRYXJpdGhtZXRpYy5kb3VibGUIY29uc3RhbnQDgcdxHMdx/D8IY29uc3RhbnQEASoPc2NyZWVuLmhlaWdodC5kCGNvbnN0YW50BAEqDm9wdGlvbi51aS5zaXplCGNvbnN0YW50BAEqCGNvbnN0YW50AzMzMzMzM9M/EWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlCmRvdWJsZS5taW4Pc2NyZWVuLmhlaWdodC5kEWFyaXRobWV0aWMuZG91YmxlCGNvbnN0YW50AwAAAAAAAOI/CGNvbnN0YW50BAEqDnNjcmVlbi53aWR0aC5kCGNvbnN0YW50BAEqDm9wdGlvbi51aS5zaXplCGNvbnN0YW50BAEqCGNvbnN0YW50A/UiAd+8mti/CGNvbnN0YW50BAErD3NjcmVlbi5oZWlnaHQuZA==;JUNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpFbnRlciBSZWdlb24AAAAAAAAAAAcAAAARZ2VuZXJpYy53YWl0d2hpbGUPY29tcGFyaXNvbi5ib29sE2dhbWUuaXNUb3dlclRlc3RpbmcIY29uc3RhbnQEAnx8E3Rvd24ud2luZG93LmFueW9wZW4OZ2VuZXJpYy5nb3RvaWYIY29uc3RhbnQCYwAAAA9jb21wYXJpc29uLmJvb2wPZ2xvYmFsLmJvb2wuZ2V0CGNvbnN0YW50BA5SZWdlb25fQ3ljbGluZwhjb25zdGFudAQCPT0IY29uc3RhbnQBABB0b3duLndpbmRvdy5zaG93CGNvbnN0YW50BAx0b3dlcnRlc3RpbmcIY29uc3RhbnQBAQxnZW5lcmljLndhaXQIY29uc3RhbnQDmpmZmZmZyT8NZ2VuZXJpYy5jbGljaw52ZWMuZnJvbUNvb3JkcxFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZQpkb3VibGUubWluDnNjcmVlbi53aWR0aC5kEWFyaXRobWV0aWMuZG91YmxlCGNvbnN0YW50A4HHcRzHcfw/CGNvbnN0YW50BAEqD3NjcmVlbi5oZWlnaHQuZAhjb25zdGFudAQBKg5vcHRpb24udWkuc2l6ZQhjb25zdGFudAQBKghjb25zdGFudANcj8L1KFzXPxFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZQpkb3VibGUubWluD3NjcmVlbi5oZWlnaHQuZBFhcml0aG1ldGljLmRvdWJsZQhjb25zdGFudAMAAAAAAADiPwhjb25zdGFudAQBKg5zY3JlZW4ud2lkdGguZAhjb25zdGFudAQBKg5vcHRpb24udWkuc2l6ZQhjb25zdGFudAQBKghjb25zdGFudAOZFmzBFmzhvwhjb25zdGFudAQBKw9zY3JlZW4uaGVpZ2h0LmQMZ2VuZXJpYy53YWl0CGNvbnN0YW50A5qZmZmZmck/EHRvd24ud2luZG93LnNob3cIY29uc3RhbnQEDHRvd2VydGVzdGluZwhjb25zdGFudAEA;LENvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpSZWdlb24gQ3ljbGUgVG9nZ2xlAQAAAAVrZXkudwEAAAAPZ2xvYmFsLmJvb2wuZ2V0CGNvbnN0YW50BBBSZW1haW5fSW5fUmVnZW9uAQAAAA9nbG9iYWwuYm9vbC5zZXQIY29uc3RhbnQEDlJlZ2Vvbl9DeWNsaW5nD2NvbXBhcmlzb24uYm9vbA9nbG9iYWwuYm9vbC5nZXQIY29uc3RhbnQEDlJlZ2Vvbl9DeWNsaW5nCGNvbnN0YW50BAI9PQhjb25zdGFudAEA;KUNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpFbnRlciBEaWZmaWN1bHR5AAAAAAAAAAAFAAAAEHRvd24ud2luZG93LnNob3cIY29uc3RhbnQEDHRvd2VydGVzdGluZwhjb25zdGFudAEBDGdlbmVyaWMud2FpdAhjb25zdGFudAOamZmZmZnJPw1nZW5lcmljLmNsaWNrDnZlYy5mcm9tQ29vcmRzEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlCmRvdWJsZS5taW4Oc2NyZWVuLndpZHRoLmQRYXJpdGhtZXRpYy5kb3VibGUIY29uc3RhbnQDgcdxHMdx/D8IY29uc3RhbnQEASoPc2NyZWVuLmhlaWdodC5kCGNvbnN0YW50BAEqDm9wdGlvbi51aS5zaXplCGNvbnN0YW50BAEqCGNvbnN0YW50A5qZmZmZmd8/EWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlCmRvdWJsZS5taW4Pc2NyZWVuLmhlaWdodC5kEWFyaXRobWV0aWMuZG91YmxlCGNvbnN0YW50AwAAAAAAAOI/CGNvbnN0YW50BAEqDnNjcmVlbi53aWR0aC5kCGNvbnN0YW50BAEqDm9wdGlvbi51aS5zaXplCGNvbnN0YW50BAEqEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlEWdsb2JhbC5kb3VibGUuZ2V0CGNvbnN0YW50BAF5CGNvbnN0YW50BAEvCGNvbnN0YW50AwAAAAAAIHxACGNvbnN0YW50BAEtCGNvbnN0YW50AwAAAAAAAPA/CGNvbnN0YW50BAErD3NjcmVlbi5oZWlnaHQuZAxnZW5lcmljLndhaXQIY29uc3RhbnQDmpmZmZmZyT8NZ2VuZXJpYy5jbGljaw52ZWMuZnJvbUNvb3JkcxFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZQpkb3VibGUubWluDnNjcmVlbi53aWR0aC5kEWFyaXRobWV0aWMuZG91YmxlCGNvbnN0YW50A4HHcRzHcfw/CGNvbnN0YW50BAEqD3NjcmVlbi5oZWlnaHQuZAhjb25zdGFudAQBKg5vcHRpb24udWkuc2l6ZQhjb25zdGFudAQBKghjb25zdGFudAOuR+F6FK7LPxFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZQpkb3VibGUubWluD3NjcmVlbi5oZWlnaHQuZBFhcml0aG1ldGljLmRvdWJsZQhjb25zdGFudAMAAAAAAADiPwhjb25zdGFudAQBKg5zY3JlZW4ud2lkdGguZAhjb25zdGFudAQBKg5vcHRpb24udWkuc2l6ZQhjb25zdGFudAQBKghjb25zdGFudANHXk08Kxrpvwhjb25zdGFudAQBKw9zY3JlZW4uaGVpZ2h0LmQ=;KUNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpEaWZmaWN1bHR5IEN5Y2xlAAAAAAAAAAANAAAAEWdlbmVyaWMud2FpdHdoaWxlD2NvbXBhcmlzb24uYm9vbBN0b3duLndpbmRvdy5hbnlvcGVuCGNvbnN0YW50BAJ8fBNnYW1lLmlzVG93ZXJUZXN0aW5nEGxvY2FsLnN0cmluZy5zZXQIY29uc3RhbnQED2RpZmZpY3VsdHlfbGlzdAhjb25zdGFudAQkMjkwLjA7MjU2LjA7MjE3LjA7MTgyLjA7MTQ1LjA7MTEyLjA7DWxvY2FsLmludC5zZXQIY29uc3RhbnQEBmxlbmd0aA1zdHJpbmcubGVuZ3RoEGxvY2FsLnN0cmluZy5nZXQIY29uc3RhbnQED2RpZmZpY3VsdHlfbGlzdBFnZW5lcmljLndhaXR3aGlsZRNnYW1lLmlzVG93ZXJUZXN0aW5nDGdlbmVyaWMud2FpdAhjb25zdGFudAMAAAAAAAAAQBBsb2NhbC5zdHJpbmcuc2V0CGNvbnN0YW50BAF4CXN1YnN0cmluZxBsb2NhbC5zdHJpbmcuZ2V0CGNvbnN0YW50BA9kaWZmaWN1bHR5X2xpc3QOYXJpdGhtZXRpYy5pbnQNc3RyaW5nLmxlbmd0aBBsb2NhbC5zdHJpbmcuZ2V0CGNvbnN0YW50BA9kaWZmaWN1bHR5X2xpc3QIY29uc3RhbnQEAS0NbG9jYWwuaW50LmdldAhjb25zdGFudAQGbGVuZ3RoDmFyaXRobWV0aWMuaW50DnN0cmluZy5pbmRleE9mEGxvY2FsLnN0cmluZy5nZXQIY29uc3RhbnQED2RpZmZpY3VsdHlfbGlzdAhjb25zdGFudAQBOw5hcml0aG1ldGljLmludA1zdHJpbmcubGVuZ3RoCGNvbnN0YW50BA9kaWZmaWN1bHR5X2xpc3QIY29uc3RhbnQEAS0NbG9jYWwuaW50LmdldAhjb25zdGFudAQGbGVuZ3RoCGNvbnN0YW50BAErCGNvbnN0YW50AgEAAAARZ2xvYmFsLmRvdWJsZS5zZXQIY29uc3RhbnQEAXkDczJkCXN1YnN0cmluZxBsb2NhbC5zdHJpbmcuZ2V0CGNvbnN0YW50BAF4CGNvbnN0YW50AgAAAAAOYXJpdGhtZXRpYy5pbnQOc3RyaW5nLmluZGV4T2YQbG9jYWwuc3RyaW5nLmdldAhjb25zdGFudAQBeAhjb25zdGFudAQBOwhjb25zdGFudAIAAAAACGNvbnN0YW50BAEtCGNvbnN0YW50AgEAAAAIY29uc3RhbnQDAAAAAAAgckANbG9jYWwuaW50LnNldAhjb25zdGFudAQGbGVuZ3RoDmFyaXRobWV0aWMuaW50DWxvY2FsLmludC5nZXQIY29uc3RhbnQEBmxlbmd0aAhjb25zdGFudAQBLQ1zdHJpbmcubGVuZ3RoEGxvY2FsLnN0cmluZy5nZXQIY29uc3RhbnQEAXgTZ2VuZXJpYy5leGVjdXRlc3luYwhjb25zdGFudAQpQ29kcmluZXllJ3MgVG93ZXJUZXN0aW5nOkVudGVyIERpZmZpY3VsdHkRZ2VuZXJpYy53YWl0dW50aWwTZ2FtZS5pc1Rvd2VyVGVzdGluZw5nZW5lcmljLmdvdG9pZghjb25zdGFudAIEAAAADmNvbXBhcmlzb24uaW50DWxvY2FsLmludC5nZXQIY29uc3RhbnQEBmxlbmd0aAhjb25zdGFudAQCIT0IY29uc3RhbnQCAAAAABNnZW5lcmljLmV4ZWN1dGVzeW5jCGNvbnN0YW50BCVDb2RyaW5leWUncyBUb3dlclRlc3Rpbmc6RW50ZXIgUmVnZW9uDGdlbmVyaWMuZ290bwhjb25zdGFudAIBAAAA;JENvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpJbml0aWFsaXNlcgEAAAAFa2V5LngAAAAACwAAAA9nbG9iYWwuYm9vbC5zZXQIY29uc3RhbnQEEFJlbWFpbl9Jbl9SZWdlb24PY29tcGFyaXNvbi5ib29sD2dsb2JhbC5ib29sLmdldAhjb25zdGFudAQQUmVtYWluX0luX1JlZ2Vvbghjb25zdGFudAQCPT0IY29uc3RhbnQBAA5nZW5lcmljLmdvdG9pZghjb25zdGFudAJjAAAAD2NvbXBhcmlzb24uYm9vbA9nbG9iYWwuYm9vbC5nZXQIY29uc3RhbnQEEFJlbWFpbl9Jbl9SZWdlb24IY29uc3RhbnQEAj09CGNvbnN0YW50AQAPZ2VuZXJpYy5leGVjdXRlCGNvbnN0YW50BClDb2RyaW5leWUncyBUb3dlclRlc3Rpbmc6RGlmZmljdWx0eSBDeWNsZRFnZW5lcmljLndhaXR1bnRpbA9jb21wYXJpc29uLmJvb2wTZ2FtZS5pc1Rvd2VyVGVzdGluZwhjb25zdGFudAQCfHwPY29tcGFyaXNvbi5ib29sD2dsb2JhbC5ib29sLmdldAhjb25zdGFudAQQUmVtYWluX0luX1JlZ2Vvbghjb25zdGFudAQCPT0IY29uc3RhbnQBABFnZW5lcmljLndhaXR3aGlsZQ9jb21wYXJpc29uLmJvb2wRY29tcGFyaXNvbi5kb3VibGUMdG93ZXIuaGVhbHRoCGNvbnN0YW50AQAIY29uc3RhbnQEAT4IY29uc3RhbnQDAAAAAAAAAAAIY29uc3RhbnQEAiYmD2dsb2JhbC5ib29sLmdldAhjb25zdGFudAQQUmVtYWluX0luX1JlZ2Vvbgp0b3dlci5leGl0DmdlbmVyaWMuZ290b2lmCGNvbnN0YW50AgQAAAAPZ2xvYmFsLmJvb2wuZ2V0CGNvbnN0YW50BBBSZW1haW5fSW5fUmVnZW9uDGdlbmVyaWMuc3RvcAhjb25zdGFudAQpQ29kcmluZXllJ3MgVG93ZXJUZXN0aW5nOkRpZmZpY3VsdHkgQ3ljbGUMZ2xvYmFsLnVuc2V0CGNvbnN0YW50BAF5DGdsb2JhbC51bnNldAhjb25zdGFudAQQUmVtYWluX0luX1JlZ2VvbgxnbG9iYWwudW5zZXQIY29uc3RhbnQEDlJlZ2Vvbl9DeWNsaW5n```

| Name<br>-------------------  | Requirements<br><nobr>Impulses - Conditions - Actions</nobr><br>--------------------------------------  | Import Code  |
| :-------------------: | :------------: | :------------ |
| <nobr>Instant Restart</nobr>  | 1 - 0 - 1  |  <nobr>```KENvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpJbnN0YW50IFJlc3RhcnQBAAAABWtleS5yAAAAAAEAAAANdG93ZXIucmVzdGFydA==```</nobr> |
| <nobr>Instant Exit</nobr>  | 1 - 0 - 1  | <nobr>```JUNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpJbnN0YW50IEV4aXQBAAAABWtleS5lAAAAAAEAAAAKdG93ZXIuZXhpdA==```</nobr>|
| <nobr>Stats</nobr>  | 1 - 1 - 2  |<nobr>```HkNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpTdGF0cwEAAAAFa2V5LnQBAAAAE2dhbWUuaXNUb3dlclRlc3RpbmcCAAAADGdlbmVyaWMud2FpdAhjb25zdGFudAOamZmZmZnJPw1nZW5lcmljLmNsaWNrDnZlYy5mcm9tQ29vcmRzEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlCmRvdWJsZS5taW4Oc2NyZWVuLndpZHRoLmQRYXJpdGhtZXRpYy5kb3VibGUIY29uc3RhbnQDgcdxHMdx/D8IY29uc3RhbnQEASoPc2NyZWVuLmhlaWdodC5kCGNvbnN0YW50BAEqDm9wdGlvbi51aS5zaXplCGNvbnN0YW50BAEqCGNvbnN0YW50AzMzMzMzM9M/EWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlCmRvdWJsZS5taW4Pc2NyZWVuLmhlaWdodC5kEWFyaXRobWV0aWMuZG91YmxlCGNvbnN0YW50AwAAAAAAAOI/CGNvbnN0YW50BAEqDnNjcmVlbi53aWR0aC5kCGNvbnN0YW50BAEqDm9wdGlvbi51aS5zaXplCGNvbnN0YW50BAEqCGNvbnN0YW50A/UiAd+8mti/CGNvbnN0YW50BAErD3NjcmVlbi5oZWlnaHQuZA==```</nobr>|
| <nobr>Enter Regeon</nobr>  | 0 - 0 - 7  | <nobr>```JUNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpFbnRlciBSZWdlb24AAAAAAAAAAAcAAAARZ2VuZXJpYy53YWl0d2hpbGUPY29tcGFyaXNvbi5ib29sE2dhbWUuaXNUb3dlclRlc3RpbmcIY29uc3RhbnQEAnx8E3Rvd24ud2luZG93LmFueW9wZW4OZ2VuZXJpYy5nb3RvaWYIY29uc3RhbnQCYwAAAA9jb21wYXJpc29uLmJvb2wPZ2xvYmFsLmJvb2wuZ2V0CGNvbnN0YW50BA5SZWdlb25fQ3ljbGluZwhjb25zdGFudAQCPT0IY29uc3RhbnQBABB0b3duLndpbmRvdy5zaG93CGNvbnN0YW50BAx0b3dlcnRlc3RpbmcIY29uc3RhbnQBAQxnZW5lcmljLndhaXQIY29uc3RhbnQDmpmZmZmZyT8NZ2VuZXJpYy5jbGljaw52ZWMuZnJvbUNvb3JkcxFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZQpkb3VibGUubWluDnNjcmVlbi53aWR0aC5kEWFyaXRobWV0aWMuZG91YmxlCGNvbnN0YW50A4HHcRzHcfw/CGNvbnN0YW50BAEqD3NjcmVlbi5oZWlnaHQuZAhjb25zdGFudAQBKg5vcHRpb24udWkuc2l6ZQhjb25zdGFudAQBKghjb25zdGFudANcj8L1KFzXPxFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZQpkb3VibGUubWluD3NjcmVlbi5oZWlnaHQuZBFhcml0aG1ldGljLmRvdWJsZQhjb25zdGFudAMAAAAAAADiPwhjb25zdGFudAQBKg5zY3JlZW4ud2lkdGguZAhjb25zdGFudAQBKg5vcHRpb24udWkuc2l6ZQhjb25zdGFudAQBKghjb25zdGFudAOZFmzBFmzhvwhjb25zdGFudAQBKw9zY3JlZW4uaGVpZ2h0LmQMZ2VuZXJpYy53YWl0CGNvbnN0YW50A5qZmZmZmck/EHRvd24ud2luZG93LnNob3cIY29uc3RhbnQEDHRvd2VydGVzdGluZwhjb25zdGFudAEA```</nobr>|
| <nobr>Regeon Cycle Toggle</nobr>  | 0 - 0 - 5  | <nobr>```LENvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpSZWdlb24gQ3ljbGUgVG9nZ2xlAQAAAAVrZXkudwEAAAAPZ2xvYmFsLmJvb2wuZ2V0CGNvbnN0YW50BBBSZW1haW5fSW5fUmVnZW9uAQAAAA9nbG9iYWwuYm9vbC5zZXQIY29uc3RhbnQEDlJlZ2Vvbl9DeWNsaW5nD2NvbXBhcmlzb24uYm9vbA9nbG9iYWwuYm9vbC5nZXQIY29uc3RhbnQEDlJlZ2Vvbl9DeWNsaW5nCGNvbnN0YW50BAI9PQhjb25zdGFudAEA```</nobr>|
| <nobr>Enter Difficulty</nobr>  | 0 - 0 - 5  |  <nobr>```KUNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpFbnRlciBEaWZmaWN1bHR5AAAAAAAAAAAFAAAAEHRvd24ud2luZG93LnNob3cIY29uc3RhbnQEDHRvd2VydGVzdGluZwhjb25zdGFudAEBDGdlbmVyaWMud2FpdAhjb25zdGFudAOamZmZmZnJPw1nZW5lcmljLmNsaWNrDnZlYy5mcm9tQ29vcmRzEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlCmRvdWJsZS5taW4Oc2NyZWVuLndpZHRoLmQRYXJpdGhtZXRpYy5kb3VibGUIY29uc3RhbnQDgcdxHMdx/D8IY29uc3RhbnQEASoPc2NyZWVuLmhlaWdodC5kCGNvbnN0YW50BAEqDm9wdGlvbi51aS5zaXplCGNvbnN0YW50BAEqCGNvbnN0YW50A5qZmZmZmd8/EWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlCmRvdWJsZS5taW4Pc2NyZWVuLmhlaWdodC5kEWFyaXRobWV0aWMuZG91YmxlCGNvbnN0YW50AwAAAAAAAOI/CGNvbnN0YW50BAEqDnNjcmVlbi53aWR0aC5kCGNvbnN0YW50BAEqDm9wdGlvbi51aS5zaXplCGNvbnN0YW50BAEqEWFyaXRobWV0aWMuZG91YmxlEWFyaXRobWV0aWMuZG91YmxlEWdsb2JhbC5kb3VibGUuZ2V0CGNvbnN0YW50BAF5CGNvbnN0YW50BAEvCGNvbnN0YW50AwAAAAAAIHxACGNvbnN0YW50BAEtCGNvbnN0YW50AwAAAAAAAPA/CGNvbnN0YW50BAErD3NjcmVlbi5oZWlnaHQuZAxnZW5lcmljLndhaXQIY29uc3RhbnQDmpmZmZmZyT8NZ2VuZXJpYy5jbGljaw52ZWMuZnJvbUNvb3JkcxFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZQpkb3VibGUubWluDnNjcmVlbi53aWR0aC5kEWFyaXRobWV0aWMuZG91YmxlCGNvbnN0YW50A4HHcRzHcfw/CGNvbnN0YW50BAEqD3NjcmVlbi5oZWlnaHQuZAhjb25zdGFudAQBKg5vcHRpb24udWkuc2l6ZQhjb25zdGFudAQBKghjb25zdGFudAOuR+F6FK7LPxFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZRFhcml0aG1ldGljLmRvdWJsZQpkb3VibGUubWluD3NjcmVlbi5oZWlnaHQuZBFhcml0aG1ldGljLmRvdWJsZQhjb25zdGFudAMAAAAAAADiPwhjb25zdGFudAQBKg5zY3JlZW4ud2lkdGguZAhjb25zdGFudAQBKg5vcHRpb24udWkuc2l6ZQhjb25zdGFudAQBKghjb25zdGFudANHXk08Kxrpvwhjb25zdGFudAQBKw9zY3JlZW4uaGVpZ2h0LmQ=```</nobr>|
| <nobr>Difficulty Cycle</nobr>  | 0 - 0 - 13  |  <nobr>```KUNvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpEaWZmaWN1bHR5IEN5Y2xlAAAAAAAAAAANAAAAEWdlbmVyaWMud2FpdHdoaWxlD2NvbXBhcmlzb24uYm9vbBN0b3duLndpbmRvdy5hbnlvcGVuCGNvbnN0YW50BAJ8fBNnYW1lLmlzVG93ZXJUZXN0aW5nEGxvY2FsLnN0cmluZy5zZXQIY29uc3RhbnQED2RpZmZpY3VsdHlfbGlzdAhjb25zdGFudAQkMjkwLjA7MjU2LjA7MjE3LjA7MTgyLjA7MTQ1LjA7MTEyLjA7DWxvY2FsLmludC5zZXQIY29uc3RhbnQEBmxlbmd0aA1zdHJpbmcubGVuZ3RoEGxvY2FsLnN0cmluZy5nZXQIY29uc3RhbnQED2RpZmZpY3VsdHlfbGlzdBFnZW5lcmljLndhaXR3aGlsZRNnYW1lLmlzVG93ZXJUZXN0aW5nDGdlbmVyaWMud2FpdAhjb25zdGFudAMAAAAAAAAAQBBsb2NhbC5zdHJpbmcuc2V0CGNvbnN0YW50BAF4CXN1YnN0cmluZxBsb2NhbC5zdHJpbmcuZ2V0CGNvbnN0YW50BA9kaWZmaWN1bHR5X2xpc3QOYXJpdGhtZXRpYy5pbnQNc3RyaW5nLmxlbmd0aBBsb2NhbC5zdHJpbmcuZ2V0CGNvbnN0YW50BA9kaWZmaWN1bHR5X2xpc3QIY29uc3RhbnQEAS0NbG9jYWwuaW50LmdldAhjb25zdGFudAQGbGVuZ3RoDmFyaXRobWV0aWMuaW50DnN0cmluZy5pbmRleE9mEGxvY2FsLnN0cmluZy5nZXQIY29uc3RhbnQED2RpZmZpY3VsdHlfbGlzdAhjb25zdGFudAQBOw5hcml0aG1ldGljLmludA1zdHJpbmcubGVuZ3RoCGNvbnN0YW50BA9kaWZmaWN1bHR5X2xpc3QIY29uc3RhbnQEAS0NbG9jYWwuaW50LmdldAhjb25zdGFudAQGbGVuZ3RoCGNvbnN0YW50BAErCGNvbnN0YW50AgEAAAARZ2xvYmFsLmRvdWJsZS5zZXQIY29uc3RhbnQEAXkDczJkCXN1YnN0cmluZxBsb2NhbC5zdHJpbmcuZ2V0CGNvbnN0YW50BAF4CGNvbnN0YW50AgAAAAAOYXJpdGhtZXRpYy5pbnQOc3RyaW5nLmluZGV4T2YQbG9jYWwuc3RyaW5nLmdldAhjb25zdGFudAQBeAhjb25zdGFudAQBOwhjb25zdGFudAIAAAAACGNvbnN0YW50BAEtCGNvbnN0YW50AgEAAAAIY29uc3RhbnQDAAAAAAAgckANbG9jYWwuaW50LnNldAhjb25zdGFudAQGbGVuZ3RoDmFyaXRobWV0aWMuaW50DWxvY2FsLmludC5nZXQIY29uc3RhbnQEBmxlbmd0aAhjb25zdGFudAQBLQ1zdHJpbmcubGVuZ3RoEGxvY2FsLnN0cmluZy5nZXQIY29uc3RhbnQEAXgTZ2VuZXJpYy5leGVjdXRlc3luYwhjb25zdGFudAQpQ29kcmluZXllJ3MgVG93ZXJUZXN0aW5nOkVudGVyIERpZmZpY3VsdHkRZ2VuZXJpYy53YWl0dW50aWwTZ2FtZS5pc1Rvd2VyVGVzdGluZw5nZW5lcmljLmdvdG9pZghjb25zdGFudAIEAAAADmNvbXBhcmlzb24uaW50DWxvY2FsLmludC5nZXQIY29uc3RhbnQEBmxlbmd0aAhjb25zdGFudAQCIT0IY29uc3RhbnQCAAAAABNnZW5lcmljLmV4ZWN1dGVzeW5jCGNvbnN0YW50BCVDb2RyaW5leWUncyBUb3dlclRlc3Rpbmc6RW50ZXIgUmVnZW9uDGdlbmVyaWMuZ290bwhjb25zdGFudAIBAAAA```</nobr>|
| <nobr>Initialiser</nobr>  | 1 - 0 - 11  |  <nobr>```JENvZHJpbmV5ZSdzIFRvd2VyVGVzdGluZzpJbml0aWFsaXNlcgEAAAAFa2V5LngAAAAACwAAAA9nbG9iYWwuYm9vbC5zZXQIY29uc3RhbnQEEFJlbWFpbl9Jbl9SZWdlb24PY29tcGFyaXNvbi5ib29sD2dsb2JhbC5ib29sLmdldAhjb25zdGFudAQQUmVtYWluX0luX1JlZ2Vvbghjb25zdGFudAQCPT0IY29uc3RhbnQBAA5nZW5lcmljLmdvdG9pZghjb25zdGFudAJjAAAAD2NvbXBhcmlzb24uYm9vbA9nbG9iYWwuYm9vbC5nZXQIY29uc3RhbnQEEFJlbWFpbl9Jbl9SZWdlb24IY29uc3RhbnQEAj09CGNvbnN0YW50AQAPZ2VuZXJpYy5leGVjdXRlCGNvbnN0YW50BClDb2RyaW5leWUncyBUb3dlclRlc3Rpbmc6RGlmZmljdWx0eSBDeWNsZRFnZW5lcmljLndhaXR1bnRpbA9jb21wYXJpc29uLmJvb2wTZ2FtZS5pc1Rvd2VyVGVzdGluZwhjb25zdGFudAQCfHwPY29tcGFyaXNvbi5ib29sD2dsb2JhbC5ib29sLmdldAhjb25zdGFudAQQUmVtYWluX0luX1JlZ2Vvbghjb25zdGFudAQCPT0IY29uc3RhbnQBABFnZW5lcmljLndhaXR3aGlsZQ9jb21wYXJpc29uLmJvb2wRY29tcGFyaXNvbi5kb3VibGUMdG93ZXIuaGVhbHRoCGNvbnN0YW50AQAIY29uc3RhbnQEAT4IY29uc3RhbnQDAAAAAAAAAAAIY29uc3RhbnQEAiYmD2dsb2JhbC5ib29sLmdldAhjb25zdGFudAQQUmVtYWluX0luX1JlZ2Vvbgp0b3dlci5leGl0DmdlbmVyaWMuZ290b2lmCGNvbnN0YW50AgQAAAAPZ2xvYmFsLmJvb2wuZ2V0CGNvbnN0YW50BBBSZW1haW5fSW5fUmVnZW9uDGdlbmVyaWMuc3RvcAhjb25zdGFudAQpQ29kcmluZXllJ3MgVG93ZXJUZXN0aW5nOkRpZmZpY3VsdHkgQ3ljbGUMZ2xvYmFsLnVuc2V0CGNvbnN0YW50BAF5DGdsb2JhbC51bnNldAhjb25zdGFudAQQUmVtYWluX0luX1JlZ2VvbgxnbG9iYWwudW5zZXQIY29uc3RhbnQEDlJlZ2Vvbl9DeWNsaW5n```</nobr>|
