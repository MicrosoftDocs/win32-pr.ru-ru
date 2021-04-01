---
title: Атрибут Trust-Attributes
description: Этот атрибут хранит атрибуты доверия для доверенного домена.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Trust-Attributes
- Схема AD атрибута Трустаттрибутес
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804811"
---
# <a name="trust-attributes-attribute"></a>Атрибут Trust-Attributes

Этот атрибут хранит атрибуты доверия для доверенного домена. Возможны следующие значения атрибутов.

-   \_Атрибут доверия \_ , не являющийся \_ транзитивным, отключает транзитивность.
-   \_ \_ \_ Родительское доверие дерева атрибута доверия установлено в родительский элемент дерева Организации.
-   ДОВЕРИЕ \_ \_ \_ корневым доверием дерева атрибута доверия с другим корнем дерева в лесу.
-   \_Атрибут доверия \_ \_ только надежная ссылка допустима только для клиентов верхнего уровня.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Trust-Attributes                     |
| LDAP-отображаемое имя | трустаттрибутес                      |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.470               |
| System-ID — GUID    | 80a67e5a-9f22-11d0-afdd-00c04fd930c9 |
| Синтаксис            | [**Перечисление**](s-enumeration.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | Неверно                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | True                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | True                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



 

 





