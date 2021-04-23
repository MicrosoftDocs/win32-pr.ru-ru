---
title: MS-DNS-Secure-делегирование — атрибут периода опроса
description: Атрибут, определяющий время между попытками опроса при смене ключей дочерней зоны в секундах.
ms.assetid: 2fc45592-30df-4317-8122-d22b5e6e2ee0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута периода опроса MS-DNS-Secure-делегирования
- msDN — схема AD атрибута Секуределегатионполлингпериод
topic_type:
- apiref
api_name:
- ms-DNS-Secure-Delegation-Polling-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c724196684fce5e8d104d4a01903a59fc38ac880
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138678"
---
# <a name="ms-dns-secure-delegation-polling-period-attribute"></a><span data-ttu-id="b96dd-105">MS-DNS-Secure-делегирование — атрибут периода опроса</span><span class="sxs-lookup"><span data-stu-id="b96dd-105">ms-DNS-Secure-Delegation-Polling-Period attribute</span></span>

<span data-ttu-id="b96dd-106">Атрибут, определяющий время между попытками опроса при смене ключей дочерней зоны в секундах.</span><span class="sxs-lookup"><span data-stu-id="b96dd-106">An attribute that defines in seconds the time between polling attempts for child zone key rollovers.</span></span>



| <span data-ttu-id="b96dd-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b96dd-107">Entry</span></span> | <span data-ttu-id="b96dd-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b96dd-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b96dd-109">CN</span><span class="sxs-lookup"><span data-stu-id="b96dd-109">CN</span></span>                | <span data-ttu-id="b96dd-110">MS-DNS-Secure-делегирование-опрос — период</span><span class="sxs-lookup"><span data-stu-id="b96dd-110">ms-DNS-Secure-Delegation-Polling-Period</span></span> |
| <span data-ttu-id="b96dd-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b96dd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b96dd-112">msDN — Секуределегатионполлингпериод</span><span class="sxs-lookup"><span data-stu-id="b96dd-112">msDNS-SecureDelegationPollingPeriod</span></span>     |
| <span data-ttu-id="b96dd-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b96dd-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="b96dd-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b96dd-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="b96dd-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b96dd-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="b96dd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b96dd-116">Attribute-Id</span></span>      | <span data-ttu-id="b96dd-117">1.2.840.113556.1.4.2142</span><span class="sxs-lookup"><span data-stu-id="b96dd-117">1.2.840.113556.1.4.2142</span></span>                 |
| <span data-ttu-id="b96dd-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b96dd-118">System-Id-Guid</span></span>    | <span data-ttu-id="b96dd-119">f6b0f0be-a8e4-4468-8fd9-c3c47b8722f9</span><span class="sxs-lookup"><span data-stu-id="b96dd-119">f6b0f0be-a8e4-4468-8fd9-c3c47b8722f9</span></span>    |
| <span data-ttu-id="b96dd-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b96dd-120">Syntax</span></span>            | [<span data-ttu-id="b96dd-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="b96dd-121">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="b96dd-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b96dd-122">Implementations</span></span>

-   [<span data-ttu-id="b96dd-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b96dd-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="b96dd-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b96dd-124">Windows Server 2012</span></span>



| <span data-ttu-id="b96dd-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="b96dd-125">Entry</span></span> | <span data-ttu-id="b96dd-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b96dd-126">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b96dd-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b96dd-127">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="b96dd-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b96dd-128">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="b96dd-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="b96dd-129">System-Only</span></span>            | <span data-ttu-id="b96dd-130">Неверно</span><span class="sxs-lookup"><span data-stu-id="b96dd-130">False</span></span>                                    |
| <span data-ttu-id="b96dd-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b96dd-131">Is-Single-Valued</span></span>       | <span data-ttu-id="b96dd-132">True</span><span class="sxs-lookup"><span data-stu-id="b96dd-132">True</span></span>                                     |
| <span data-ttu-id="b96dd-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b96dd-133">Is Indexed</span></span>             | <span data-ttu-id="b96dd-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="b96dd-134">False</span></span>                                    |
| <span data-ttu-id="b96dd-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b96dd-135">In Global Catalog</span></span>      | <span data-ttu-id="b96dd-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="b96dd-136">False</span></span>                                    |
| <span data-ttu-id="b96dd-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b96dd-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="b96dd-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b96dd-138">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b96dd-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b96dd-139">Range-Lower</span></span>            | <span data-ttu-id="b96dd-140">0</span><span class="sxs-lookup"><span data-stu-id="b96dd-140">0</span></span>                                        |
| <span data-ttu-id="b96dd-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b96dd-141">Range-Upper</span></span>            | <span data-ttu-id="b96dd-142">2592000</span><span class="sxs-lookup"><span data-stu-id="b96dd-142">2592000</span></span>                                  |
| <span data-ttu-id="b96dd-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b96dd-143">Search-Flags</span></span>           | <span data-ttu-id="b96dd-144">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b96dd-144">0x00000008</span></span>                               |
| <span data-ttu-id="b96dd-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b96dd-145">System-Flags</span></span>           | <span data-ttu-id="b96dd-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b96dd-146">0x00000010</span></span>                               |
| <span data-ttu-id="b96dd-147">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b96dd-147">Classes used in</span></span>        | [<span data-ttu-id="b96dd-148">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="b96dd-148">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





