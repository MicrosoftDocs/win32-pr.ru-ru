---
title: Атрибут Trust-Partner
description: Имя домена, с которым существует доверие.
ms.assetid: 0b7c8e78-614b-46dd-8616-40d75b461639
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Trust-Partner
- Схема AD атрибута Трустпартнер
topic_type:
- apiref
api_name:
- Trust-Partner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ce551bbf23c7eec378088a0a8d9a9ced25612e40cae1766c55099bb4e45b31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835444"
---
# <a name="trust-partner-attribute"></a>Атрибут Trust-Partner

Имя домена, с которым существует доверие.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | Trust-Partner                               |
| LDAP-отображаемое имя | трустпартнер                                |
| Размер              | \-                                          |
| Привилегия обновления  | Это значение задается системой.            |
| Частота обновления  | При создании нового доверия.                |
| Attribute-Id      | 1.2.840.113556.1.4.133                      |
| System-ID — GUID    | bf967a5d-0de6-11d0-a285-00aa003049e2        |
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
| Является однозначным       | Верно                                                 |
| Индексируется             | Верно                                                 |
| В глобальном каталоге      | Неверно                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | Верно                                                 |
| Индексируется             | Верно                                                 |
| В глобальном каталоге      | Верно                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | Верно                                                 |
| Индексируется             | Верно                                                 |
| В глобальном каталоге      | Верно                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | Верно                                                 |
| Индексируется             | Верно                                                 |
| В глобальном каталоге      | Верно                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | Верно                                                 |
| Индексируется             | Верно                                                 |
| В глобальном каталоге      | Верно                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | Верно                                                 |
| Индексируется             | Верно                                                 |
| В глобальном каталоге      | Верно                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



 

 





