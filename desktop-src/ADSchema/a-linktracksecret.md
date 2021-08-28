---
title: Link-Track-секретный атрибут
description: Этот атрибут хранит ссылку на секретный ключ, который позволяет преобразовать зашифрованный файл в обычный текст.
ms.assetid: e476f4af-71a8-4bd9-a81d-f825bfbf267b
ms.tgt_platform: multiple
keywords:
- Схема ссылки — секретный атрибут Active Directory
- Схема AD атрибута Линктракксекрет
topic_type:
- apiref
api_name:
- Link-Track-Secret
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90fd71ed399c8a2881f16c13942f7210b152d20ebf5a284f071e8af85b40bf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119302004"
---
# <a name="link-track-secret-attribute"></a>Link-Track-секретный атрибут

Этот атрибут хранит ссылку на секретный ключ, который позволяет преобразовать зашифрованный файл в обычный текст.



| Ввод | Значение |
|-------------------|-------------------------------------------------------|
| CN                | Направление связи — секрет                                     |
| LDAP-отображаемое имя | линктракксекрет                                       |
| Размер              | \-                                                    |
| Привилегия обновления  | \-                                                    |
| Частота обновления  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.269                                |
| System-ID — GUID    | 2ae80fe2-47b4-11d0-a1a4-00c04fd930c9                  |
| Синтаксис            | [**Object(ссылка_на_реплику)**](s-object-replica-link.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|----------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Неверно                                                          |
| Является однозначным       | Верно                                                           |
| Индексируется             | Неверно                                                          |
| В глобальном каталоге      | Неверно                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Классы, используемые в        | [**Link-Track-Vol-запись**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|----------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Неверно                                                          |
| Является однозначным       | Верно                                                           |
| Индексируется             | Неверно                                                          |
| В глобальном каталоге      | Неверно                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Классы, используемые в        | [**Link-Track-Vol-запись**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Неверно                                                          |
| Является однозначным       | Верно                                                           |
| Индексируется             | Неверно                                                          |
| В глобальном каталоге      | Неверно                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Классы, используемые в        | [**Link-Track-Vol-запись**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Неверно                                                          |
| Является однозначным       | Верно                                                           |
| Индексируется             | Неверно                                                          |
| В глобальном каталоге      | Неверно                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Классы, используемые в        | [**Link-Track-Vol-запись**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Неверно                                                          |
| Является однозначным       | Верно                                                           |
| Индексируется             | Неверно                                                          |
| В глобальном каталоге      | Неверно                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Классы, используемые в        | [**Link-Track-Vol-запись**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Неверно                                                          |
| Является однозначным       | Верно                                                           |
| Индексируется             | Неверно                                                          |
| В глобальном каталоге      | Неверно                                                          |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 16                                                             |
| Search-Flags           | 0x00000000                                                     |
| System-Flags           | 0x00000010                                                     |
| Классы, используемые в        | [**Link-Track-Vol-запись**](c-linktrackvolentry.md)<br/> |



 

 





