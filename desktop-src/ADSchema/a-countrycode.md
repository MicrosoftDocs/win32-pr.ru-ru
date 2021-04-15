---
title: Атрибут Country-Code
description: Указывает код страны или региона для выбранного языка пользователя. Это значение не используется в Windows 2000.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Country-Code
- Схема AD атрибута Каунтрикоде
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655528"
---
# <a name="country-code-attribute"></a>Атрибут Country-Code

Указывает код страны или региона для выбранного языка пользователя. Это значение не используется в Windows 2000.



| Ввод | Значение |
|-------------------|-----------------------------------------|
| CN                | Country-Code                            |
| LDAP-отображаемое имя | countryCode                             |
| Размер              | 2 байта                                 |
| Привилегия обновления  | Владелец учетной записи или администратор домена   |
| Частота обновления  | При изменении страны или региона пользователя. |
| Attribute-Id      | 1.2.840.113556.1.4.25                   |
| System-ID — GUID    | 5fd42471-1262-11d0-a060-00aa006c33ed    |
| Синтаксис            | [**Перечисление**](s-enumeration.md)    |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Неверно                                                                                                                             |
| Является однозначным       | True                                                                                                                              |
| Индексируется             | Неверно                                                                                                                             |
| В глобальном каталоге      | Неверно                                                                                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                      |
| Range-Lower            | \-                                                                                                                                |
| Range-Upper            | \-                                                                                                                                |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Организационная единица**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Неверно                                                                                                                             |
| Является однозначным       | True                                                                                                                              |
| Индексируется             | Неверно                                                                                                                             |
| В глобальном каталоге      | Неверно                                                                                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Организационная единица**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|----------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Неверно                                                          |
| Является однозначным       | True                                                           |
| Индексируется             | Неверно                                                          |
| В глобальном каталоге      | Неверно                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 65535                                                          |
| Search-Flags           | 0x00000010                                                     |
| System-Flags           | 0x00000010                                                     |
| Классы, используемые в        | [**Организационная единица**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Неверно                                                                                                                             |
| Является однозначным       | True                                                                                                                              |
| Индексируется             | Неверно                                                                                                                             |
| В глобальном каталоге      | Неверно                                                                                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Организационная единица**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Неверно                                                                                                                             |
| Является однозначным       | True                                                                                                                              |
| Индексируется             | Неверно                                                                                                                             |
| В глобальном каталоге      | Неверно                                                                                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Организационная единица**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Неверно                                                                                                                             |
| Является однозначным       | True                                                                                                                              |
| Индексируется             | Неверно                                                                                                                             |
| В глобальном каталоге      | Неверно                                                                                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Организационная единица**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Неверно                                                                                                                             |
| Является однозначным       | True                                                                                                                              |
| Индексируется             | Неверно                                                                                                                             |
| В глобальном каталоге      | Неверно                                                                                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Организационная единица**](c-organizationalunit.md)<br/> |



 

 





