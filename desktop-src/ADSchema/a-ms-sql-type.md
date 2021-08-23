---
title: атрибут MS-SQL-Type
description: тип репликации, используемый сервером SQL.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- схема AD атрибута MS-SQL-Type
- схема AD атрибута mS-SQL-Type
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15850884b8071fc103abf2c8d3f12ad68d4f5ed946ef2b491b4907b87b1cb524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583294"
---
# <a name="ms-sql-type-attribute"></a>атрибут MS-SQL-Type

тип репликации, используемый сервером SQL. Для этого атрибута возможны следующие значения.



| Значение        | Описание                           |
|--------------|---------------------------------------|
| 0<br/> | Репликация транзакций.<br/> |
| 1<br/> | Репликация моментальных снимков.<br/>      |
| 2<br/> | Репликация слиянием.<br/>         |



 



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | тип MS-SQL                                 |
| LDAP-отображаемое имя | тип mS-SQL                                 |
| Размер              | \-                                          |
| Привилегия обновления  | Администратор домена                        |
| Частота обновления  | При настройке репликации.                 |
| Attribute-Id      | 1.2.840.113556.1.4.1391                     |
| System-ID — GUID    | ca48eba8-ccee-11d2-9993-0000f87a57d4        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Нет                                                                                                                               |
| Является однозначным       | Верно                                                                                                                                |
| Индексируется             | Нет                                                                                                                               |
| В глобальном каталоге      | Нет                                                                                                                               |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Классы, используемые в        | [**MS-SQL-склпубликатион**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-олапдатабасе**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Нет                                                                                                                               |
| Является однозначным       | Верно                                                                                                                                |
| Индексируется             | Нет                                                                                                                               |
| В глобальном каталоге      | Нет                                                                                                                               |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Классы, используемые в        | [**MS-SQL-склпубликатион**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-олапдатабасе**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Нет                                                                                                                               |
| Является однозначным       | Верно                                                                                                                                |
| Индексируется             | Нет                                                                                                                               |
| В глобальном каталоге      | Нет                                                                                                                               |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Классы, используемые в        | [**MS-SQL-склпубликатион**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-олапдатабасе**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Нет                                                                                                                               |
| Является однозначным       | Верно                                                                                                                                |
| Индексируется             | Нет                                                                                                                               |
| В глобальном каталоге      | Нет                                                                                                                               |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Классы, используемые в        | [**MS-SQL-склпубликатион**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-олапдатабасе**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Нет                                                                                                                               |
| Является однозначным       | Верно                                                                                                                                |
| Индексируется             | Нет                                                                                                                               |
| В глобальном каталоге      | Нет                                                                                                                               |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Классы, используемые в        | [**MS-SQL-склпубликатион**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-олапдатабасе**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Нет                                                                                                                               |
| Является однозначным       | Верно                                                                                                                                |
| Индексируется             | Нет                                                                                                                               |
| В глобальном каталоге      | Нет                                                                                                                               |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Классы, используемые в        | [**MS-SQL-склпубликатион**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-олапдатабасе**](c-ms-sql-olapdatabase.md)<br/> |



 

 





