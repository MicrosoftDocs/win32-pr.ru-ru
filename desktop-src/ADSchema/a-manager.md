---
title: Атрибут Manager
description: Содержит различающееся имя пользователя, который является руководителем пользователя. Объект-пользователь руководителя содержит свойство directReports, содержащее ссылки на все объекты user, для свойств диспетчера которых задано это различающееся имя.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута диспетчера
- Схема AD атрибута диспетчера
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b17f3252963e03c86b5b25a3651606a004afe672f1c8ec07f419ddff3a826
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301264"
---
# <a name="manager-attribute"></a>Атрибут Manager

Содержит различающееся имя пользователя, который является руководителем пользователя. Объект-пользователь руководителя содержит свойство directReports, содержащее ссылки на все объекты user, для свойств диспетчера которых задано это различающееся имя.



| Ввод | Значение |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Manager                                                                     |
| LDAP-отображаемое имя | manager                                                                     |
| Размер              | \-                                                                          |
| Привилегия обновления  | Администратор домена или владелец учетной записи.                                      |
| Частота обновления  | При создании записи пользователя и при необходимости изменения руководителя. |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| System-ID — GUID    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
| Синтаксис            | [**Object(DS-DN)**](s-object-ds-dn.md)                                     |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|--------------------------------------------------------------------|
| Идентификатор ссылки                | 42                                                                 |
| MAPI-Id                | 0x8005                                                             |
| System-Only            | Неверно                                                              |
| Является однозначным       | Верно                                                               |
| Индексируется             | Неверно                                                              |
| В глобальном каталоге      | Верно                                                               |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | Верно                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Верно                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | Верно                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Верно                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | Верно                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Верно                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | Верно                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Верно                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | Верно                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Верно                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





