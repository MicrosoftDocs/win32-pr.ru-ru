---
title: ODJ_WIN7BLOB
description: Определение ODJ_WIN7BLOB IDL
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104339565"
---
# <a name="odj_win7blob-structure"></a><span data-ttu-id="a256d-103">Структура ODJ_WIN7BLOB</span><span class="sxs-lookup"><span data-stu-id="a256d-103">ODJ_WIN7BLOB structure</span></span>

<span data-ttu-id="a256d-104">Содержит основные сведения, необходимые для приподключения клиента к домену.</span><span class="sxs-lookup"><span data-stu-id="a256d-104">Contains the basic information required to join a client to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="a256d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a256d-105">Syntax</span></span>

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a><span data-ttu-id="a256d-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a256d-106">Members</span></span>

### <a name="lpdomain"></a><span data-ttu-id="a256d-107">лпдомаин</span><span class="sxs-lookup"><span data-stu-id="a256d-107">lpDomain</span></span>

<span data-ttu-id="a256d-108">Необходимо задать имя домена.</span><span class="sxs-lookup"><span data-stu-id="a256d-108">Must be set to the domain name.</span></span>

### <a name="lpmachinename"></a><span data-ttu-id="a256d-109">лпмачиненаме</span><span class="sxs-lookup"><span data-stu-id="a256d-109">lpMachineName</span></span>

<span data-ttu-id="a256d-110">Необходимо задать имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="a256d-110">Must be set to the machine name.</span></span>

### <a name="lpmachinepassword"></a><span data-ttu-id="a256d-111">лпмачинепассворд</span><span class="sxs-lookup"><span data-stu-id="a256d-111">lpMachinePassword</span></span>

<span data-ttu-id="a256d-112">Необходимо задать пароль открытым текстом для учетной записи компьютера, идентифицируемой Лпмачиненаме</span><span class="sxs-lookup"><span data-stu-id="a256d-112">Must be set to a cleartext password for the machine account identified by lpMachineName</span></span>

### <a name="dnsdomaininfo"></a><span data-ttu-id="a256d-113">днсдомаининфо</span><span class="sxs-lookup"><span data-stu-id="a256d-113">DnsDomainInfo</span></span>

<span data-ttu-id="a256d-114">Содержит сведения о присоединенном домене.</span><span class="sxs-lookup"><span data-stu-id="a256d-114">Contains information about the domain being joined.</span></span>

### <a name="dcinfo"></a><span data-ttu-id="a256d-115">дЦинфо</span><span class="sxs-lookup"><span data-stu-id="a256d-115">DcInfo</span></span>

<span data-ttu-id="a256d-116">Содержит сведения об именовании и адресации контроллера домена, который использовался для создания учетной записи компьютера Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a256d-116">Contains naming and addressing information about the domain controller that was used to create the machine account Active Directory.</span></span>

### <a name="options"></a><span data-ttu-id="a256d-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="a256d-117">Options</span></span>

<span data-ttu-id="a256d-118">Необходимо задать значение 0.</span><span class="sxs-lookup"><span data-stu-id="a256d-118">Must be set to zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="a256d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a256d-119">See also</span></span>

[<span data-ttu-id="a256d-120">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="a256d-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="a256d-121">**\_ \_ \_ сведения о DNS-домене политики \_ ODJ**</span><span class="sxs-lookup"><span data-stu-id="a256d-121">**ODJ\_POLICY\_DNS\_DOMAIN\_INFO**</span></span>](odj-odj_policy_dns_domain_info.md)

[<span data-ttu-id="a256d-122">**DOMAIN_CONTROLLER_INFOW**</span><span class="sxs-lookup"><span data-stu-id="a256d-122">**DOMAIN_CONTROLLER_INFOW**</span></span>](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



