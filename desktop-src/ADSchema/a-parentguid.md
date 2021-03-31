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
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893705"
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
| System-Only            | True         |
| Является однозначным       | True         |
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
| System-Only            | True         |
| Является однозначным       | True         |
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
| System-Only            | True         |
| Является однозначным       | True         |
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
| System-Only            | True         |
| Является однозначным       | True         |
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
| System-Only            | True         |
| Является однозначным       | True         |
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
| System-Only            | True         |
| Является однозначным       | True         |
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
| System-Only            | True         |
| Является однозначным       | True         |
| Индексируется             | Неверно        |
| В глобальном каталоге      | Неверно        |
| NT-Security-дескриптор | О:БАГ: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Классы, используемые в        | \-           |



 

 




