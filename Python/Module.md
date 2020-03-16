# Module

## Make custom module and import
- package name = name of parent directory
- use absolute import
```python
from package1.package2.filename import classname 
from package1.package2.filename import funcname
```

## ABC
- Useful as interface class in python
- https://docs.python.org/ko/3.6/library/abc.html
```python
import abc


class MailSender:
    __metaclass__ = abc.ABCMeta
    
    @abc.abstractmethod
    def send(self, sender, receiver, subject, body):
        pass



class MockMailSender(MailSender):
    def send(self, sender, receiver, subject, body):
        #...



class SmtpMailSender(MailSender):
    def send(self, sender, receiver, subject, body):
        #...
```
