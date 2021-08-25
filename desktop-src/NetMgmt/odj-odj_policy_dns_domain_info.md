---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: Определение ODJ_POLICY_DNS_DOMAIN_INFO IDL
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d0a83ccade72a11449ca0cc9b35b9fc58e9c53d48f8248a9f6074cdb087cc0c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911603"
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
