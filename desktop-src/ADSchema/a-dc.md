---
title: Атрибут Domain-Component
description: Атрибут именования для объектов Domain и DNS. Обычно отображается как DC имя_домена.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Domain-Component
- Схема AD атрибута контроллера домена
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe93b6629ac176452edbe5cdf13bf35afa955890cde369273f87990034bcd3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177777"
---
# <a name="domain-component-attribute"></a>Атрибут Domain-Component

Атрибут именования для объектов Domain и DNS. Обычно отображается как DC = имя_домена.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | Domain-Component                            |
| LDAP-отображаемое имя | dc                                          |
| Размер              | \-                                          |
| Привилегия обновления  | Администратор домена                        |
| Частота обновления  | При создании домена.                 |
| Attribute-Id      | 0.9.2342.19200300.100.1.25                  |
| System-ID — GUID    | 19195a55-6da0-11d0-afd3-00c04fd930c9        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Нет                                                                                                                   |
| Является однозначным       | True                                                                                                                    |
| Индексируется             | Нет                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> [**DNS — зона**](c-dnszone.md)<br/> [**Поддомен**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Нет                                                                                                                   |
| Является однозначным       | True                                                                                                                    |
| Индексируется             | Нет                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> [**DNS — зона**](c-dnszone.md)<br/> [**Поддомен**](c-domain.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|---------------------------------------|
| Идентификатор ссылки                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Нет                                 |
| Является однозначным       | True                                  |
| Индексируется             | Нет                                 |
| В глобальном каталоге      | True                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 255                                   |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000012                            |
| Классы, используемые в        | [**Поддомен**](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Нет                                                                                                                   |
| Является однозначным       | True                                                                                                                    |
| Индексируется             | Нет                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> [**DNS — зона**](c-dnszone.md)<br/> [**Поддомен**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Нет                                                                                                                   |
| Является однозначным       | True                                                                                                                    |
| Индексируется             | Нет                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> [**DNS — зона**](c-dnszone.md)<br/> [**Поддомен**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Нет                                                                                                                   |
| Является однозначным       | True                                                                                                                    |
| Индексируется             | Нет                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> [**DNS — зона**](c-dnszone.md)<br/> [**Поддомен**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Нет                                                                                                                   |
| Является однозначным       | True                                                                                                                    |
| Индексируется             | Нет                                                                                                                   |
| В глобальном каталоге      | True                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Классы, используемые в        | [**DNS-узел**](c-dnsnode.md)<br/> [**DNS — зона**](c-dnszone.md)<br/> [**Поддомен**](c-domain.md)<br/> |



 

 





