---
title: Атрибут периода сборки мусора-Coll
description: Этот атрибут расположен в службе каталогов CN, CN Windows NT, CN Services, CN Configuration,... объектами. Он представляет время (в часах) между запуском сборки мусора DS.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута периода с мусором-Coll
- Схема AD атрибута Гарбажеколлпериод
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654835"
---
# <a name="garbage-coll-period-attribute"></a>Атрибут периода сборки мусора-Coll

Этот атрибут находится в общем = службе каталогов, CN = Windows NT, CN = Services, CN = Configuration,... объектами. Он представляет время (в часах) между запуском сборки мусора DS.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Мусор-Coll-период                  |
| LDAP-отображаемое имя | гарбажеколлпериод                    |
| Размер              | 4 байта                              |
| Привилегия обновления  | Администратор домена                 |
| Частота обновления  | Очень редки.                           |
| Attribute-Id      | 1.2.840.113556.1.2.301               |
| System-ID — GUID    | 5fd424a1-1262-11d0-a060-00aa006c33ed |
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
|------------------------|-------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Неверно                                                                                                 |
| Является однозначным       | True                                                                                                  |
| Индексируется             | Неверно                                                                                                 |
| В глобальном каталоге      | Неверно                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Классы, используемые в        | [**Получатель почты**](c-mailrecipient.md)<br/> [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Неверно                                                                                                 |
| Является однозначным       | True                                                                                                  |
| Индексируется             | Неверно                                                                                                 |
| В глобальном каталоге      | Неверно                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Классы, используемые в        | [**Получатель почты**](c-mailrecipient.md)<br/> [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | 0x80AF                                           |
| System-Only            | Неверно                                            |
| Является однозначным       | True                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Неверно                                                                                                 |
| Является однозначным       | True                                                                                                  |
| Индексируется             | Неверно                                                                                                 |
| В глобальном каталоге      | Неверно                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Классы, используемые в        | [**Получатель почты**](c-mailrecipient.md)<br/> [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Неверно                                                                                                 |
| Является однозначным       | True                                                                                                  |
| Индексируется             | Неверно                                                                                                 |
| В глобальном каталоге      | Неверно                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Классы, используемые в        | [**Получатель почты**](c-mailrecipient.md)<br/> [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Неверно                                                                                                 |
| Является однозначным       | True                                                                                                  |
| Индексируется             | Неверно                                                                                                 |
| В глобальном каталоге      | Неверно                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Классы, используемые в        | [**Получатель почты**](c-mailrecipient.md)<br/> [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Неверно                                                                                                 |
| Является однозначным       | True                                                                                                  |
| Индексируется             | Неверно                                                                                                 |
| В глобальном каталоге      | Неверно                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Классы, используемые в        | [**Получатель почты**](c-mailrecipient.md)<br/> [**Служба NTDS**](c-ntdsservice.md)<br/> |



 

 





