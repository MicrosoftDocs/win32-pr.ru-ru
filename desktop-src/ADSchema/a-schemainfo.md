---
title: Атрибут Schema-Info
description: Внутреннее двоичное значение, используемое для обнаружения изменений схемы между контроллерами домена и принудительного цикла репликации NC схемы перед репликацией любого другого NC. Используется для разрешения связей при присвоении роли FSMO схемы и изменения нескольких контроллеров домена.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Schema-Info
- Схема AD атрибута schemaInfo
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa0d55dd29f207b84b0951ee448ba988d128fabfd126f38b2a4692d7cd3e0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646533"
---
# <a name="schema-info-attribute"></a>Атрибут Schema-Info

Внутреннее двоичное значение, используемое для обнаружения изменений схемы между контроллерами домена и принудительного цикла репликации NC схемы перед репликацией любого другого NC. Используется для разрешения связей при присвоении роли FSMO схемы и изменения нескольких контроллеров домена.



| Ввод | Значение |
|-------------------|-------------------------------------------------------|
| CN                | Schema-Info                                           |
| LDAP-отображаемое имя | schemaInfo                                            |
| Размер              | \-                                                    |
| Привилегия обновления  | Это значение задается системой.                      |
| Частота обновления  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1358                               |
| System-ID — GUID    | f9fb64ae-93b4-11d2-9945-0000f87a57d4                  |
| Синтаксис            | [**Object(ссылка_на_реплику)**](s-object-replica-link.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Нет                           |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**дмд**](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Нет                           |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**дмд**](c-dmd.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Нет                           |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**дмд**](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Нет                           |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**дмд**](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Нет                           |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**дмд**](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Нет                           |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**дмд**](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Нет                           |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**дмд**](c-dmd.md)<br/> |



 

 





