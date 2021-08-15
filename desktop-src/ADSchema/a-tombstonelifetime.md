---
title: Атрибут Tombstone-Lifetime
description: Число дней до удаления удаленного объекта из служб каталогов.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Tombstone-Lifetime
- Схема AD атрибута Томбстонелифетиме
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96d440b82f488e7968f787ae52d9f431350bee6050bd50b385f5751f51e76a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644954"
---
# <a name="tombstone-lifetime-attribute"></a>Атрибут Tombstone-Lifetime

Число дней до удаления удаленного объекта из служб каталогов. Это помогает удалять объекты из реплицируемых серверов и предотвращать восстановление из повторного представления удаленного объекта. Это значение находится в объекте службы каталогов в сетевом адаптере конфигурации.



| Ввод | Значение |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| LDAP-отображаемое имя | томбстонелифетиме                                         |
| Размер              | 4 байта. Значение по умолчанию — 60 дней, если значения не заданы. |
| Привилегия обновления  | \-                                                        |
| Частота обновления  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| System-ID — GUID    | 16c3a860-1273-11d0-a060-00aa006c33ed                      |
| Синтаксис            | [**Перечисление**](s-enumeration.md)                      |



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
| MAPI-Id                | 0x8145                                           |
| System-Only            | Неверно                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Неверно                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Неверно                                            |
| Является однозначным       | Верно                                             |
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
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Неверно                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Неверно                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Неверно                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Служба NTDS**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|--------------------------------------------------|
| Идентификатор ссылки                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Неверно                                            |
| Является однозначным       | Верно                                             |
| Индексируется             | Неверно                                            |
| В глобальном каталоге      | Неверно                                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Классы, используемые в        | [**Служба NTDS**](c-ntdsservice.md)<br/> |



 

 





