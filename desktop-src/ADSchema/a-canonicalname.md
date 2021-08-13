---
title: Атрибут Canonical-Name
description: Имя объекта в каноническом формате.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Canonical-Name
- Схема AD атрибута Каноникалнаме
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d88b31dd351e255c252188388bd1ba06b3a1c073163f5cd2cc9d2deac16a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307194"
---
# <a name="canonical-name-attribute"></a>Атрибут Canonical-Name

Имя объекта в каноническом формате. myserver2.fabrikam.com/users/jeffsmith — это пример различающегося имени в каноническом формате. Это сконструированный атрибут. Возвращаемые результаты идентичны функциям, возвращаемым следующей функцией Active Directory: DsCrackNames (NULL, \_ флаг имени DS \_ , \_ только синтаксис \_ , \_ полное доменное имя DS \_ 1779 \_ , \_ каноническое \_ имя DS,...).

Дополнительные сведения о форматах имен см. в разделе [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | Canonical-Name                              |
| LDAP-отображаемое имя | canonicalName                               |
| Размер              | \-                                          |
| Привилегия обновления  | \-                                          |
| Частота обновления  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.916                      |
| System-ID — GUID    | 9a7ad945-ca53-11d1-bbd0-0080c76670c0        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



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
| Является однозначным       | Неверно                           |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Неверно                           |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Неверно                           |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Неверно                           |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Неверно                           |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Неверно                           |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|---------------------------------|
| Идентификатор ссылки                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Верно                            |
| Является однозначным       | Неверно                           |
| Индексируется             | Неверно                           |
| В глобальном каталоге      | Неверно                           |
| NT-Security-дескриптор | О:БАГ: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Классы, используемые в        | [**Вверх**](c-top.md)<br/> |



 

