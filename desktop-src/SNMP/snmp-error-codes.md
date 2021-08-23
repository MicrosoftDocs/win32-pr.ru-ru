---
title: Коды ошибок SNMP (SNMP. h)
description: Корпорация Майкрософт реализует следующие коды ошибок SNMP, определенные спецификацией SNMPv2C.
ms.assetid: 7e7e2bc0-a058-4853-b736-1946e64a0c4a
topic_type:
- apiref
api_name:
- SNMP_ERRORSTATUS_NOERROR
- SNMP_ERRORSTATUS_TOOBIG
- SNMP_ERRORSTATUS_NOSUCHNAME
- SNMP_ERRORSTATUS_BADVALUE
- SNMP_ERRORSTATUS_READONLY
- SNMP_ERRORSTATUS_GENERR
- SNMP_ERRORSTATUS_NOACCESS
- SNMP_ERRORSTATUS_WRONGTYPE
- SNMP_ERRORSTATUS_WRONGLENGTH
- SNMP_ERRORSTATUS_WRONGENCODING
- SNMP_ERRORSTATUS_WRONGVALUE
- SNMP_ERRORSTATUS_NOCREATION
- SNMP_ERRORSTATUS_INCONSISTENTVALUE
- SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE
- SNMP_ERRORSTATUS_COMMITFAILED
- SNMP_ERRORSTATUS_UNDOFAILED
- SNMP_ERRORSTATUS_AUTHORIZATIONERROR
- SNMP_ERRORSTATUS_NOTWRITABLE
- SNMP_ERRORSTATUS_INCONSISTENTNAME
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583394dfc3093f4f0d5cf3d7c7cef68d7ff6d57930e3abf957d857defec227c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008932"
---
# <a name="snmp-error-codes"></a>Коды ошибок SNMP

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. вместо этого используйте [служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Корпорация Майкрософт реализует следующие коды ошибок SNMP, определенные спецификацией SNMPv2C.



| Константа/значение                                                                                                                                                                                                                                                                              | Описание                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_ERRORSTATUS_NOERROR"></span><span id="snmp_errorstatus_noerror"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС, \_ Ошибка**</dt> <dt>0</dt> </dl>                                      | Агент сообщает о том, что во время передачи не возникали ошибки.<br/>                                                                                      |
| <span id="SNMP_ERRORSTATUS_TOOBIG"></span><span id="snmp_errorstatus_toobig"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ тубиг**</dt> <dt>1</dt> </dl>                                         | Агенту не удалось разместить результаты запрошенной операции SNMP в одном SNMP-сообщении.<br/>                                                     |
| <span id="SNMP_ERRORSTATUS_NOSUCHNAME"></span><span id="snmp_errorstatus_nosuchname"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ носучнаме**</dt> <dt>2</dt> </dl>                             | Запрошенная операция SNMP определила неизвестную переменную.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_BADVALUE"></span><span id="snmp_errorstatus_badvalue"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ бадвалуе**</dt> <dt>3</dt> </dl>                                   | Запрошенная операция SNMP попыталась изменить переменную, но она указала либо синтаксис, либо значение ошибки.<br/>                                            |
| <span id="SNMP_ERRORSTATUS_READONLY"></span><span id="snmp_errorstatus_readonly"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ только для чтения**</dt> <dt>4</dt> </dl>                                   | Запрошенная операция SNMP попыталась изменить переменную, которая не может быть изменена в соответствии с профилем сообщества переменной.<br/>         |
| <span id="SNMP_ERRORSTATUS_GENERR"></span><span id="snmp_errorstatus_generr"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ женерр**</dt> <dt>5</dt> </dl>                                         | В ходе запрошенной операции SNMP возникла ошибка, отличная от перечисленных ниже.<br/>                                                          |
| <span id="SNMP_ERRORSTATUS_NOACCESS"></span><span id="snmp_errorstatus_noaccess"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ НЕдоступно**</dt> <dt>6</dt> </dl>                                   | Указанная переменная SNMP недоступна.<br/>                                                                                                      |
| <span id="SNMP_ERRORSTATUS_WRONGTYPE"></span><span id="snmp_errorstatus_wrongtype"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ вронгтипе**</dt> <dt>7</dt> </dl>                                | Значение указывает тип, который не согласуется с типом, необходимым для переменной.<br/>                                                            |
| <span id="SNMP_ERRORSTATUS_WRONGLENGTH"></span><span id="snmp_errorstatus_wronglength"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ вронгленгс**</dt> <dt>8</dt> </dl>                          | Значение указывает длину, которая не согласуется с длиной, необходимой для переменной.<br/>                                                        |
| <span id="SNMP_ERRORSTATUS_WRONGENCODING"></span><span id="snmp_errorstatus_wrongencoding"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ вронженкодинг**</dt> <dt>9</dt> </dl>                    | Значение содержит абстрактный синтаксис нотации One (ASN. 1), который не согласуется с тегом ASN. 1 поля.<br/>                           |
| <span id="SNMP_ERRORSTATUS_WRONGVALUE"></span><span id="snmp_errorstatus_wrongvalue"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ вронгвалуе**</dt> <dt>10</dt> </dl>                            | Значение не может быть присвоено переменной.<br/>                                                                                                       |
| <span id="SNMP_ERRORSTATUS_NOCREATION"></span><span id="snmp_errorstatus_nocreation"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС ( \_ Создание**</dt> ) <dt>11</dt> </dl>                            | Переменная не существует, и агент не может ее создать.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></span><span id="snmp_errorstatus_inconsistentvalue"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ инконсистентвалуе**</dt> <dt>12</dt> </dl>       | Значение не согласуется со значениями других управляемых объектов.<br/>                                                                                     |
| <span id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></span><span id="snmp_errorstatus_resourceunavailable"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ ресаурцеунаваилабле**</dt> <dt>13</dt> </dl> | Присвоение значения переменной требует выделения ресурсов, которые в данный момент недоступны.<br/>                                                |
| <span id="SNMP_ERRORSTATUS_COMMITFAILED"></span><span id="snmp_errorstatus_commitfailed"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ коммитфаилед**</dt> <dt>14</dt> </dl>                      | Ошибки проверки не обнаружены, но переменные не были обновлены.<br/>                                                                                       |
| <span id="SNMP_ERRORSTATUS_UNDOFAILED"></span><span id="snmp_errorstatus_undofailed"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ ундофаилед**</dt> <dt>15</dt> </dl>                            | Ошибки проверки не обнаружены. Некоторые переменные были обновлены, так как их назначение невозможно отменить.<br/>                                    |
| <span id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></span><span id="snmp_errorstatus_authorizationerror"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ AUTHORIZATIONERROR**</dt> <dt>16</dt> </dl>    | Произошла ошибка авторизации.<br/>                                                                                                                    |
| <span id="SNMP_ERRORSTATUS_NOTWRITABLE"></span><span id="snmp_errorstatus_notwritable"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ нотвритабле**</dt> <dt>17</dt> </dl>                         | Переменная существует, но агент не может изменить ее.<br/>                                                                                                 |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></span><span id="snmp_errorstatus_inconsistentname"></span><dl> <dt>**Протокол SNMP \_ ЕРРОРСТАТУС \_ инконсистентнаме**</dt> <dt>18</dt> </dl>          | Переменная не существует; Агент не может создать его, так как именованный экземпляр объекта не согласуется со значениями других управляемых объектов.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                        |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Протокол SNMP. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Обзор протокола SNMP](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Справочник по SNMP](snmp-reference.md)
</dt> </dl>

 

