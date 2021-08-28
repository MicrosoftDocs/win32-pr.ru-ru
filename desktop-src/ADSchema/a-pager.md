---
title: Телефон-пейджер-первичный атрибут
description: Основной номер пейджера.
ms.assetid: e5230e09-f76b-4d2a-b56b-d989d315f9bb
ms.tgt_platform: multiple
keywords:
- схема AD атрибута Телефон-пейджер-Primary
- Схема AD атрибута пейджера
topic_type:
- apiref
api_name:
- Phone-Pager-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ebfa52809d53ebf42679b303ebd03fb1f4056f725f08624269c3bdcca8683a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647874"
---
# <a name="phone-pager-primary-attribute"></a>Телефон-пейджер-первичный атрибут

Основной номер пейджера.



| Ввод | Значение |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Телефон-пейджер-основной                                                              |
| LDAP-отображаемое имя | pager                                                                            |
| Размер              | \-                                                                               |
| Привилегия обновления  | Администратор домена или владелец учетной записи.                                           |
| Частота обновления  | При создании записи пользователя и при необходимости изменения номера телефона. |
| Attribute-Id      | 0.9.2342.19200300.100.1.42                                                       |
| System-ID — GUID    | f0f8ffa6-1191-11d0-a060-00aa006c33ed                                             |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|--------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                 |
| MAPI-Id                | 0x3A21                                                             |
| System-Only            | Нет                                                              |
| Является однозначным       | Верно                                                               |
| Индексируется             | Нет                                                              |
| В глобальном каталоге      | Нет                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | Нет                                                                                                                                                    |
| Является однозначным       | Верно                                                                                                                                                     |
| Индексируется             | Нет                                                                                                                                                    |
| В глобальном каталоге      | Нет                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | Нет                                                                                                                                                    |
| Является однозначным       | Верно                                                                                                                                                     |
| Индексируется             | Нет                                                                                                                                                    |
| В глобальном каталоге      | Нет                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | Нет                                                                                                                                                    |
| Является однозначным       | Верно                                                                                                                                                     |
| Индексируется             | Нет                                                                                                                                                    |
| В глобальном каталоге      | Нет                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | Нет                                                                                                                                                    |
| Является однозначным       | Верно                                                                                                                                                     |
| Индексируется             | Нет                                                                                                                                                    |
| В глобальном каталоге      | Нет                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A21                                                                                                                                                   |
| System-Only            | Нет                                                                                                                                                    |
| Является однозначным       | Верно                                                                                                                                                     |
| Индексируется             | Нет                                                                                                                                                    |
| В глобальном каталоге      | Нет                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Пользователь**](c-user.md)<br/> |



 

 





