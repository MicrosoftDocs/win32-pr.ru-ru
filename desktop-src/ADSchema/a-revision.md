---
title: Атрибут Revision
description: Уровень редакции для дескриптора безопасности или другое изменение. Используется только в объектах SAM-Server и DS-UI-Settings.
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Revision
- Схема AD атрибута Revision
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8948bd865db776c52ac021d296792a6f7d0720dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535903"
---
# <a name="revision-attribute"></a>Атрибут Revision

Уровень редакции для дескриптора безопасности или другое изменение. Используется только в объектах SAM-Server и DS-UI-Settings.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Редакция                             |
| LDAP-отображаемое имя | revision                             |
| Размер              | 4 байта                              |
| Привилегия обновления  | Это значение задается системой.     |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.145               |
| System-ID — GUID    | bf967a21-0de6-11d0-a285-00aa003049e2 |
| Синтаксис            | [**Перечисление**](s-enumeration.md) |



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
|------------------------|---------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Неверно                                                                                 |
| Является однозначным       | True                                                                                  |
| Индексируется             | Неверно                                                                                 |
| В глобальном каталоге      | Неверно                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Классы, используемые в        | [**SAM-домен-база**](c-samdomainbase.md)<br/> [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|---------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Неверно                                                                                 |
| Является однозначным       | True                                                                                  |
| Индексируется             | Неверно                                                                                 |
| В глобальном каталоге      | Неверно                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Классы, используемые в        | [**SAM-домен-база**](c-samdomainbase.md)<br/> [**Вверх**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Неверно                           |
| Является однозначным       | True                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|---------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Неверно                                                                                 |
| Является однозначным       | True                                                                                  |
| Индексируется             | Неверно                                                                                 |
| В глобальном каталоге      | Неверно                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Классы, используемые в        | [**SAM-домен-база**](c-samdomainbase.md)<br/> [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|---------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Неверно                                                                                 |
| Является однозначным       | True                                                                                  |
| Индексируется             | Неверно                                                                                 |
| В глобальном каталоге      | Неверно                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Классы, используемые в        | [**SAM-домен-база**](c-samdomainbase.md)<br/> [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|---------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Неверно                                                                                 |
| Является однозначным       | True                                                                                  |
| Индексируется             | Неверно                                                                                 |
| В глобальном каталоге      | Неверно                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Классы, используемые в        | [**SAM-домен-база**](c-samdomainbase.md)<br/> [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|---------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Неверно                                                                                 |
| Является однозначным       | True                                                                                  |
| Индексируется             | Неверно                                                                                 |
| В глобальном каталоге      | Неверно                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Классы, используемые в        | [**SAM-домен-база**](c-samdomainbase.md)<br/> [**Вверх**](c-top.md)<br/> |



 

 





