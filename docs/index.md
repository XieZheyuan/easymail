# EasyMail Class
Make Send Mail Easy In Python 3
```python
try:
    #Import EasyMail
    import easyemail
except(ModuleNotFoundError,ImportError):
    #Use Folder Version
    from . import easymail

```
1、Send An Plain Email

```python
def sendPlain(client,
              receivers,
              text="",
              subject="",
              sender_name=None,
              receivers_name=None,
              encoding="utf-8"
              ):
    '''
    Send Plain Email
    :param client:EMAIL CLIENT(SMTPClient)
    :param receivers:the Receivers(str or list or tuple or frozenset)
    :param text:Email HTML Body
    :param subject:Email Subject
    :param sender_name:Email Sender's Name(From,Default value is sender Email Address)
    :param receivers_name:Email Receivers' Name(To,Default value is 1st Receivers)
    :param encoding:Text,Subject,sender_name,receivers_name 's encoding,default is 'utf-8'
    :return:Hasn't return
    '''
    pass
```
You can use this futc. to send an email,like this
```python
from easymail import *
client=SMTPClient("smtp.abc.com")#Your Email Server
client.login("def@abc.com","123456")#Your Email And Your Password
sendPlain(client,["ghi@abc.com"],"The Subject","HelloWorld","ghi","def","utf-8")
```
The HTML Futc.:
```python
def sendHTML(client:SMTPClient,
              receivers,
              text="",
              subject="",
              sender_name=None,
              receivers_name=None,
              encoding="utf-8"
              ):
    '''
    Send Plain Email
    :param client:EMAIL CLIENT(SMTPClient)
    :param receivers:the Receivers(str or list or tuple or frozenset)
    :param text:Email Body
    :param subject:Email Subject
    :param sender_name:Email Sender's Name(From,Default value is sender Email Address)
    :param receivers_name:Email Receivers' Name(To,Default value is 1st Receivers)
    :param encoding:Text,Subject,sender_name,receivers_name 's encoding,default is 'utf-8'
    :return:Hasn't return
    
    '''
    pass
```
Html is similar to the function of sending plain text, so I won't repeat it here.

send Any Text:
```python
def sendAnyText(client:SMTPClient,
              receivers,
                typeof="plain",
              text="",
              subject="",
              sender_name=None,
              receivers_name=None,
              encoding="utf-8"
              ):
    '''
    Send Plain Email
    :param client:EMAIL CLIENT(SMTPClient)
    :param receivers:the Receivers(str or list or tuple or frozenset)
    :param typeof:Mail Body Type(default:plain)
    :param text:Email Body
    :param subject:Email Subject
    :param sender_name:Email Sender's Name(From,Default value is sender Email Address)
    :param receivers_name:Email Receivers' Name(To,Default value is 1st Receivers)
    :param encoding:Text,Subject,sender_name,receivers_name 's encoding,default is 'utf-8'
    :return:Hasn't return
    '''
    pass
```
It's similar too!