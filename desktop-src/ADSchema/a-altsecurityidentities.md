---
title: Атрибут "Alt-Security-identitys"
description: Содержит сопоставления для сертификатов X. 509 или внешних учетных записей пользователей Kerberos этому пользователю в целях проверки подлинности.
ms.assetid: 40b2af9c-fd4f-4883-8494-2b64682ee50c
ms.tgt_platform: multiple
keywords:
- Alt — безопасность — схема AD атрибутов удостоверений
- Схема AD атрибута Алтсекуритидентитиес
topic_type:
- apiref
api_name:
- Alt-Security-Identities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2548e337f29778400bb173a8c15d928d7b06d988
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989579"
---
# <a name="alt-security-identities-attribute"></a>Атрибут "Alt-Security-identitys"

Содержит сопоставления для сертификатов X. 509 или внешних учетных записей пользователей Kerberos этому пользователю в целях проверки подлинности.



| Ввод | Значение |
|-------------------|-----------------------------------------------------|
| CN                | Alt-Security — удостоверения                             |
| LDAP-отображаемое имя | altSecurityIdentities                               |
| Размер              | \-                                                  |
| Привилегия обновления  | Администратор домена                                |
| Частота обновления  | Каждый раз, когда требуется новый механизм проверки подлинности. |
| Attribute-Id      | 1.2.840.113556.1.4.867                              |
| System-ID — GUID    | 00fbf30c-91fe-11d1-aebc-0000f80367c1                |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)         |



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
| Является однозначным       | Неверно                                                        |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | Неверно                                                        |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | Неверно                                                        |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | Неверно                                                        |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | Неверно                                                        |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|--------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Неверно                                                        |
| Является однозначным       | Неверно                                                        |
| Индексируется             | True                                                         |
| В глобальном каталоге      | True                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



 

 





