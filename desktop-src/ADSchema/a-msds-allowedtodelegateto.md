---
title: Атрибут ms-DS-Allowed-to-Delegate
description: Это атрибут для объектов учетной записи службы (компьютера или учетной записи пользователя).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута Active-DS-Allow-to-Delegate
- Схема AD атрибута msDS-Алловедтоделегатето
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655215"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a>Атрибут ms-DS-Allowed-to-Delegate

Это атрибут для объектов учетной записи службы (компьютера или учетной записи пользователя). Он содержит список имен субъектов-служб (SPN). Этот атрибут используется для настройки службы таким образом, чтобы она могла получать билеты службы, которые можно использовать для ограниченного делегирования.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | MS-DS-Allowed-to-Delegate-to                |
| LDAP-отображаемое имя | msDS-Алловедтоделегатето                    |
| Размер              | от 0 до 64 КБ                                    |
| Привилегия обновления  | \-                                          |
| Частота обновления  | Редко                                |
| Attribute-Id      | 1.2.840.113556.1.4.1787                     |
| System-ID — GUID    | 800d94d7-b7a1-42a1-b14d-7cae1423d07f        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|--------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Неверно                                                              |
| Является однозначным       | Неверно                                                              |
| Индексируется             | Неверно                                                              |
| В глобальном каталоге      | Неверно                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|--------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Неверно                                                              |
| Является однозначным       | Неверно                                                              |
| Индексируется             | Неверно                                                              |
| В глобальном каталоге      | Неверно                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|--------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Неверно                                                              |
| Является однозначным       | Неверно                                                              |
| Индексируется             | Неверно                                                              |
| В глобальном каталоге      | Неверно                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|--------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Неверно                                                              |
| Является однозначным       | Неверно                                                              |
| Индексируется             | Неверно                                                              |
| В глобальном каталоге      | Неверно                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|--------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Неверно                                                              |
| Является однозначным       | Неверно                                                              |
| Индексируется             | Неверно                                                              |
| В глобальном каталоге      | Неверно                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





