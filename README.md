# python-sms-activate-ru


### Описание на русском ниже

Wrapper for automatic reception of SMS-messages by sms-activate.ru

[![N|Solid](https://img.shields.io/pypi/pyversions/smsactivateru.svg)](https://pypi.python.org/pypi/smsactivateru)

### Installation
You can install or upgrade package with:

$ pip install git+https://github.com/Spec122/python-sms-activate-ru/
```
### Example
```python
from smsactivateru import Sms, SmsService, GetNumber

wrapper = Sms('API KEY')

activation = GetNumber(
	service=SmsService().Youla,
).request(wrapper)

input('Press enter if you sms was sent')

activation.was_sent().request(wrapper)
code = activation.wait_code(wrapper=wrapper)
print(code)
```
More examples located in /example/ dir

----
Библиотека на python для работы с api сервиса автоматического приёма смс – sms-activate.ru

[![N|Solid](https://img.shields.io/pypi/pyversions/smsactivateru.svg)](https://pypi.python.org/pypi/smsactivateru)

### Установка
Установка с помощью стандартного пакетного менеджера pip:
```
$ pip install git+https://github.com/Spec122/python-sms-activate-ru/
```
### Простой пример
```python
from smsactivateru import Sms, SmsService, GetNumber

wrapper = Sms('API KEY')

activation = GetNumber(
	service=SmsService().Youla,
).request(wrapper)

input('Press enter if you sms was sent')

activation.was_sent().request(wrapper)
code = activation.wait_code(wrapper=wrapper)
print(code)
```
Это пример использует встроенный обработчик. Вы можете вручную устанавливать статусы и управлять процессом, а так же много чего ещё.
Больше примеров находится в папке /example/
