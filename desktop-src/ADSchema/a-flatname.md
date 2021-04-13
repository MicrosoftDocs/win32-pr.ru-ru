---
title: Атрибут Flat-Name
description: Для доменов Windows NT неструктурированное имя является NetBIOS-именем. Для ссылок, не имеющих \ 8211; Домены Windows NT, неструктурированное имя — это идентифицирующее имя этого домена или значение NULL.
ms.assetid: ec368657-a0e7-4416-ab80-1d18d98bbcfa
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Flat-Name
- Схема AD атрибута Флатнаме
topic_type:
- apiref
api_name:
- Flat-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373ee0736c051932fdb6dd20701f0c5ec353ad3b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493593"
---
# <a name="flat-name-attribute"></a>Атрибут Flat-Name

Для доменов Windows NT неструктурированное имя является NetBIOS-именем. Для ссылок, не являющихся доменами Windows NT, неструктурированным именем является идентифицирующее имя этого домена или **значение NULL**.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | Flat-Name                                   |
| LDAP-отображаемое имя | флатнаме                                    |
| Размер              | \-                                          |
| Привилегия обновления  | \-                                          |
| Частота обновления  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.511                      |
| System-ID — GUID    | b7b13117-b82e-11d0-afee-0000f80367c1        |
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
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | True                                                 |
| В глобальном каталоге      | Неверно                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | True                                                 |
| В глобальном каталоге      | Неверно                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | True                                                 |
| В глобальном каталоге      | Неверно                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | True                                                 |
| В глобальном каталоге      | Неверно                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | True                                                 |
| В глобальном каталоге      | Неверно                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | True                                                 |
| В глобальном каталоге      | Неверно                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



 

 





