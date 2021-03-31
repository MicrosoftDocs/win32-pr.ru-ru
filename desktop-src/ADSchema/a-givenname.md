---
title: Атрибут Given-Name
description: Содержит заданное имя (имя) пользователя.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Given-Name
- Схема AD атрибута givenName
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76ab181c6aaf03c2a497be1718df789bfddc6b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893601"
---
# <a name="given-name-attribute"></a>Атрибут Given-Name

Содержит заданное имя (имя) пользователя.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | Given-Name                                  |
| LDAP-отображаемое имя | givenName                                   |
| Размер              | \-                                          |
| Привилегия обновления  | Администратор домена или владелец учетной записи.      |
| Частота обновления  | При создании записи пользователя.          |
| Attribute-Id      | 2.5.4.42                                    |
| System-ID — GUID    | f0f8ff8e-1191-11d0-a060-00aa006c33ed        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



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
| Идентификатор ссылки                | \-                                                                 |
| MAPI-Id                | 0x3A06                                                             |
| System-Only            | Неверно                                                              |
| Является однозначным       | True                                                               |
| Индексируется             | True                                                               |
| В глобальном каталоге      | True                                                               |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000005                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | True                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | True                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | True                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | True                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A06                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | True                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 64                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





