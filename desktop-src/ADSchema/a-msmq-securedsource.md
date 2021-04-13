---
title: Атрибут защиты от MSMQ, защищенный источником
description: Это часть объекта MSMQ, которая задается путем вызова API в Мккреатекуеуе или Мксетпропертиес. Он определяет, принимает ли MSMQ сообщения только из защищенного источника (например, HTTPS) для этой очереди.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов, защищенных с самого источника MSMQ
- Схема AD атрибута MSMQ-SecuredSource
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535975"
---
# <a name="msmq-secured-source-attribute"></a>Атрибут защиты от MSMQ, защищенный источником

Это часть объекта MSMQ, которая задается путем вызова API в Мккреатекуеуе или Мксетпропертиес. Он определяет, принимает ли MSMQ сообщения только из защищенного источника (например, HTTPS) для этой очереди.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MSMQ — защищенный источник                  |
| LDAP-отображаемое имя | MSMQ-SecuredSource                   |
| Размер              | 4 байта                              |
| Привилегия обновления  | Владелец очереди.                     |
| Частота обновления  | При создании очереди.             |
| Attribute-Id      | 1.2.840.113556.1.4.1713              |
| System-ID — GUID    | 8bf0221b-7a06-4d63-91f0-1499941813d3 |
| Синтаксис            | [**Логическая**](s-boolean.md)         |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | True                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | True                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**Очередь MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | True                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | True                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**Очередь MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | True                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | True                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**Очередь MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | True                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | True                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**Очередь MSMQ**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | True                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | True                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**Очередь MSMQ**](c-msmqqueue.md)<br/> |



 

 





