---
title: Атрибут LDAP-отображаемое имя
description: Имя, используемое клиентами LDAP, например поставщик LDAP ADSI, для чтения и записи атрибута с помощью протокола LDAP.
ms.assetid: 9cb0b2f0-16cf-4fc6-85b2-d21ff71bc477
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута LDAP-отображаемого имени
- Схема AD атрибута lDAPDisplayName
topic_type:
- apiref
api_name:
- LDAP-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd089ab917cc8f96e04171bc868acd012726ac4431c756e4dd055354b276953d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804264"
---
# <a name="ldap-display-name-attribute"></a>Атрибут LDAP-отображаемое имя

Имя, используемое клиентами LDAP, например поставщик LDAP ADSI, для чтения и записи атрибута с помощью протокола LDAP.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | LDAP-отображаемое имя                           |
| LDAP-отображаемое имя | lDAPDisplayName                             |
| Размер              | \-                                          |
| Привилегия обновления  | Администратор схемы                        |
| Частота обновления  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.2.460                      |
| System-ID — GUID    | bf96799a-0de6-11d0-a285-00aa003049e2        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



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
| MAPI-Id                | 0x8171                                                                                                    |
| System-Only            | Нет                                                                                                     |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Верно                                                                                                      |
| В глобальном каталоге      | Верно                                                                                                      |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | 1                                                                                                         |
| Range-Upper            | 256                                                                                                       |
| Search-Flags           | 0x00000009                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | 0x8171                                                                                                    |
| System-Only            | Нет                                                                                                     |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Верно                                                                                                      |
| В глобальном каталоге      | Верно                                                                                                      |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | 1                                                                                                         |
| Range-Upper            | 256                                                                                                       |
| Search-Flags           | 0x00000009                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | 0x8171                                                                                                    |
| System-Only            | Нет                                                                                                     |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Верно                                                                                                      |
| В глобальном каталоге      | Верно                                                                                                      |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | 1                                                                                                         |
| Range-Upper            | 256                                                                                                       |
| Search-Flags           | 0x00000009                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | 0x8171                                                                                                    |
| System-Only            | Нет                                                                                                     |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Верно                                                                                                      |
| В глобальном каталоге      | Верно                                                                                                      |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | 1                                                                                                         |
| Range-Upper            | 256                                                                                                       |
| Search-Flags           | 0x00000009                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | 0x8171                                                                                                    |
| System-Only            | Нет                                                                                                     |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Верно                                                                                                      |
| В глобальном каталоге      | Верно                                                                                                      |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | 1                                                                                                         |
| Range-Upper            | 256                                                                                                       |
| Search-Flags           | 0x00000009                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | 0x8171                                                                                                    |
| System-Only            | Нет                                                                                                     |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Верно                                                                                                      |
| В глобальном каталоге      | Верно                                                                                                      |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | 1                                                                                                         |
| Range-Upper            | 256                                                                                                       |
| Search-Flags           | 0x00000009                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                        |
| MAPI-Id                | 0x8171                                                                                                    |
| System-Only            | Нет                                                                                                     |
| Является однозначным       | Верно                                                                                                      |
| Индексируется             | Верно                                                                                                      |
| В глобальном каталоге      | Верно                                                                                                      |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                              |
| Range-Lower            | 1                                                                                                         |
| Range-Upper            | 256                                                                                                       |
| Search-Flags           | 0x00000009                                                                                                |
| System-Flags           | 0x00000010                                                                                                |
| Классы, используемые в        | [**Attribute-Schema**](c-attributeschema.md)<br/> [**Class-schema**](c-classschema.md)<br/> |



 

 





