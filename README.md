# Peasy Logs
Easily ship your **Python** print statements to your favorite chat bot.

## About
**Peasy Logs** listens to your function's `print` statements and sends a request for each of them.
While this is not very performant, it is a great way for periodic tasks that need to be watched.

- No need to setup complicated logging infrastructure

- Use the chat tools you already own for simple logging messages

## Supported chat bots
- [Google Chat](https://developers.google.com/chat/how-tos/webhooks)

## Use Cases
- Check that your script is running
- Let your users know about the status of your script

## Usage
Send your print statements the easy way:
```python
from peasy_logs import GChatConnector, LogShipper

connector = GChatConnector('<your-webhook-url>')
log_shipper = LogShipper(connector)

@log_shipper
def function_to_log():
    print("This print message will be send to the chat")
```
