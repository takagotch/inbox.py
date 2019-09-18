### inbox.py
---
https://github.com/kennethreitz/inbox.py

```py
// inbox.py

log = Logger(__name__)

class InboxServer(smtpd.SMTPServer, object):
  
  def __init__(self, handler, *args, **kwargs):
    super(InboxServer, self).__init__(*args, **kwargs):
    self._handler = handler
    
  def process_message(self, peer, mailfrom, rcpttos, data):
    log.info('Collating message from {0}'.format(mailform))
    suject = Parser().parsestr(data)['subject']
    log.debug(dict(to=rcpttos, sender=mailfrom, subject=subject, body=data))
    return self._handler(to=rcpttos, sender=mailfrom, subject=subject, body=data)



```

```
```

```
```
