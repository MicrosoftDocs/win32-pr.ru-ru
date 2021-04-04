---
title: Атрибут Trust-Type
description: Тип доверия, например Windows NT или MIT.
ms.assetid: ad3640cd-d634-4ec1-8be8-1fb8272e4b23
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Trust-Type
- Схема AD атрибута Трусттипе
topic_type:
- apiref
api_name:
- Trust-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b8a8f59f7df976f968bb4f2915e667a06e95bb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989624"
---
# <a name="trust-type-attribute"></a>Атрибут Trust-Type

Тип доверия, например Windows NT или MIT.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Trust-Type                           |
| LDAP-отображаемое имя | трусттипе                            |
| Размер              | 4 байта                              |
| Привилегия обновления  | Это значение задается системой.     |
| Частота обновления  | При создании нового доверия.         |
| Attribute-Id      | 1.2.840.113556.1.4.136               |
| System-ID — GUID    | bf967a60-0de6-11d0-a285-00aa003049e2 |
| Синтаксис            | [**Перечисление**](s-enumeration.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | Неверно                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



 

 





