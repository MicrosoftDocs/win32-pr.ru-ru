---
title: Атрибут времени последнего задания
description: Время последнего изменения секрета.
ms.assetid: 71245cd4-90d8-4aa1-ad96-d46d6b3a7ad0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута времени последнего задания
- Схема AD атрибута Ластсеттиме
topic_type:
- apiref
api_name:
- Last-Set-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7349535f4fbf17624b9cfc353627676988cdf4af63c742ad4c764f2d28e8e29b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804254"
---
# <a name="last-set-time-attribute"></a>Атрибут времени последнего задания

Время последнего изменения секрета. Это значение хранится в виде большого целого числа, представляющего число 100-наносекундных интервалов с 1 января 1601 (UTC).



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Время последнего набора                        |
| LDAP-отображаемое имя | ластсеттиме                          |
| Размер              | 8 байт                              |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.53                |
| System-ID — GUID    | bf967998-0de6-11d0-a285-00aa003049e2 |
| Синтаксис            | [**Интервал**](s-interval.md)       |



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
| MAPI-Id                | \-                                    |
| System-Only            | Нет                                 |
| Является однозначным       | Верно                                  |
| Индексируется             | Нет                                 |
| В глобальном каталоге      | Нет                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Классы, используемые в        | [**Владел**](c-secret.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|---------------------------------------|
| Идентификатор ссылки                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Нет                                 |
| Является однозначным       | Верно                                  |
| Индексируется             | Нет                                 |
| В глобальном каталоге      | Нет                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Классы, используемые в        | [**Владел**](c-secret.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|---------------------------------------|
| Идентификатор ссылки                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Нет                                 |
| Является однозначным       | Верно                                  |
| Индексируется             | Нет                                 |
| В глобальном каталоге      | Нет                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Классы, используемые в        | [**Владел**](c-secret.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|---------------------------------------|
| Идентификатор ссылки                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Нет                                 |
| Является однозначным       | Верно                                  |
| Индексируется             | Нет                                 |
| В глобальном каталоге      | Нет                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Классы, используемые в        | [**Владел**](c-secret.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|---------------------------------------|
| Идентификатор ссылки                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Нет                                 |
| Является однозначным       | Верно                                  |
| Индексируется             | Нет                                 |
| В глобальном каталоге      | Нет                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Классы, используемые в        | [**Владел**](c-secret.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|---------------------------------------|
| Идентификатор ссылки                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Нет                                 |
| Является однозначным       | Верно                                  |
| Индексируется             | Нет                                 |
| В глобальном каталоге      | Нет                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                          |
| Range-Lower            | \-                                    |
| Range-Upper            | \-                                    |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Классы, используемые в        | [**Владел**](c-secret.md)<br/> |



 

 





