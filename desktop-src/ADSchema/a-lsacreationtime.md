---
title: LSA-атрибут времени создания
description: атрибут времени создания LSA-Time используется для поддержки репликации в домены Windows NT 4,0.
ms.assetid: a5446cbf-aa35-4ea6-a2e0-9d0ea58edaf1
ms.tgt_platform: multiple
keywords:
- LSA-схема AD атрибута времени создания
- Схема AD атрибута Лсакреатионтиме
topic_type:
- apiref
api_name:
- LSA-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa3e93b7df9c44e9277b9e49a87b056a74e31814f1c69787b2ccb7d3aed5fa3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301544"
---
# <a name="lsa-creation-time-attribute"></a>LSA-атрибут времени создания

атрибут **времени создания LSA-Time** используется для поддержки репликации в домены Windows NT 4,0.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | LSA-время создания                    |
| LDAP-отображаемое имя | лсакреатионтиме                      |
| Размер              | 8 байт                              |
| Привилегия обновления  | Это значение задается системой.     |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.66                |
| System-ID — GUID    | bf9679ad-0de6-11d0-a285-00aa003049e2 |
| Синтаксис            | [**Интервал**](s-interval.md)       |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



 

 





