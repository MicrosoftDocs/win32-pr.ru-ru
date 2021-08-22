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
ms.openlocfilehash: b71610e0f970962e8145808d3e4038306dc955ea631f07112b8eb4b57c13e5f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509074"
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
| System-Only            | Нет                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Нет                                            |
| В глобальном каталоге      | Нет                                            |
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
| System-Only            | Нет                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Нет                                            |
| В глобальном каталоге      | Нет                                            |
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
| System-Only            | Нет                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Нет                                            |
| В глобальном каталоге      | Нет                                            |
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
| System-Only            | Нет                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Нет                                            |
| В глобальном каталоге      | Нет                                            |
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
| System-Only            | Нет                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Нет                                            |
| В глобальном каталоге      | Нет                                            |
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
| System-Only            | Нет                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Нет                                            |
| В глобальном каталоге      | Нет                                            |
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
| System-Only            | Нет                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Нет                                            |
| В глобальном каталоге      | Нет                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 32767                                            |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Class-schema**](c-classschema.md)<br/> |



 

 





