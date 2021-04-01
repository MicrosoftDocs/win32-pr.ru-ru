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
# <a name="odj_policy_dns_domain_info-structure"></a><span data-ttu-id="6b3c7-103">Структура ODJ_POLICY_DNS_DOMAIN_INFO</span><span class="sxs-lookup"><span data-stu-id="6b3c7-103">ODJ_POLICY_DNS_DOMAIN_INFO structure</span></span>

<span data-ttu-id="6b3c7-104">Содержит сведения о домене и лесу, к которым должен быть присоединен клиент.</span><span class="sxs-lookup"><span data-stu-id="6b3c7-104">Contains information about the domain and forest that a client should be joined to.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b3c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b3c7-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="6b3c7-106">Члены</span><span class="sxs-lookup"><span data-stu-id="6b3c7-106">Members</span></span>

### <a name="name"></a><span data-ttu-id="6b3c7-107">Имя</span><span class="sxs-lookup"><span data-stu-id="6b3c7-107">Name</span></span>

<span data-ttu-id="6b3c7-108">Необходимо задать NetBIOS-имя домена.</span><span class="sxs-lookup"><span data-stu-id="6b3c7-108">Must be set to a Netbios domain name.</span></span>

### <a name="dnsdomainname"></a><span data-ttu-id="6b3c7-109">DnsDomainName</span><span class="sxs-lookup"><span data-stu-id="6b3c7-109">DnsDomainName</span></span>

<span data-ttu-id="6b3c7-110">Необходимо задать имя домена в формате DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3c7-110">Must be set to a domain name in DNS format.</span></span>

### <a name="dnsforestname"></a><span data-ttu-id="6b3c7-111">днсфорестнаме</span><span class="sxs-lookup"><span data-stu-id="6b3c7-111">DnsForestName</span></span>

<span data-ttu-id="6b3c7-112">Необходимо задать имя леса в формате DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3c7-112">Must be set to a forest name in DNS format.</span></span>

### <a name="domainguid"></a><span data-ttu-id="6b3c7-113">домаингуид</span><span class="sxs-lookup"><span data-stu-id="6b3c7-113">DomainGuid</span></span>

<span data-ttu-id="6b3c7-114">Необходимо задать идентификатор GUID домена.</span><span class="sxs-lookup"><span data-stu-id="6b3c7-114">Must be set to the domain guid.</span></span>

### <a name="sid"></a><span data-ttu-id="6b3c7-115">Sid</span><span class="sxs-lookup"><span data-stu-id="6b3c7-115">Sid</span></span>

<span data-ttu-id="6b3c7-116">Необходимо задать идентификатор безопасности домена.</span><span class="sxs-lookup"><span data-stu-id="6b3c7-116">Must be set to the domain sid.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b3c7-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b3c7-117">See also</span></span>

[<span data-ttu-id="6b3c7-118">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="6b3c7-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="6b3c7-119">**\_строка Юникода \_ ODJ**</span><span class="sxs-lookup"><span data-stu-id="6b3c7-119">**ODJ\_UNICODE\_STRING**</span></span>](odj-odj_unicode_string.md)

[<span data-ttu-id="6b3c7-120">**\_идентификатор безопасности ODJ**</span><span class="sxs-lookup"><span data-stu-id="6b3c7-120">**ODJ\_SID**</span></span>](odj-odj_sid.md)
