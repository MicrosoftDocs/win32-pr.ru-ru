---
title: атрибут MS-TAPI-Protocol-ID
description: Этот атрибут указывает тип конференции TAPI.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-TAPI-ID
- Схема AD атрибута Мстапи-Протоколид
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10538f66b98988fafa69d4fe2f3e70b47348c999
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138875"
---
# <a name="ms-tapi-protocol-id-attribute"></a>атрибут MS-TAPI-Protocol-ID

Этот атрибут указывает тип конференции TAPI. Этот атрибут используется для определения способа интерпретации двоичного объекта binary в атрибуте [**MS-TAPI-Conference-BLOB**](a-mstapi-conferenceblob.md) . Этот атрибут является произвольной строкой, обычно длина которой меньше 100 символов.



| Ввод | Значение |
|-------------------|------------------------------------------------------------|
| CN                | MS-TAPI-Protocol-ID                                        |
| LDAP-отображаемое имя | Мстапи — Протоколид                                          |
| Размер              | \-                                                         |
| Привилегия обновления  | Специальные привилегии не требуются.                            |
| Частота обновления  | Задается один раз во время создания объекта Rt-Conference. |
| Attribute-Id      | 1.2.840.113556.1.4.1699                                    |
| System-ID — GUID    | 89c1ebcf-7a5f-41fd-99ca-c900b32299ab                       |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)                |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



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
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



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
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



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
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



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
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



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
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



 

 





