---
title: Атрибут Unicode-Pwd
description: пароль пользователя в Windows NT односторонний формат (OWF). Windows 2000 использует Windows NT OWF. Это свойство используется только операционной системой. Обратите внимание, что невозможно получить открытый пароль обратно из формы OWF пароля.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Unicode-Pwd
- Схема объявления атрибута unicodePwd
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e21929cf41b58688f768ada0b608ca3ef0892a4a54043c30f5cac2d5a72258b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681091"
---
# <a name="unicode-pwd-attribute"></a>Атрибут Unicode-Pwd

пароль пользователя в Windows NT односторонний формат (OWF). Windows 2000 использует Windows NT OWF. Это свойство используется только операционной системой. Обратите внимание, что невозможно получить открытый пароль обратно из формы OWF пароля.



| Ввод | Значение |
|-------------------|------------------------------------------------------------------------------|
| CN                | Unicode-Pwd                                                                  |
| LDAP-отображаемое имя | unicodePwd                                                                   |
| Размер              | \-                                                                           |
| Привилегия обновления  | Администратор домена или владелец учетной записи.                                       |
| Частота обновления  | При создании записи пользователя и при необходимости изменения пароля. |
| Attribute-Id      | 1.2.840.113556.1.4.90                                                        |
| System-ID — GUID    | bf9679e1-0de6-11d0-a285-00aa003049e2                                         |
| Синтаксис            | [**Object(ссылка_на_реплику)**](s-object-replica-link.md)                        |



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
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
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
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
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
| System-Only            | Неверно                                                             |
| Является однозначным       | True                                                              |
| Индексируется             | Неверно                                                             |
| В глобальном каталоге      | Неверно                                                             |
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
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
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
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
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
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
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
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



 

 





