---
title: атрибут MS-DNS-NSEC3-User-Salt
description: Атрибут, определяющий указанную пользователем строку NSEC3, используемую при подписывании зоны DNS. Если значение пустое, будет использоваться случайная соль.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DNS-NSEC3-User-соли
- msDN — схема AD атрибута NSEC3UserSalt
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d28acb28dec95ef13afc37f9d7f26d713d5cf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804715"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a>атрибут MS-DNS-NSEC3-User-Salt

Атрибут, определяющий указанную пользователем строку NSEC3, используемую при подписывании зоны DNS. Если значение пустое, будет использоваться случайная соль.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | MS-DNS-NSEC3-User-Salt                      |
| LDAP-отображаемое имя | msDN — NSEC3UserSalt                         |
| Размер              | \-                                          |
| Привилегия обновления  | \-                                          |
| Частота обновления  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.2148                     |
| System-ID — GUID    | aff16770-9622-4fbc-a128-3088777605b9        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2012**](#windows-server-2012)

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
| Range-Lower            | 0                                        |
| Range-Upper            | 510                                      |
| Search-Flags           | 0x00000008                               |
| System-Flags           | 0x00000010                               |
| Классы, используемые в        | [**DNS — зона**](c-dnszone.md)<br/> |



 

 





