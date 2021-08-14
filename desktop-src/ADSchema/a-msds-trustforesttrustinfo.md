---
title: Атрибут ms-DS-Trust-лесом-Trust-info
description: Содержит сведения о доверии лесов (двоичный BLOB-объект), используемый системой для объекта Trusted-Domain.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-Trust-лесом-Trust-info
- Схема AD атрибута msDS-Трустфоресттрустинфо
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae350001aa616052c1f0358497364ecfbce55d40e91314c56100d12848efc0ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960573"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a>Атрибут ms-DS-Trust-лесом-Trust-info

Содержит сведения о доверии лесов (двоичный BLOB-объект), используемый системой для объекта Trusted-Domain.



| Ввод | Значение |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-Trust-лес-Trust-сведения                                                                                      |
| LDAP-отображаемое имя | msDS-Трустфоресттрустинфо                                                                                          |
| Размер              | \-                                                                                                                 |
| Привилегия обновления  | \-                                                                                                                 |
| Частота обновления  | Только при изменении отношения доверия между лесами. Это может произойти при изменении топологии доверенного леса. |
| Attribute-Id      | 1.2.840.113556.1.4.1702                                                                                            |
| System-ID — GUID    | 29cc866e-49d3-4969-942e-1dbc0925d183                                                                               |
| Синтаксис            | [**Object(ссылка_на_реплику)**](s-object-replica-link.md)                                                              |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Неверно                                                |
| Является однозначным       | Верно                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | Верно                                                 |
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
| Является однозначным       | Верно                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | Верно                                                 |
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
| Является однозначным       | Верно                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | Верно                                                 |
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
| Является однозначным       | Верно                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | Верно                                                 |
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
| Является однозначным       | Верно                                                 |
| Индексируется             | Неверно                                                |
| В глобальном каталоге      | Верно                                                 |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



 

 





