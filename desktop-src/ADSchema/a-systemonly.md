---
title: Атрибут System-Only
description: Логическое значение, указывающее, может ли только Active Directory изменять класс. Только системные классы могут создаваться или удаляться только агентом системы каталогов.
ms.assetid: 78d2da1f-bdf1-452b-bc64-78088f3630dd
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута System-Only
- Схема AD атрибута Системонли
topic_type:
- apiref
api_name:
- System-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c28707c2cc2d9070ff639dd9c9e9d934a0a5569e32ae40b067e639e6a21e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835865"
---
# <a name="system-only-attribute"></a>Атрибут System-Only

Логическое значение, указывающее, может ли только Active Directory изменять класс. Только системные классы могут создаваться или удаляться только агентом системы каталогов.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | System-Only                          |
| LDAP-отображаемое имя | systemOnly                           |
| Размер              | 4 байта                              |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.170               |
| System-ID — GUID    | bf967a46-0de6-11d0-a285-00aa003049e2 |
| Синтаксис            | [**Логическое**](s-boolean.md)         |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Верно                                                                                                      |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Неверно                                                                                                     |
| В глобальном каталоге      | Неверно                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Верно                                                                                                      |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Неверно                                                                                                     |
| В глобальном каталоге      | Неверно                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Верно                                                                                                      |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Неверно                                                                                                     |
| В глобальном каталоге      | Неверно                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Верно                                                                                                      |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Неверно                                                                                                     |
| В глобальном каталоге      | Неверно                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Верно                                                                                                      |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Неверно                                                                                                     |
| В глобальном каталоге      | Неверно                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Верно                                                                                                      |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Неверно                                                                                                     |
| В глобальном каталоге      | Неверно                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | \-                                                                                                        |
| System-Only            | Верно                                                                                                      |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Неверно                                                                                                     |
| В глобальном каталоге      | Неверно                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | \-                                                                                                        |
| Range-Upper            | \-                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



 

 





