---
description: Перечисляет типы ACE, определенные в данный момент.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de555170bc8b7c1594b38adaa95d19b7e9ace54c8241fc971ea9f5383cf3e115
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785223"
---
# <a name="ace"></a>ТУЗ

**ACE** — это [*запись управления доступом*](/windows/desktop/SecGloss/a-gly) в [*списке управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL).

В следующей таблице перечислены определенные в данный момент типы **ACE** .



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип ACE</th>
<th>Структура</th>
<th>Тип ACL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Доступ разрешен</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></td>
<td>Разграничительного</td>
</tr>
<tr class="even">
<td><ul>
<li>Доступ разрешен</li>
<li>Разрешает обратный вызов во время проверки доступа</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></td>
<td>Разграничительного</td>
</tr>
<tr class="odd">
<td><ul>
<li>Доступ разрешен</li>
<li>Для конкретного объекта</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></td>
<td>Разграничительного</td>
</tr>
<tr class="even">
<td><ul>
<li>Доступ разрешен</li>
<li>Для конкретного объекта</li>
<li>Разрешает обратный вызов во время проверки доступа</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Разграничительного</td>
</tr>
<tr class="odd">
<td><ul>
<li>Доступ запрещен</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></td>
<td>Разграничительного</td>
</tr>
<tr class="even">
<td><ul>
<li>Доступ запрещен</li>
<li>Разрешает обратный вызов во время проверки доступа</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></td>
<td>Разграничительного</td>
</tr>
<tr class="odd">
<td><ul>
<li>Доступ запрещен</li>
<li>Для конкретного объекта</li>
<li>Разрешает обратный вызов во время проверки доступа</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Разграничительного</td>
</tr>
<tr class="even">
<td><ul>
<li>Доступ запрещен</li>
<li>Для конкретного объекта</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></td>
<td>Разграничительного</td>
</tr>
<tr class="odd">
<td><ul>
<li>Системный сигнал</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></td>
<td>Система</td>
</tr>
<tr class="even">
<td><ul>
<li>Системный сигнал</li>
<li>Разрешает обратный вызов во время проверки доступа</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></td>
<td>Система</td>
</tr>
<tr class="odd">
<td><ul>
<li>Системный сигнал</li>
<li>Для конкретного объекта</li>
<li>Разрешает обратный вызов во время проверки доступа</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Система</td>
</tr>
<tr class="even">
<td><ul>
<li>Системный сигнал</li>
<li>Для конкретного объекта</li>
</ul></td>
<td><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></td>
<td>Система</td>
</tr>
<tr class="odd">
<td><ul>
<li>Аудит системы</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></td>
<td>Система</td>
</tr>
<tr class="even">
<td><ul>
<li>Аудит системы</li>
<li>Разрешает обратный вызов во время проверки доступа</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></td>
<td>Система</td>
</tr>
<tr class="odd">
<td><ul>
<li>Аудит системы</li>
<li>Для конкретного объекта</li>
<li>Разрешает обратный вызов во время проверки доступа</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Система</td>
</tr>
<tr class="even">
<td><ul>
<li>Аудит системы</li>
<li>Для конкретного объекта</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></td>
<td>Система</td>
</tr>
</tbody>
</table>



 

Системные оповещения и элементы управления оповещениями системы не поддерживаются в настоящее время.

> [!Note]  
> Каждая запись ACE начинается с [**структуры \_ заголовка ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . Формат данных, следующих за заголовком, различается в зависимости от типа ACE, указанного в заголовке.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winnt. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аддаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**ДОСТУП к \_ разрешенному \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**ДОСТУП \_ запрещен \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**\_ACE системного оповещения \_**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**\_ACE аудита \_ системы**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

