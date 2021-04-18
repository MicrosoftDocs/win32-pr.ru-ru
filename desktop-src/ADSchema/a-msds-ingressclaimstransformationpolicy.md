---
title: MS-DS-входящие-Claims-преобразование-атрибут политики
description: Это ссылка на объект политики преобразования утверждений для входящих утверждений (утверждений, поступающих в этот лес) из доверенного домена.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- MS-DS-входящий-Claims-преобразование-схема AD атрибута политики
- Схема AD атрибута msDS-Ингрессклаимстрансформатионполици
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536038"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a>MS-DS-входящие-Claims-преобразование-атрибут политики

Это ссылка на объект политики преобразования утверждений для входящих утверждений (утверждений, поступающих в этот лес) из доверенного домена. Это применимо только к исходящему или двунаправленному доверию между лесами. Если эта ссылка отсутствует, все входящие утверждения будут удалены.



| Ввод | Значение |
|-------------------|--------------------------------------------|
| CN                | MS-DS-входящие-Claims-преобразование — политика |
| LDAP-отображаемое имя | msDS-Ингрессклаимстрансформатионполици     |
| Размер              | \-                                         |
| Привилегия обновления  | \-                                         |
| Частота обновления  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.2191                    |
| System-ID — GUID    | 86284c08-0c6e-1540-8b15-75147d23d20d       |
| Синтаксис            | [**Object(DS-DN)**](s-object-ds-dn.md)    |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | 2190                                                 |
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



 

 





