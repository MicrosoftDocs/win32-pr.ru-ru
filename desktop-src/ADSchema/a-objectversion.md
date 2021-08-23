---
title: Атрибут Object-Version
description: Это можно использовать для хранения номера версии объекта.
ms.assetid: 1aa8520b-c640-4ea2-9230-f28154bf69b0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Object-Version
- Схема AD атрибута Обжектверсион
topic_type:
- apiref
api_name:
- Object-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: facf10e8ea5466b75f9ce87f9a980a0ddc197dde839f40d76157f128c15b5d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704554"
---
# <a name="object-version-attribute"></a>Атрибут Object-Version

Это можно использовать для хранения номера версии объекта.



| Ввод | Значение |
|-------------------|----------------------------------------------------------------|
| CN                | Object-Version                                                 |
| LDAP-отображаемое имя | обжектверсион                                                  |
| Размер              | 4 байта                                                        |
| Привилегия обновления  | Это значение задается конструктором объекта.               |
| Частота обновления  | Это значение должно увеличиваться каждый раз при изменении объекта. |
| Attribute-Id      | 1.2.840.113556.1.2.76                                          |
| System-ID — GUID    | 16775848-47f3-11d1-a9c3-0000f80367c1                           |
| Синтаксис            | [**Перечисление**](s-enumeration.md)                           |



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
| MAPI-Id                | 0x80F7                          |
| System-Only            | Нет                           |
| Является однозначным       | Верно                            |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | 0x80F7                          |
| System-Only            | Нет                           |
| Является однозначным       | Верно                            |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | 0x80F7                          |
| System-Only            | Нет                           |
| Является однозначным       | Верно                            |
| Индексируется             | Нет                           |
| В глобальном каталоге      | Нет                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | 0x80F7                          |
| System-Only            | Неверно                           |
| Является однозначным       | Верно                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | 0x80F7                          |
| System-Only            | Неверно                           |
| Является однозначным       | Верно                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | 0x80F7                          |
| System-Only            | Неверно                           |
| Является однозначным       | Верно                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | 0x80F7                          |
| System-Only            | Неверно                           |
| Является однозначным       | Верно                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



 

 





