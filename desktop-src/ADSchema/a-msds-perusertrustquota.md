---
title: Атрибут квоты MS-DS-на пользователя (Trust)
description: Используется для принудительного применения квоты для каждого пользователя при создании Trusted-Domain объектов, которым разрешено право на доступ к новому элементу управления, CREATE-Inbound-лесами-Trust.
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута квоты MS-DS-на пользователя и доверия
- Схема AD атрибута msDS-Перусертрусткуота
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fc51a6e3e3e9f3d14534487590985197ed7c97fbca8bc1042108bfcdba97530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425830"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a>Атрибут квоты MS-DS-на пользователя (Trust)

Используется для принудительного применения квоты для каждого пользователя при создании Trusted-Domain объектов, которым разрешено право на доступ к новому элементу управления, CREATE-Inbound-лесами-Trust. Этот атрибут ограничивает количество объектов Trusted-Domain, которые могут быть созданы одним пользователем без прав администратора.



| Ввод | Значение |
|-------------------|-------------------------------------------|
| CN                | Квота MS-DS-на пользователя — доверие                |
| LDAP-отображаемое имя | msDS-Перусертрусткуота                    |
| Размер              | \-                                        |
| Привилегия обновления  | Администратор домена                      |
| Частота обновления  | При создании леса и редко после него. |
| Attribute-Id      | 1.2.840.113556.1.4.1788                   |
| System-ID — GUID    | d161adf0-ca24-4993-a3aa-8b2c981302e8      |
| Синтаксис            | [**Перечисление**](s-enumeration.md)      |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Нет                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Нет                                        |
| В глобальном каталоге      | Нет                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Нет                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Нет                                        |
| В глобальном каталоге      | Нет                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Нет                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Нет                                        |
| В глобальном каталоге      | Нет                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Нет                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Нет                                        |
| В глобальном каталоге      | Нет                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Нет                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Нет                                        |
| В глобальном каталоге      | Нет                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**SAM-домен**](c-samdomain.md)<br/> |



 

 





