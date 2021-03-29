---
title: Атрибут «фамилия»
description: Этот атрибут содержит семейство или фамилию пользователя.
ms.assetid: d9d53c9f-4efa-47c4-aec4-518fb8a868b3
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута фамилии
- Схема AD атрибута sn
topic_type:
- apiref
api_name:
- Surname
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453352574a7aec10c56492060ac2de6ceeca030f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989627"
---
# <a name="surname-attribute"></a>Атрибут «фамилия»

Этот атрибут содержит семейство или фамилию пользователя.



| Ввод | Значение |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Surname                                                                          |
| LDAP-отображаемое имя | sn                                                                               |
| Размер              | \-                                                                               |
| Привилегия обновления  | Любой пользователь может обновить этот объект на основе безопасности создаваемого объекта. |
| Частота обновления  | \-                                                                               |
| Attribute-Id      | 2.5.4.4                                                                          |
| System-ID — GUID    | bf967a41-0de6-11d0-a285-00aa003049e2                                             |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|---------------------------------------|
| Идентификатор ссылки                | \-                                    |
| MAPI-Id                | 0x3A11                                |
| System-Only            | Неверно                                 |
| Является однозначным       | True                                  |
| Индексируется             | True                                  |
| В глобальном каталоге      | True                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 64                                    |
| Search-Flags           | 0x00000005                            |
| System-Flags           | 0x00000010                            |
| Классы, используемые в        | [**Человек**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Неверно                                                                                         |
| Является однозначным       | True                                                                                          |
| Индексируется             | True                                                                                          |
| В глобальном каталоге      | True                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**Человек**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Неверно                                                                                         |
| Является однозначным       | True                                                                                          |
| Индексируется             | True                                                                                          |
| В глобальном каталоге      | True                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**Человек**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Неверно                                                                                         |
| Является однозначным       | True                                                                                          |
| Индексируется             | True                                                                                          |
| В глобальном каталоге      | True                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**Человек**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Неверно                                                                                         |
| Является однозначным       | True                                                                                          |
| Индексируется             | True                                                                                          |
| В глобальном каталоге      | True                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**Человек**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Неверно                                                                                         |
| Является однозначным       | True                                                                                          |
| Индексируется             | True                                                                                          |
| В глобальном каталоге      | True                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**Человек**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





