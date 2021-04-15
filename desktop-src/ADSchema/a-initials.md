---
title: Атрибут инициалов
description: Содержит инициалы для частей полного имени пользователя. Его можно использовать в качестве отчества в адресной книге Windows.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Начальная схема атрибута AD
- начальная схема атрибута AD
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946f6c9633c1126a30ae4898274096a54db9a402
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655267"
---
# <a name="initials-attribute"></a>Атрибут инициалов

Содержит инициалы для частей полного имени пользователя. Его можно использовать в качестве отчества в адресной книге Windows.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | Инициалы                                    |
| LDAP-отображаемое имя | Initials                                    |
| Размер              | \-                                          |
| Привилегия обновления  | Администратор домена или владелец учетной записи.      |
| Частота обновления  | \-                                          |
| Attribute-Id      | 2.5.4.43                                    |
| System-ID — GUID    | f0f8ff90-1191-11d0-a060-00aa006c33ed        |
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
| MAPI-Id                | 0x3A0A                                                             |
| System-Only            | Неверно                                                              |
| Является однозначным       | True                                                               |
| Индексируется             | Неверно                                                              |
| В глобальном каталоге      | Неверно                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 6                                                                  |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Неверно                                                                                                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Неверно                                                                                                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Неверно                                                                                                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Неверно                                                                                                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Неверно                                                                                                                  |
| Является однозначным       | True                                                                                                                   |
| Индексируется             | Неверно                                                                                                                  |
| В глобальном каталоге      | Неверно                                                                                                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





