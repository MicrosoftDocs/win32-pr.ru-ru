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
ms.openlocfilehash: 62338280079ca5a3732ba3d72941fdb9b978720692b7211ae41612651f86387d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022802"
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
| Индексируется             | Верно                                                         |
| В глобальном каталоге      | Верно                                                         |
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
| Индексируется             | Верно                                                         |
| В глобальном каталоге      | Верно                                                         |
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
| Индексируется             | Верно                                                         |
| В глобальном каталоге      | Верно                                                         |
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
| Индексируется             | Верно                                                         |
| В глобальном каталоге      | Верно                                                         |
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
| Индексируется             | Верно                                                         |
| В глобальном каталоге      | Верно                                                         |
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
| Индексируется             | Верно                                                         |
| В глобальном каталоге      | Верно                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> |



 

 





