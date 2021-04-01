---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: Определение ODJ_POLICY_DNS_DOMAIN_INFO IDL
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "103797167"
---
# <a name="odj_policy_dns_domain_info-structure"></a>Структура ODJ_POLICY_DNS_DOMAIN_INFO

Содержит сведения о домене и лесу, к которым должен быть присоединен клиент.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a>Члены

### <a name="name"></a>Имя

Необходимо задать NetBIOS-имя домена.

### <a name="dnsdomainname"></a>DnsDomainName

Необходимо задать имя домена в формате DNS.

### <a name="dnsforestname"></a>днсфорестнаме

Необходимо задать имя леса в формате DNS.

### <a name="domainguid"></a>домаингуид

Необходимо задать идентификатор GUID домена.

### <a name="sid"></a>Sid

Необходимо задать идентификатор безопасности домена.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

[**\_строка Юникода \_ ODJ**](odj-odj_unicode_string.md)

[**\_идентификатор безопасности ODJ**](odj-odj_sid.md)
