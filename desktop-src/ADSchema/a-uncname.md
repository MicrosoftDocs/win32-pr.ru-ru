---
title: Атрибут UNC-Name
description: Универсальное имя соглашения об именовании для общих томов и принтеров.
ms.assetid: 967fd0dc-10af-4482-bc2c-1d1dc13dee39
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута UNC-Name
- Схема AD атрибута uncname
topic_type:
- apiref
api_name:
- UNC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e06bc54ebb035a491e2d93a1c372e2d46fc43f76
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655038"
---
# <a name="unc-name-attribute"></a>Атрибут UNC-Name

Универсальное имя соглашения об именовании для общих томов и принтеров.



| Ввод | Значение |
|-------------------|-----------------------------------------------|
| CN                | UNC-Name                                      |
| LDAP-отображаемое имя | uNCName                                       |
| Размер              | \-                                            |
| Привилегия обновления  | Администратор домена                          |
| Частота обновления  | При создании новых томов или очередей печати. |
| Attribute-Id      | 1.2.840.113556.1.4.137                        |
| System-ID — GUID    | bf967a64-0de6-11d0-a285-00aa003049e2          |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)   |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                |
| Является однозначным       | True                                                                                                                                                 |
| Индексируется             | True                                                                                                                                                 |
| В глобальном каталоге      | True                                                                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                           |
| Классы, используемые в        | [**Каталог индекс-сервер**](c-indexservercatalog.md)<br/> [**Очередь печати**](c-printqueue.md)<br/> [**Том**](c-volume.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                        |
| MAPI-Id                | \-                                                                                                                                                                                        |
| System-Only            | Неверно                                                                                                                                                                                     |
| Является однозначным       | True                                                                                                                                                                                      |
| Индексируется             | True                                                                                                                                                                                      |
| В глобальном каталоге      | True                                                                                                                                                                                      |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                        |
| Search-Flags           | 0x00000001                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                |
| Классы, используемые в        | [**FT-DFS**](c-ftdfs.md)<br/> [**Каталог индекс-сервер**](c-indexservercatalog.md)<br/> [**Очередь печати**](c-printqueue.md)<br/> [**Том**](c-volume.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                                                                                                                                |
| Является однозначным       | True                                                                                                                                                                                                                                                                 |
| Индексируется             | True                                                                                                                                                                                                                                                                 |
| В глобальном каталоге      | True                                                                                                                                                                                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Классы, используемые в        | [**FT-DFS**](c-ftdfs.md)<br/> [**Каталог индекс-сервер**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Очередь печати**](c-printqueue.md)<br/> [**Том**](c-volume.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                                                                                                                                |
| Является однозначным       | True                                                                                                                                                                                                                                                                 |
| Индексируется             | True                                                                                                                                                                                                                                                                 |
| В глобальном каталоге      | True                                                                                                                                                                                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Классы, используемые в        | [**FT-DFS**](c-ftdfs.md)<br/> [**Каталог индекс-сервер**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Очередь печати**](c-printqueue.md)<br/> [**Том**](c-volume.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                                                                                                                                |
| Является однозначным       | True                                                                                                                                                                                                                                                                 |
| Индексируется             | True                                                                                                                                                                                                                                                                 |
| В глобальном каталоге      | True                                                                                                                                                                                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Классы, используемые в        | [**FT-DFS**](c-ftdfs.md)<br/> [**Каталог индекс-сервер**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Очередь печати**](c-printqueue.md)<br/> [**Том**](c-volume.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Неверно                                                                                                                                                                                                                                                                |
| Является однозначным       | True                                                                                                                                                                                                                                                                 |
| Индексируется             | True                                                                                                                                                                                                                                                                 |
| В глобальном каталоге      | True                                                                                                                                                                                                                                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Классы, используемые в        | [**FT-DFS**](c-ftdfs.md)<br/> [**Каталог индекс-сервер**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Очередь печати**](c-printqueue.md)<br/> [**Том**](c-volume.md)<br/> |



 

 





