---
title: REPL-Уптодате-атрибут Vector
description: Отслеживает сведения о состоянии внутренней репликации для всего NC. Сведения можно извлечь в общедоступной форме через API Дсрепликажетинфо (). Имеется во всех корневых объектах NC.
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- REPL-схема AD атрибута Уптодате-Vector
- Схема AD атрибута Реплуптодатевектор
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9263111459d01d99cf5990d1c818b5ff2a7a19be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655301"
---
# <a name="repl-uptodate-vector-attribute"></a>REPL-Уптодате-атрибут Vector

Отслеживает сведения о состоянии внутренней репликации для всего NC. Сведения можно извлечь в общедоступной форме через API Дсрепликажетинфо (). Имеется во всех корневых объектах NC.



| Ввод | Значение |
|-------------------|--------------------------------------------------------------------------------|
| CN                | REPL-Уптодате-Vector                                                           |
| LDAP-отображаемое имя | реплуптодатевектор                                                             |
| Размер              | Длина пропорциональна количеству реплик (прошлых и существующих) NC. |
| Привилегия обновления  | Это значение задается системой.                                               |
| Частота обновления  | Изменения в ответ на завершенные циклы входящей репликации.                   |
| Attribute-Id      | 1.2.840.113556.1.4.4                                                           |
| System-ID — GUID    | bf967a16-0de6-11d0-a285-00aa003049e2                                           |
| Синтаксис            | [**Object(ссылка_на_реплику)**](s-object-replica-link.md)                          |



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
| System-Only            | True                            |
| Является однозначным       | True                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | True                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Является однозначным       | True                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | True                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Является однозначным       | True                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | True                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Является однозначным       | True                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | True                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Является однозначным       | True                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | True                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Является однозначным       | True                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | True                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Является однозначным       | True                            |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | True                            |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



 

 





