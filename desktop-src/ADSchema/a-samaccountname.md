---
title: SAM-атрибут имени учетной записи
description: Имя входа, используемое для поддержки клиентов и серверов под управлением более ранних версий операционной системы, таких как Windows NT 4,0, Windows 95, Windows 98 и LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- SAM-имя учетной записи-схема AD
- Схема AD атрибута sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893665"
---
# <a name="sam-account-name-attribute"></a>SAM-атрибут имени учетной записи

Имя входа, используемое для поддержки клиентов и серверов под управлением более ранних версий операционной системы, таких как Windows NT 4,0, Windows 95, Windows 98 и LAN Manager.

Этот атрибут должен иметь длину не более 20 символов для поддержки более ранних версий клиентов и не может содержать следующие символы:

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| Ввод | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | SAM-имя учетной записи                                                                         |
| LDAP-отображаемое имя | sAMAccountName                                                                           |
| Размер              | не более 20 символов.                                                                   |
| Привилегия обновления  | Администратор домена                                                                     |
| Частота обновления  | Это значение должно быть назначено при создании записи учетной записи и не должно изменяться. |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| System-ID — GUID    | 3e0abfd0-126a-11d0-a060-00aa006c33ed                                                     |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)                                              |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | True                                                         |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | True                                                         |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | True                                                         |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | True                                                         |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | True                                                         |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | True                                                         |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



 

 





