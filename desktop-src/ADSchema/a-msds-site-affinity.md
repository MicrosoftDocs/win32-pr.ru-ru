---
title: MS-DS-site-атрибут сходства
description: Атрибут "MS-DS-site-Affinity" используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута сходства MS-DS-site
- msDS — схема AD атрибута сходства сайтов
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1d3fc359388f5303be808786a929840a409d29505949601b54bd9c7a8b18cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544584"
---
# <a name="ms-ds-site-affinity-attribute"></a>MS-DS-site-атрибут сходства

Атрибут " **MS-DS-site-affinity** " используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.



| Ввод | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| CN                | Соответствие MS-DS-site-affinity                                                                     |
| LDAP-отображаемое имя | msDS — сходство сайтов                                                                      |
| Размер              | Многозначный бинарный большой двоичный объект, где каждое значение имеет тип sizeof (GUID) + sizeof (большое \_ целое число). |
| Привилегия обновления  | \-                                                                                      |
| Частота обновления  | По умолчанию — каждые три месяца.                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.1443                                                                 |
| System-ID — GUID    | c17c5602-bcb7-46f0-9656-6370ca884b72                                                    |
| Синтаксис            | [**Object(ссылка_на_реплику)**](s-object-replica-link.md)                                   |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Верно                              |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Верно                              |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Верно                              |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Верно                              |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет                             |
| Является однозначным       | Нет                             |
| Индексируется             | Верно                              |
| В глобальном каталоге      | Нет                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



 

 





