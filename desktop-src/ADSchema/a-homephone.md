---
title: Phone — Главная — первичный атрибут
description: Основной номер домашнего телефона пользователя.
ms.assetid: 624d89fd-942c-448d-bd51-7d93954370b1
ms.tgt_platform: multiple
keywords:
- Телефон — Главная первичная схема AD
- Схема AD атрибута homePhone
topic_type:
- apiref
api_name:
- Phone-Home-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d2e68116a15dcbf4431d33bb56b4ffed8ee2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655271"
---
# <a name="phone-home-primary-attribute"></a>Phone — Главная — первичный атрибут

Основной номер домашнего телефона пользователя.



| Ввод | Значение |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Телефон — Главная страница                                                               |
| LDAP-отображаемое имя | homePhone                                                                        |
| Размер              | \-                                                                               |
| Привилегия обновления  | Администратор домена или владелец учетной записи.                                           |
| Частота обновления  | При создании записи пользователя и при необходимости изменения номера телефона. |
| Attribute-Id      | 0.9.2342.19200300.100.1.20                                                       |
| System-ID — GUID    | f0f8ffa1-1191-11d0-a060-00aa006c33ed                                             |
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
| MAPI-Id                | 0x3A09                                                             |
| System-Only            | Неверно                                                              |
| Является однозначным       | True                                                               |
| Индексируется             | Неверно                                                              |
| В глобальном каталоге      | True                                                               |
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
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                    |
| Является однозначным       | True                                                                                                                                                     |
| Индексируется             | Неверно                                                                                                                                                    |
| В глобальном каталоге      | True                                                                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Нажат**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                    |
| Является однозначным       | True                                                                                                                                                     |
| Индексируется             | Неверно                                                                                                                                                    |
| В глобальном каталоге      | True                                                                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Нажат**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                    |
| Является однозначным       | True                                                                                                                                                     |
| Индексируется             | Неверно                                                                                                                                                    |
| В глобальном каталоге      | True                                                                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Нажат**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                    |
| Является однозначным       | True                                                                                                                                                     |
| Индексируется             | Неверно                                                                                                                                                    |
| В глобальном каталоге      | True                                                                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Нажат**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                    |
| Является однозначным       | True                                                                                                                                                     |
| Индексируется             | Неверно                                                                                                                                                    |
| В глобальном каталоге      | True                                                                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Классы, используемые в        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Пользователь**](c-user.md)<br/> |



 

 





