---
title: MSMQ — атрибут адреса многоадресной рассылки
description: Это часть объекта MSMQ, которая задается путем вызова API в Мккреатекуеуе или Мксетпропертиес. Он определяет, будут ли MSMQ принимать сообщения с адреса многоадресной рассылки.
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- MSMQ — схема AD атрибута «адрес многоадресной рассылки»
- Схема AD атрибута MSMQ-MulticastAddress
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b90543c40e22d8dd5fdc2b3e5195bd9382357
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535978"
---
# <a name="msmq-multicast-address-attribute"></a>MSMQ — атрибут адреса многоадресной рассылки

Это часть объекта MSMQ, которая задается путем вызова API в Мккреатекуеуе или Мксетпропертиес. Он определяет, будут ли MSMQ принимать сообщения с адреса многоадресной рассылки.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | MSMQ — адрес многоадресной рассылки                      |
| LDAP-отображаемое имя | MSMQ-MulticastAddress                       |
| Размер              | 4 байта                                     |
| Привилегия обновления  | Владелец очереди.                            |
| Частота обновления  | При создании очереди.                    |
| Attribute-Id      | 1.2.840.113556.1.4.1714                     |
| System-ID — GUID    | 1d2f4412-f10d-4337-9b48-6e5b125cd265        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



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



 

 





