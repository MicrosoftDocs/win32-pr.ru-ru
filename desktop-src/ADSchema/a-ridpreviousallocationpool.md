---
title: Атрибут RID — предыдущий выделенный пул
description: Содержит пул относительных идентификаторов (RID), из которого выделяется контроллер домена.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута RID предыдущего уровня выделения ресурсов пула
- Схема AD атрибута Ридпревиаусаллокатионпул
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5199d9fd0f91b94ed6625a8759f3a5acd76a892460c44e3315911350f0ff59f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837364"
---
# <a name="rid-previous-allocation-pool-attribute"></a>Атрибут RID — предыдущий выделенный пул

Атрибут **RID-Previous-распределения-Pool** содержит пул относительных идентификаторов (RID), из которого выделяется контроллер домена. Этот атрибут представляет собой 8-байтовое значение, содержащее пару из четырех байтов, представляющих начальное и конечное значения пула RID. Начальное значение находится в младших четырех байтах, а конечное значение — в верхних четырех байтах.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | RID — предыдущий пул выделения ресурсов         |
| LDAP-отображаемое имя | ридпревиаусаллокатионпул            |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| System-ID — GUID    | 6617188a-8f3c-11d0-afda-00c04fd930c9 |
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
|------------------------|----------------------------------------|
| Идентификатор ссылки                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Верно                                   |
| Является однозначным       | Верно                                   |
| Индексируется             | Неверно                                  |
| В глобальном каталоге      | Неверно                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Классы, используемые в        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|----------------------------------------|
| Идентификатор ссылки                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Верно                                   |
| Является однозначным       | Верно                                   |
| Индексируется             | Неверно                                  |
| В глобальном каталоге      | Неверно                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Классы, используемые в        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------|
| Идентификатор ссылки                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Верно                                   |
| Является однозначным       | Верно                                   |
| Индексируется             | Неверно                                  |
| В глобальном каталоге      | Неверно                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Классы, используемые в        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------|
| Идентификатор ссылки                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Верно                                   |
| Является однозначным       | Верно                                   |
| Индексируется             | Неверно                                  |
| В глобальном каталоге      | Неверно                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Классы, используемые в        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------|
| Идентификатор ссылки                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Верно                                   |
| Является однозначным       | Верно                                   |
| Индексируется             | Неверно                                  |
| В глобальном каталоге      | Неверно                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Классы, используемые в        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------|
| Идентификатор ссылки                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Верно                                   |
| Является однозначным       | Верно                                   |
| Индексируется             | Неверно                                  |
| В глобальном каталоге      | Неверно                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Классы, используемые в        | [**RID-Set**](c-ridset.md)<br/> |



 

 





