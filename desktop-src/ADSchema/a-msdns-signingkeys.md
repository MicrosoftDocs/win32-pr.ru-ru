---
title: атрибут MS-DNS-Sign-Keys
description: Атрибут, содержащий набор зашифрованных ключей подписывания DNSSEC, используемых DNS-сервером для подписывания зоны DNS.
ms.assetid: 99aa1541-eb3f-48ee-b449-a16c17e9c002
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибутов ключей MS-DNS-Sign-Keys
- msDN — схема AD атрибута Сигнингкэйс
topic_type:
- apiref
api_name:
- ms-DNS-Signing-Keys
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e80d81ed984e0ac96aba1793458b5577173c7e7c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494058"
---
# <a name="ms-dns-signing-keys-attribute"></a><span data-ttu-id="3bc6a-105">атрибут MS-DNS-Sign-Keys</span><span class="sxs-lookup"><span data-stu-id="3bc6a-105">ms-DNS-Signing-Keys attribute</span></span>

<span data-ttu-id="3bc6a-106">Атрибут, содержащий набор зашифрованных ключей подписывания DNSSEC, используемых DNS-сервером для подписывания зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="3bc6a-106">An attribute that contains the set of encrypted DNSSEC signing keys used by the DNS server to sign the DNS zone.</span></span>



| <span data-ttu-id="3bc6a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="3bc6a-107">Entry</span></span> | <span data-ttu-id="3bc6a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3bc6a-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="3bc6a-109">CN</span><span class="sxs-lookup"><span data-stu-id="3bc6a-109">CN</span></span>                | <span data-ttu-id="3bc6a-110">Ключи для подписывания MS-DNS</span><span class="sxs-lookup"><span data-stu-id="3bc6a-110">ms-DNS-Signing-Keys</span></span>                                   |
| <span data-ttu-id="3bc6a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3bc6a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3bc6a-112">msDN — Сигнингкэйс</span><span class="sxs-lookup"><span data-stu-id="3bc6a-112">msDNS-SigningKeys</span></span>                                     |
| <span data-ttu-id="3bc6a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="3bc6a-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="3bc6a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3bc6a-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="3bc6a-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3bc6a-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="3bc6a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3bc6a-116">Attribute-Id</span></span>      | <span data-ttu-id="3bc6a-117">1.2.840.113556.1.4.2144</span><span class="sxs-lookup"><span data-stu-id="3bc6a-117">1.2.840.113556.1.4.2144</span></span>                               |
| <span data-ttu-id="3bc6a-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3bc6a-118">System-Id-Guid</span></span>    | <span data-ttu-id="3bc6a-119">b7673e6d-cad9-4e9e-b31a-63e8098fdd63</span><span class="sxs-lookup"><span data-stu-id="3bc6a-119">b7673e6d-cad9-4e9e-b31a-63e8098fdd63</span></span>                  |
| <span data-ttu-id="3bc6a-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bc6a-120">Syntax</span></span>            | [<span data-ttu-id="3bc6a-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="3bc6a-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="3bc6a-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3bc6a-122">Implementations</span></span>

-   [<span data-ttu-id="3bc6a-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3bc6a-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="3bc6a-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bc6a-124">Windows Server 2012</span></span>



| <span data-ttu-id="3bc6a-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="3bc6a-125">Entry</span></span> | <span data-ttu-id="3bc6a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3bc6a-126">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="3bc6a-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3bc6a-127">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="3bc6a-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3bc6a-128">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="3bc6a-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="3bc6a-129">System-Only</span></span>            | <span data-ttu-id="3bc6a-130">Неверно</span><span class="sxs-lookup"><span data-stu-id="3bc6a-130">False</span></span>                                    |
| <span data-ttu-id="3bc6a-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3bc6a-131">Is-Single-Valued</span></span>       | <span data-ttu-id="3bc6a-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="3bc6a-132">False</span></span>                                    |
| <span data-ttu-id="3bc6a-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3bc6a-133">Is Indexed</span></span>             | <span data-ttu-id="3bc6a-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="3bc6a-134">False</span></span>                                    |
| <span data-ttu-id="3bc6a-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3bc6a-135">In Global Catalog</span></span>      | <span data-ttu-id="3bc6a-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="3bc6a-136">False</span></span>                                    |
| <span data-ttu-id="3bc6a-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3bc6a-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="3bc6a-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3bc6a-138">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="3bc6a-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3bc6a-139">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="3bc6a-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3bc6a-140">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="3bc6a-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3bc6a-141">Search-Flags</span></span>           | <span data-ttu-id="3bc6a-142">0x00000008</span><span class="sxs-lookup"><span data-stu-id="3bc6a-142">0x00000008</span></span>                               |
| <span data-ttu-id="3bc6a-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3bc6a-143">System-Flags</span></span>           | <span data-ttu-id="3bc6a-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3bc6a-144">0x00000010</span></span>                               |
| <span data-ttu-id="3bc6a-145">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3bc6a-145">Classes used in</span></span>        | [<span data-ttu-id="3bc6a-146">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="3bc6a-146">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





