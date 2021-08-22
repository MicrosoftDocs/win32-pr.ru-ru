---
title: атрибут MS-TAPI-unique-identifier
description: Предоставляет имя многоадресной конференции TAPI. Это атрибут именования класса Rt-Conference.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-TAPI-unique-identifier
- Мстапи — схема AD атрибута UID
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e929ecb48cdc7d12b0b75eb275a338e0a6371f365d4591ed532b399aaff03a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508544"
---
# <a name="ms-tapi-unique-identifier-attribute"></a>атрибут MS-TAPI-unique-identifier

Предоставляет имя многоадресной конференции TAPI. Это атрибут именования класса Rt-Conference.



| Ввод | Значение |
|-------------------|-----------------------------------------------------------------------|
| CN                | MS-TAPI-unique-identifier                                             |
| LDAP-отображаемое имя | Мстапи — UID                                                            |
| Размер              | Может быть произвольной строкой, обычно длина которой не превышает 100 символов. |
| Привилегия обновления  | Специальные привилегии не требуются.                                       |
| Частота обновления  | Задается один раз во время создания объекта Rt-Conference.            |
| Attribute-Id      | 1.2.840.113556.1.4.1698                                               |
| System-ID — GUID    | 70a4e7ea-b3b9-4643-8918-e6dd2471bfd4                                  |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)                           |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Нет                                                                                                                       |
| Является однозначным       | Верно                                                                                                                        |
| Индексируется             | Нет                                                                                                                       |
| В глобальном каталоге      | Нет                                                                                                                       |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Нет                                                                                                                       |
| Является однозначным       | Верно                                                                                                                        |
| Индексируется             | Нет                                                                                                                       |
| В глобальном каталоге      | Нет                                                                                                                       |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Нет                                                                                                                       |
| Является однозначным       | Верно                                                                                                                        |
| Индексируется             | Нет                                                                                                                       |
| В глобальном каталоге      | Нет                                                                                                                       |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Нет                                                                                                                       |
| Является однозначным       | Верно                                                                                                                        |
| Индексируется             | Нет                                                                                                                       |
| В глобальном каталоге      | Нет                                                                                                                       |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Нет                                                                                                                       |
| Является однозначным       | Верно                                                                                                                        |
| Индексируется             | Нет                                                                                                                       |
| В глобальном каталоге      | Нет                                                                                                                       |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



 

 





