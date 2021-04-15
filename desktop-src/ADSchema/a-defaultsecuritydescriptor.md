---
title: Атрибут-дескриптор безопасности по умолчанию
description: Дескриптор безопасности, назначаемый объекту при его первом создании.
ms.assetid: 22575883-2ef3-492b-9868-1eb350c4f547
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута по умолчанию для дескрипторов безопасности
- Схема AD атрибута Дефаултсекуритидескриптор
topic_type:
- apiref
api_name:
- Default-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0b4a8dbe0c633a15b6a5167cb1171a14d1769
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493551"
---
# <a name="default-security-descriptor-attribute"></a>Атрибут-дескриптор безопасности по умолчанию

Дескриптор безопасности, назначаемый объекту при его первом создании.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | Дескриптор безопасности по умолчанию                 |
| LDAP-отображаемое имя | дефаултсекуритидескриптор                   |
| Размер              | \-                                          |
| Привилегия обновления  | Администратор схемы                        |
| Частота обновления  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.224                      |
| System-ID — GUID    | 807a6d30-1669-11d0-a064-00aa006c33ed        |
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
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Неверно                                            |
| Является однозначным       | True                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Неверно                                            |
| Является однозначным       | True                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Class-schema**](c-classschema.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Неверно                                            |
| Является однозначным       | True                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Неверно                                            |
| Является однозначным       | True                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Неверно                                            |
| Является однозначным       | True                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Неверно                                            |
| Является однозначным       | True                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Class-schema**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Неверно                                            |
| Является однозначным       | True                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Class-schema**](c-classschema.md)<br/> |



 

 





