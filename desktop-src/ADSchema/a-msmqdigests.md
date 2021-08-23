---
title: Атрибут MSMQ-Digests
description: Массив дайджестов соответствующих сертификатов в атрибуте mSMQ-Sign-Certificates. Они используются для сопоставления дайджеста с сертификатом.
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MSMQ-Digests
- Схема AD атрибута Мсмкдижестс
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff810ec6cbb8b9d461cec7d349cfb7abd08f1d6e8e330e9b0e1b23e7caefff5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081888"
---
# <a name="msmq-digests-attribute"></a>Атрибут MSMQ-Digests

Массив дайджестов соответствующих сертификатов в атрибуте mSMQ-Sign-Certificates. Они используются для сопоставления дайджеста с сертификатом.



| Ввод | Значение |
|-------------------|-------------------------------------------------------|
| CN                | MSMQ-Digests                                          |
| LDAP-отображаемое имя | мсмкдижестс                                           |
| Размер              | Каждый дайджест имеет размер 16 байт.                              |
| Привилегия обновления  | \-                                                    |
| Частота обновления  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.948                                |
| System-ID — GUID    | 9a0dc33c-c100-11d1-bbc5-0080c76670c0                  |
| Синтаксис            | [**Object(ссылка_на_реплику)**](s-object-replica-link.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Нет                                                                                         |
| Является однозначным       | Нет                                                                                         |
| Индексируется             | Верно                                                                                          |
| В глобальном каталоге      | Верно                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**MSMQ — перенесено — пользователь**](c-msmqmigrateduser.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Нет                                                                                         |
| Является однозначным       | Нет                                                                                         |
| Индексируется             | Верно                                                                                          |
| В глобальном каталоге      | Верно                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**MSMQ — перенесено — пользователь**](c-msmqmigrateduser.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Нет                                                                                         |
| Является однозначным       | Нет                                                                                         |
| Индексируется             | Верно                                                                                          |
| В глобальном каталоге      | Верно                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**MSMQ — перенесено — пользователь**](c-msmqmigrateduser.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Нет                                                                                         |
| Является однозначным       | Нет                                                                                         |
| Индексируется             | Верно                                                                                          |
| В глобальном каталоге      | Верно                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**MSMQ — перенесено — пользователь**](c-msmqmigrateduser.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Нет                                                                                         |
| Является однозначным       | Нет                                                                                         |
| Индексируется             | Верно                                                                                          |
| В глобальном каталоге      | Верно                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**MSMQ — перенесено — пользователь**](c-msmqmigrateduser.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Нет                                                                                         |
| Является однозначным       | Нет                                                                                         |
| Индексируется             | Верно                                                                                          |
| В глобальном каталоге      | Верно                                                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                  |
| Range-Lower            | 16                                                                                            |
| Range-Upper            | 16                                                                                            |
| Search-Flags           | 0x00000001                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Классы, используемые в        | [**MSMQ — перенесено — пользователь**](c-msmqmigrateduser.md)<br/> [**Пользователь**](c-user.md)<br/> |



 

 





