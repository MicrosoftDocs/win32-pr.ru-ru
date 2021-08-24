---
title: Атрибут Security-Identifier
description: Уникальное значение переменной длины, используемое для указания учетной записи пользователя, учетной записи группы или сеанса входа в систему, к которому применяется ACE.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Security-Identifier
- Схема AD атрибута securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f15449127dd11e7e0ebfef9f63d8e79470ed662377cbdd1929ed072b2502dae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836874"
---
# <a name="security-identifier-attribute"></a>Атрибут Security-Identifier

Уникальное значение переменной длины, используемое для указания учетной записи пользователя, учетной записи группы или сеанса входа в систему, к которому применяется ACE.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Security-Identifier                  |
| LDAP-отображаемое имя | securityIdentifier                   |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.121               |
| System-ID — GUID    | bf967a2f-0de6-11d0-a285-00aa003049e2 |
| Синтаксис            | [**Строка (SID)**](s-string-sid.md)  |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Неверно                                                                                                             |
| Является однозначным       | Верно                                                                                                              |
| Индексируется             | Неверно                                                                                                             |
| В глобальном каталоге      | Неверно                                                                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Неверно                                                                                                             |
| Является однозначным       | Верно                                                                                                              |
| Индексируется             | Неверно                                                                                                             |
| В глобальном каталоге      | Верно                                                                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Неверно                                                                                                             |
| Является однозначным       | Верно                                                                                                              |
| Индексируется             | Неверно                                                                                                             |
| В глобальном каталоге      | Верно                                                                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Неверно                                                                                                             |
| Является однозначным       | Верно                                                                                                              |
| Индексируется             | Неверно                                                                                                             |
| В глобальном каталоге      | Верно                                                                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Неверно                                                                                                             |
| Является однозначным       | Верно                                                                                                              |
| Индексируется             | Неверно                                                                                                             |
| В глобальном каталоге      | Верно                                                                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Неверно                                                                                                             |
| Является однозначным       | Верно                                                                                                              |
| Индексируется             | Неверно                                                                                                             |
| В глобальном каталоге      | Верно                                                                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Классы, используемые в        | [**Безопасность — участник**](c-securityprincipal.md)<br/> [**Доверенный домен**](c-trusteddomain.md)<br/> |



 

 





