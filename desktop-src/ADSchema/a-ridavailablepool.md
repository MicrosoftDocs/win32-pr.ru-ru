---
title: RID — атрибут пула доступности
description: Пространство, из которого выделяются пулы RID.
ms.assetid: abb6218f-def2-4a38-964f-3f0ee6c6f917
ms.tgt_platform: multiple
keywords:
- RID — схема AD атрибутов пула
- Схема AD атрибута Ридаваилаблепул
topic_type:
- apiref
api_name:
- RID-Available-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb3a616d0c687b0dc5514b0dcf54ff5832ffc2a9175f99328bec025c8bde53f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118423590"
---
# <a name="rid-available-pool-attribute"></a>RID — атрибут пула доступности

Пространство, из которого выделяются пулы RID.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | RID — пул доступности                   |
| LDAP-отображаемое имя | ридаваилаблепул                     |
| Размер              | 8 байт                              |
| Привилегия обновления  | Это значение задается системой.     |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.370               |
| System-ID — GUID    | 66171888-8f3c-11d0-afda-00c04fd930c9 |
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
|------------------------|------------------------------------------------|
| Идентификатор ссылки                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Нет.                                          |
| Является однозначным       | Верно                                           |
| Индексируется             | Нет.                                          |
| В глобальном каталоге      | Нет.                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                   |
| Range-Lower            | \-                                             |
| Range-Upper            | \-                                             |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Классы, используемые в        | [**Диспетчер RID**](c-ridmanager.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------------|
| Идентификатор ссылки                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Нет.                                          |
| Является однозначным       | Верно                                           |
| Индексируется             | Нет.                                          |
| В глобальном каталоге      | Нет.                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                   |
| Range-Lower            | \-                                             |
| Range-Upper            | \-                                             |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Классы, используемые в        | [**Диспетчер RID**](c-ridmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------------|
| Идентификатор ссылки                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Нет.                                          |
| Является однозначным       | Верно                                           |
| Индексируется             | Нет.                                          |
| В глобальном каталоге      | Нет.                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                   |
| Range-Lower            | \-                                             |
| Range-Upper            | \-                                             |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Классы, используемые в        | [**Диспетчер RID**](c-ridmanager.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------------|
| Идентификатор ссылки                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Нет.                                          |
| Является однозначным       | Верно                                           |
| Индексируется             | Нет.                                          |
| В глобальном каталоге      | Нет.                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                   |
| Range-Lower            | \-                                             |
| Range-Upper            | \-                                             |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Классы, используемые в        | [**Диспетчер RID**](c-ridmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------------|
| Идентификатор ссылки                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Нет.                                          |
| Является однозначным       | Верно                                           |
| Индексируется             | Нет.                                          |
| В глобальном каталоге      | Нет.                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                   |
| Range-Lower            | \-                                             |
| Range-Upper            | \-                                             |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Классы, используемые в        | [**Диспетчер RID**](c-ridmanager.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------|
| Идентификатор ссылки                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Нет.                                          |
| Является однозначным       | Верно                                           |
| Индексируется             | Нет.                                          |
| В глобальном каталоге      | Нет.                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                   |
| Range-Lower            | \-                                             |
| Range-Upper            | \-                                             |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Классы, используемые в        | [**Диспетчер RID**](c-ridmanager.md)<br/> |



 

 





