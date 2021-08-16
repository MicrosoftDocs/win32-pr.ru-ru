---
title: ms-DS-Egress-claims-преобразование — атрибут политики
description: Это ссылка на объект политики преобразования утверждений для исходящих утверждений (утверждений, походящих из этого леса) в доверенный домен.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- active-DS-Egress-claims-преобразование — схема AD атрибута политики
- Схема AD атрибута msDS-Егрессклаимстрансформатионполици
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ec71308c0ebc17942b3400d8ddd9e87ff88ea29d4f21e93047c3aa80f77128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118014657"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a>ms-DS-Egress-claims-преобразование — атрибут политики

Это ссылка на объект политики преобразования утверждений для исходящих утверждений (утверждений, походящих из этого леса) в доверенный домен. Это применимо только к входящему или двунаправленному доверию между лесами. Если эта ссылка отсутствует, все утверждения разрешены для исходящего трафика "как есть".



| Ввод | Значение |
|-------------------|-------------------------------------------|
| CN                | ms-DS-Egress-claims-преобразование — политика |
| LDAP-отображаемое имя | msDS-Егрессклаимстрансформатионполици     |
| Размер              | \-                                        |
| Привилегия обновления  | \-                                        |
| Частота обновления  | \-                                        |
| Attribute-Id      | 1.2.840.113556.1.4.2192                   |
| System-ID — GUID    | c137427e-9a73-b040-9190-1b095bb43288      |
| Синтаксис            | [**Object(DS-DN)**](s-object-ds-dn.md)   |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|------------------------------------------------------|
| Идентификатор ссылки                | 2192                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | Нет.                                                |
| Является однозначным       | Верно                                                 |
| Индексируется             | Нет.                                                |
| В глобальном каталоге      | Нет.                                                |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Классы, используемые в        | [**Доверенный домен**](c-trusteddomain.md)<br/> |



 

 





