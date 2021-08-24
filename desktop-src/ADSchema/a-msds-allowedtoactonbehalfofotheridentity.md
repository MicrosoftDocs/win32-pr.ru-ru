---
title: Атрибут ms-DS-Allowed-to-акту-On-My-Identity
description: Этот атрибут используется для проверки доступа, чтобы определить, имеет ли запрашивающий разрешение на действия от имени других удостоверений для служб, выполняющихся в качестве этой учетной записи.
ms.assetid: 38203665-4505-461b-b6ab-b634725ac2fa
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута Identity в службе MS-DS-Allowed-to-"
- Схема AD атрибута msDS-AllowedToActOnBehalfOfOtherIdentity
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3ea9795dd89777d390235193ff2663e5b514125cdf539c34dfc85ad1664bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119552844"
---
# <a name="ms-ds-allowed-to-act-on-behalf-of-other-identity-attribute"></a>Атрибут ms-DS-Allowed-to-акту-On-My-Identity

Этот атрибут используется для проверки доступа, чтобы определить, имеет ли запрашивающий разрешение на действия от имени других удостоверений для служб, выполняющихся в качестве этой учетной записи.



| Ввод | Значение |
|-------------------|-----------------------------------------------------|
| CN                | MS-DS-Allowed-to-"Active-on-чужое удостоверение"    |
| LDAP-отображаемое имя | msDS-AllowedToActOnBehalfOfOtherIdentity            |
| Размер              | \-                                                  |
| Привилегия обновления  | \-                                                  |
| Частота обновления  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.4.2182                             |
| System-ID — GUID    | 3f78c3e5-f79a-46bd-a0b8-9d18116ddc79                |
| Синтаксис            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|--------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Верно                                                               |
| Является однозначным       | Верно                                                               |
| Индексируется             | Нет                                                              |
| В глобальном каталоге      | Нет                                                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                       |
| Range-Lower            | 0                                                                  |
| Range-Upper            | 132096                                                             |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Классы, используемые в        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





