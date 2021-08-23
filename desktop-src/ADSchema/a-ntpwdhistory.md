---
title: Атрибут журнала NT-PWD-History
description: журнал паролей пользователя в Windows NT односторонний формат (OWF). Windows 2000 использует Windows NT OWF.
ms.assetid: 7c6a0fe2-561e-43a2-af46-7505e7e13288
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута NT-PWD-History
- Схема AD атрибута Нтпвдхистори
topic_type:
- apiref
api_name:
- Nt-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f247358e95b804330f245cf86ba2390c54da17e015060a0ea65a80566383558
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648184"
---
# <a name="nt-pwd-history-attribute"></a>Атрибут журнала NT-PWD-History

журнал паролей пользователя в Windows NT односторонний формат (OWF). Windows 2000 использует Windows NT OWF.



| Ввод | Значение |
|-------------------|-------------------------------------------------------|
| CN                | NT-PWD-History                                        |
| LDAP-отображаемое имя | нтпвдхистори                                          |
| Размер              | \-                                                    |
| Привилегия обновления  | Это значение задается системой.                      |
| Частота обновления  | Каждый раз, когда пользователь изменяет пароли.                 |
| Attribute-Id      | 1.2.840.113556.1.4.94                                 |
| System-ID — GUID    | bf9679e2-0de6-11d0-a285-00aa003049e2                  |
| Синтаксис            | [**Object(ссылка_на_реплику)**](s-object-replica-link.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Нет                             |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Нет                             |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Нет                                                             |
| Является однозначным       | Нет                                                             |
| Индексируется             | Нет                                                             |
| В глобальном каталоге      | Нет                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Классы, используемые в        | [**Объект MS-DS-BIND-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Нет                             |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Нет                             |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Нет                             |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Нет                             |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



 

 





