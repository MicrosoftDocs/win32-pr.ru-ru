---
title: ACS-ДСБМ — атрибут priority
description: Эти атрибуты содержат приоритет для этого диспетчера пропускной способности подсети (СБМ).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-ДСБМ — схема AD атрибута priority
- Схема AD атрибута Аксдсбмприорити
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7a80c9c866b5c91f83f884ecaafe60e4596af4ca8d625791ed9264679c356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637494"
---
# <a name="acs-dsbm-priority-attribute"></a>ACS-ДСБМ — атрибут priority

Эти атрибуты содержат приоритет для этого диспетчера пропускной способности подсети (СБМ). Если необходимо указать новый назначенный диспетчер пропускной способности подсети (ДСБМ), это значение отправляется в другие СБМС в домене как часть сообщения с \_ запросом ДСБМ. СБМ с наивысшим приоритетом выбирается в качестве нового ДСБМ.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | ACS — ДСБМ — приоритет                    |
| LDAP-отображаемое имя | аксдсбмприорити                      |
| Размер              | 4 байта                              |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.776               |
| System-ID — GUID    | 1cb3559e-56d0-11d1-a9c6-0000f80367c1 |
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
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**ACS — подсеть**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**ACS — подсеть**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**ACS — подсеть**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**ACS — подсеть**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**ACS — подсеть**](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------|
| Идентификатор ссылки                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Неверно                                        |
| Является однозначным       | Верно                                         |
| Индексируется             | Неверно                                        |
| В глобальном каталоге      | Неверно                                        |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Классы, используемые в        | [**ACS — подсеть**](c-acssubnet.md)<br/> |



 

 





