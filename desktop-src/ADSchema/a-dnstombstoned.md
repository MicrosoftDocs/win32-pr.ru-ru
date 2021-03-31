---
title: Атрибут DNS-Tombstoned
description: Значение true, если объект был захоронен. Этот атрибут существует, чтобы упростить и ускорить поиск захороненных записей. Захороненные объекты — это объекты, которые были удалены, но еще не удалены из каталога.
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута DNS-Tombstoned
- Схема AD атрибута Днстомбстонед
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dba61706861b808f28d7f6874a9bfd93d4152c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893117"
---
# <a name="dns-tombstoned-attribute"></a>Атрибут DNS-Tombstoned

Значение true, если объект был захоронен. Этот атрибут существует, чтобы упростить и ускорить поиск захороненных записей. Захороненные объекты — это объекты, которые были удалены, но еще не удалены из каталога.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | DNS-Tombstoned                       |
| LDAP-отображаемое имя | днстомбстонед                        |
| Размер              | 4 байта                              |
| Привилегия обновления  | Это значение задается системой.     |
| Частота обновления  | При каждом удалении объекта.       |
| Attribute-Id      | 1.2.840.113556.1.4.1414              |
| System-ID — GUID    | d5eb2eb7-be4e-463b-a214-634a44d7392e |
| Синтаксис            | [**Логическая**](s-boolean.md)         |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | True                                     |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | True                                     |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | True                                     |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | True                                     |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | True                                     |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | True                                     |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> |



 

 





