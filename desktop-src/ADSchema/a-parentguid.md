---
title: Атрибут parent-GUID
description: Это сконструированный атрибут, созданный для поддержки элемента управления DirSync. Этот атрибут содержит objectGuid родителя объекта при репликации создания, переименования или перемещения объекта.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута parent-GUID
- Схема AD атрибута Парентгуид
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f42ba5aedc73f04d8967b84bcfbff39c54ce0dbcdf769e48a747ffa0d3e8c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119325434"
---
# <a name="parent-guid-attribute"></a>Атрибут parent-GUID

Это сконструированный атрибут, созданный для поддержки элемента управления DirSync. Этот атрибут содержит objectGuid родителя объекта при репликации создания, переименования или перемещения объекта.



| Ввод | Значение |
|-------------------|-------------------------------------------------------|
| CN                | Родительский элемент — GUID                                           |
| LDAP-отображаемое имя | парентгуид                                            |
| Размер              | 16 байт                                              |
| Привилегия обновления  | Это значение задается системой.                      |
| Частота обновления  | Во время репликации                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1224                               |
| System-ID — GUID    | 2df90d74-009f-11d2-aa4c-00c04fd7d83a                  |
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
|------------------------|--------------|
| Идентификатор ссылки                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Верно         |
| Является однозначным       | Верно         |
| Индексируется             | Неверно        |
| В глобальном каталоге      | Неверно        |
| NT-Security-дескриптор | О:БАГ: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Классы, используемые в        | \-           |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|--------------|
| Идентификатор ссылки                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Верно         |
| Является однозначным       | Верно         |
| Индексируется             | Неверно        |
| В глобальном каталоге      | Неверно        |
| NT-Security-дескриптор | О:БАГ: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Классы, используемые в        | \-           |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|--------------|
| Идентификатор ссылки                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Верно         |
| Является однозначным       | Верно         |
| Индексируется             | Неверно        |
| В глобальном каталоге      | Неверно        |
| NT-Security-дескриптор | О:БАГ: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Классы, используемые в        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|--------------|
| Идентификатор ссылки                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Верно         |
| Является однозначным       | Верно         |
| Индексируется             | Неверно        |
| В глобальном каталоге      | Неверно        |
| NT-Security-дескриптор | О:БАГ: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Классы, используемые в        | \-           |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|--------------|
| Идентификатор ссылки                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Верно         |
| Является однозначным       | Верно         |
| Индексируется             | Неверно        |
| В глобальном каталоге      | Неверно        |
| NT-Security-дескриптор | О:БАГ: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Классы, используемые в        | \-           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|--------------|
| Идентификатор ссылки                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Верно         |
| Является однозначным       | Верно         |
| Индексируется             | Неверно        |
| В глобальном каталоге      | Неверно        |
| NT-Security-дескриптор | О:БАГ: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Классы, используемые в        | \-           |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|--------------|
| Идентификатор ссылки                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Верно         |
| Является однозначным       | Верно         |
| Индексируется             | Неверно        |
| В глобальном каталоге      | Неверно        |
| NT-Security-дескриптор | О:БАГ: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Классы, используемые в        | \-           |



 

 




