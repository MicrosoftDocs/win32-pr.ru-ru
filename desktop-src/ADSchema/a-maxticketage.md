---
title: Атрибут max-Ticket-Age
description: Этот атрибут определяет максимальное количество времени (в часах), в течение которого можно использовать билет предоставления билета (TGT) для проверки подлинности Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Max-Ticket-Age
- Схема AD атрибута Макстиккетаже
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804409"
---
# <a name="max-ticket-age-attribute"></a>Атрибут max-Ticket-Age

Этот атрибут определяет максимальное количество времени (в часах), в течение которого можно использовать билет предоставления билета (TGT) для проверки подлинности Kerberos. По истечении срока действия TGT пользователя должен быть запрошен новый запрос, или должен быть обновлен существующий. По умолчанию для этого параметра задано значение 10 часов в объекте групповая политика домена по умолчанию (GPO).



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Max-Ticket-Age                       |
| LDAP-отображаемое имя | макстиккетаже                         |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| System-ID — GUID    | bf9679be-0de6-11d0-a285-00aa003049e2 |
| Синтаксис            | [**Пределах**](s-interval.md)       |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|----------------------------------------------------|
| Идентификатор ссылки                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Неверно                                              |
| Является однозначным       | True                                               |
| Индексируется             | Неверно                                              |
| В глобальном каталоге      | Неверно                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Классы, используемые в        | [**Политика домена**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|----------------------------------------------------|
| Идентификатор ссылки                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Неверно                                              |
| Является однозначным       | True                                               |
| Индексируется             | Неверно                                              |
| В глобальном каталоге      | Неверно                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Классы, используемые в        | [**Политика домена**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------|
| Идентификатор ссылки                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Неверно                                              |
| Является однозначным       | True                                               |
| Индексируется             | Неверно                                              |
| В глобальном каталоге      | Неверно                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Классы, используемые в        | [**Политика домена**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------------|
| Идентификатор ссылки                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Неверно                                              |
| Является однозначным       | True                                               |
| Индексируется             | Неверно                                              |
| В глобальном каталоге      | Неверно                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Классы, используемые в        | [**Политика домена**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------|
| Идентификатор ссылки                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Неверно                                              |
| Является однозначным       | True                                               |
| Индексируется             | Неверно                                              |
| В глобальном каталоге      | Неверно                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Классы, используемые в        | [**Политика домена**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------------|
| Идентификатор ссылки                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Неверно                                              |
| Является однозначным       | True                                               |
| Индексируется             | Неверно                                              |
| В глобальном каталоге      | Неверно                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Классы, используемые в        | [**Политика домена**](c-domainpolicy.md)<br/> |



 

 





