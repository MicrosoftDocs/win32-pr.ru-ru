---
title: атрибут типа DHCP
description: Тип DHCP-сервера.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута типа DHCP
- Схема AD атрибута Дхкптипе
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f4cc64a05db9b88d13a1e7dfb3ce0976391b9d2514388ae9045eb11d97a5b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049654"
---
# <a name="dhcp-type-attribute"></a>атрибут типа DHCP

Тип DHCP-сервера. Этот атрибут задается для всех объектов класса objectClass [**дхкпкласс**](c-dhcpclass.md). Его значение определяет тип объекта:

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| Ввод | Значение |
|-------------------|--------------------------------------------------------|
| CN                | Тип DHCP                                              |
| LDAP-отображаемое имя | дхкптипе                                               |
| Размер              | 4 байта                                                |
| Привилегия обновления  | Администратор домена.                                  |
| Частота обновления  | При добавлении или удалении нового сервера из леса. |
| Attribute-Id      | 1.2.840.113556.1.4.699                                 |
| System-ID — GUID    | 963d273b-48be-11d1-a9c3-0000f80367c1                   |
| Синтаксис            | [**Перечисление**](s-enumeration.md)                   |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Верно                                         |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**DHCP-класс**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Верно                                         |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**DHCP-класс**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Верно                                         |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**DHCP-класс**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Верно                                         |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**DHCP-класс**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Верно                                         |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**DHCP-класс**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Верно                                         |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**DHCP-класс**](c-dhcpclass.md)<br/> |



 

 





