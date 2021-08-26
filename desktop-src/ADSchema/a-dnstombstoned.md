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
ms.openlocfilehash: 6ef8f1b61d8d12fc1725fd695467058ac93277a7aab0977ccaed128a74da79d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077864"
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
| Синтаксис            | [**Логическое**](s-boolean.md)         |



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
| System-Only            | Нет                                    |
| Является однозначным       | Верно                                     |
| Индексируется             | Верно                                     |
| В глобальном каталоге      | Нет                                    |
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
| System-Only            | Нет                                    |
| Является однозначным       | Верно                                     |
| Индексируется             | Верно                                     |
| В глобальном каталоге      | Нет                                    |
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
| System-Only            | Нет                                    |
| Является однозначным       | Верно                                     |
| Индексируется             | Верно                                     |
| В глобальном каталоге      | Нет                                    |
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
| System-Only            | Нет                                    |
| Является однозначным       | Верно                                     |
| Индексируется             | Верно                                     |
| В глобальном каталоге      | Нет                                    |
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
| System-Only            | Нет                                    |
| Является однозначным       | Верно                                     |
| Индексируется             | Верно                                     |
| В глобальном каталоге      | Нет                                    |
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
| System-Only            | Нет                                    |
| Является однозначным       | Верно                                     |
| Индексируется             | Верно                                     |
| В глобальном каталоге      | Нет                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> |



 

 





