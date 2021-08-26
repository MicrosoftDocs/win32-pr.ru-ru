---
description: Перечисляет типы ACE, определенные в данный момент.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa93490c4cf74ac33e3b15eeb888f011f81aa2b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470990"
---
# <a name="ace"></a>ТУЗ

**ACE** — это [*запись управления доступом*](/windows/desktop/SecGloss/a-gly) в [*списке управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL).

В следующей таблице перечислены определенные в данный момент типы **ACE** .




| Тип ACE | Структура | Тип ACL | 
|----------|-----------|----------|
| <ul><li>Доступ разрешен</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a> | Разграничительного | 
| <ul><li>Доступ разрешен</li><li>Разрешает обратный вызов во время проверки доступа</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a> | Разграничительного | 
| <ul><li>Доступ разрешен</li><li>Для конкретного объекта</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a> | Разграничительного | 
| <ul><li>Доступ разрешен</li><li>Для конкретного объекта</li><li>Разрешает обратный вызов во время проверки доступа</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a> | Разграничительного | 
| <ul><li>Доступ запрещен</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a> | Разграничительного | 
| <ul><li>Доступ запрещен</li><li>Разрешает обратный вызов во время проверки доступа</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a> | Разграничительного | 
| <ul><li>Доступ запрещен</li><li>Для конкретного объекта</li><li>Разрешает обратный вызов во время проверки доступа</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a> | Разграничительного | 
| <ul><li>Доступ запрещен</li><li>Для конкретного объекта</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a> | Разграничительного | 
| <ul><li>Системный сигнал</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a> | Система | 
| <ul><li>Системный сигнал</li><li>Разрешает обратный вызов во время проверки доступа</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a> | Система | 
| <ul><li>Системный сигнал</li><li>Для конкретного объекта</li><li>Разрешает обратный вызов во время проверки доступа</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a> | Система | 
| <ul><li>Системный сигнал</li><li>Для конкретного объекта</li></ul> | <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a> | Система | 
| <ul><li>Аудит системы</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a> | Система | 
| <ul><li>Аудит системы</li><li>Разрешает обратный вызов во время проверки доступа</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a> | Система | 
| <ul><li>Аудит системы</li><li>Для конкретного объекта</li><li>Разрешает обратный вызов во время проверки доступа</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a> | Система | 
| <ul><li>Аудит системы</li><li>Для конкретного объекта</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a> | Система | 




 

Системные оповещения и элементы управления оповещениями системы не поддерживаются в настоящее время.

> [!Note]  
> Каждая запись ACE начинается с [**структуры \_ заголовка ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . Формат данных, следующих за заголовком, различается в зависимости от типа ACE, указанного в заголовке.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>Winnt. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

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

