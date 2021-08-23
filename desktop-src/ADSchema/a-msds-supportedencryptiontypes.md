---
title: Атрибут ms-DS-Supported-Encryption-Types
description: Алгоритмы шифрования, поддерживаемые учетными записями пользователя, компьютера или доверия. Примечание. в KDC эти сведения используются при создании билета службы для этой учетной записи.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- служба MS-DS-Supported-Encryption-Types Attribute AD Schema
- Схема AD атрибута msDS-Суппортеденкриптионтипес
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d092061dfebcea8e9a0e4f4a060010e16102108d1e2e74f05e6df2db706141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544344"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>Атрибут ms-DS-Supported-Encryption-Types

Алгоритмы шифрования, поддерживаемые учетными записями пользователя, компьютера или доверия.

> [!Note]  
> KDC использует эти сведения при создании билета службы для этой учетной записи. Службы и компьютеры могут автоматически обновлять этот атрибут в соответствующих учетных записях в Active Directory и поэтому должны иметь доступ на запись к этому атрибуту.

 



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MS-DS-Supported-Encryption-Types     |
| LDAP-отображаемое имя | msDS-Суппортеденкриптионтипес        |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-ID — GUID    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
| Синтаксис            | [**Перечисление**](s-enumeration.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Нет                                                                                  |
| Является однозначным       | Верно                                                                                   |
| Индексируется             | Нет                                                                                  |
| В глобальном каталоге      | Нет                                                                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Нет                                                                                  |
| Является однозначным       | Верно                                                                                   |
| Индексируется             | Нет                                                                                  |
| В глобальном каталоге      | Нет                                                                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|----------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Нет                                                                                  |
| Является однозначным       | Верно                                                                                   |
| Индексируется             | Нет                                                                                  |
| В глобальном каталоге      | Нет                                                                                  |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> [**Пользователь**](c-user.md)<br/> |



 

 





