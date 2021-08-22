---
title: атрибут MS-FRS-Topology-преф
description: Атрибут MS-FRS-Topology-преф используется для записи предпочтительных параметров топологии NTFRS.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-FRS-Topology-преф
- Мсфрс-Topology-схема AD атрибута преф
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8467a038db4f5c263253d31c33cb7dc01bb548712918d654b27b7778079d5c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960533"
---
# <a name="ms-frs-topology-pref-attribute"></a>атрибут MS-FRS-Topology-преф

Атрибут **MS-FRS-Topology-преф** используется для записи предпочтительных параметров топологии NTFRS. Когда член FRS добавляется в набор реплик или удаляется из него, эти атрибуты называются и вносятся изменения в соединения между остальными членами FRS в наборе реплик.

Допустимые значения для этого атрибута:

| Значение | Описание                              |
|-------|------------------------------------------|
| 1     | \_рстопологипреф \_ кольца FRS<br/>     |
| 2     | FRS \_ рстопологипреф \_ хубспоке<br/> |
| 3     | FRS \_ рстопологипреф \_ фуллмеш<br/> |
| 4     | \_РСТОПОЛОГИПРЕФ FRS \_<br/>   |



 



| Ввод | Значение |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-Topology-преф                                               |
| LDAP-отображаемое имя | Мсфрс-Topology-преф                                                |
| Размер              | \-                                                                 |
| Привилегия обновления  | Администратор домена                                               |
| Частота обновления  | При создании набора реплик или изменении предпочтительной топологии. |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| System-ID — GUID    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)                        |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Неверно                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Неверно                                                     |
| В глобальном каталоге      | Неверно                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Неверно                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Неверно                                                     |
| В глобальном каталоге      | Неверно                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Неверно                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Неверно                                                     |
| В глобальном каталоге      | Неверно                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Неверно                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Неверно                                                     |
| В глобальном каталоге      | Неверно                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Неверно                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Неверно                                                     |
| В глобальном каталоге      | Неверно                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



 

 





