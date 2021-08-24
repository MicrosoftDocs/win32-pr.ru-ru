---
title: RID-распределение — атрибут пула
description: Пул, который был предварительно выбран для использования диспетчером RID при использовании RID-Previous-распределения-пула.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "выделение RID — пул"
- Схема AD атрибута Ридаллокатионпул
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce6ff101ca49e8d2ffafdb31f2d05cf1cb2371ee3336525ab31318925d349805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837384"
---
# <a name="rid-allocation-pool-attribute"></a>RID-распределение — атрибут пула

Пул, который был предварительно выбран для использования диспетчером RID при использовании RID-Previous-распределения-пула.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | RID-распределение — пул                  |
| LDAP-отображаемое имя | ридаллокатионпул                    |
| Размер              | 8 байт                              |
| Привилегия обновления  | Это значение задается системой.     |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.371               |
| System-ID — GUID    | 66171889-8f3c-11d0-afda-00c04fd930c9 |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
| Классы, используемые в        | [**RID-Set**](c-ridset.md)<br/> |



 

 





