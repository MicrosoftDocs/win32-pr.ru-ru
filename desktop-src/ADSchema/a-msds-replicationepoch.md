---
title: Атрибут ms-DS-Репликатионепоч
description: Он используется для хранения эпохи, при которой реплицируются все контроллеры домена. Эпоха — это период времени, в течение которого домен имеет определенное имя. Новый эпоха начинается, когда происходит изменение доменного имени.
ms.assetid: d8a3c4fd-f416-483f-820f-7b3182d0bfc3
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-Репликатионепоч
- Схема AD атрибута msDS-Репликатионепоч
topic_type:
- apiref
api_name:
- ms-DS-ReplicationEpoch
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9aaefefe5cd1ae269508390ae13f67037fdb8a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536005"
---
# <a name="ms-ds-replicationepoch-attribute"></a>Атрибут ms-DS-Репликатионепоч

Он используется для хранения эпохи, при которой реплицируются все контроллеры домена. Эпоха — это период времени, в течение которого домен имеет определенное имя. Новый эпоха начинается, когда происходит изменение доменного имени.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MS-DS-Репликатионепоч               |
| LDAP-отображаемое имя | msDS-Репликатионепоч                |
| Размер              | \-                                   |
| Привилегия обновления  | Это значение задается системой.     |
| Частота обновления  | Только во время реструктуризации домена.      |
| Attribute-Id      | 1.2.840.113556.1.4.1720              |
| System-ID — GUID    | 08e3aa79-eb1c-45b5-af7b-8f94246c8e41 |
| Синтаксис            | [**Перечисление**](s-enumeration.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | Неверно                                    |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000011                               |
| Классы, используемые в        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | Неверно                                    |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000011                               |
| Классы, используемые в        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | Неверно                                    |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000011                               |
| Классы, используемые в        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | Неверно                                    |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000011                               |
| Классы, используемые в        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | Неверно                                    |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000011                               |
| Классы, используемые в        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------|
| Идентификатор ссылки                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Неверно                                    |
| Является однозначным       | True                                     |
| Индексируется             | Неверно                                    |
| В глобальном каталоге      | Неверно                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000011                               |
| Классы, используемые в        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





