---
title: Атрибут Script-Path
description: Этот атрибут указывает путь к сценарию входа пользователя. Строка может иметь значение null.
ms.assetid: 356f2ba0-ceca-4805-a536-286c6a8b54fc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Script-Path
- Схема AD атрибута scriptPath
topic_type:
- apiref
api_name:
- Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbb015b627da90bab453f45dda0a46449f3362b3313e288e2a0f56bb59d0e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923214"
---
# <a name="script-path-attribute"></a>Атрибут Script-Path

Этот атрибут указывает путь к сценарию входа пользователя. Строка может иметь значение null.



| Ввод | Значение |
|-------------------|------------------------------------------------------------------------|
| CN                | Script-Path                                                            |
| LDAP-отображаемое имя | scriptPath                                                             |
| Размер              | \-                                                                     |
| Привилегия обновления  | Администратор домена или владелец учетной записи.                                 |
| Частота обновления  | При создании записи пользователя, когда необходимо изменить путь. |
| Attribute-Id      | 1.2.840.113556.1.4.62                                                  |
| System-ID — GUID    | bf9679a8-0de6-11d0-a285-00aa003049e2                                   |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)                            |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



 

 





