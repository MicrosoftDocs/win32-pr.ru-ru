---
title: Атрибут времени распространения MS-DNS
description: Атрибут, используемый для определения в секундах ожидаемого времени, необходимого для распространения изменений зоны с помощью Active Directory.
ms.assetid: ca48d956-f88f-440f-bbc9-23015130f393
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута времени распространения MS-DNS
- msDN — схема AD атрибута Пропагатионтиме
topic_type:
- apiref
api_name:
- ms-DNS-Propagation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6885d9dabb1d5d41cec20cc6922671f54b1a8a1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893545"
---
# <a name="ms-dns-propagation-time-attribute"></a><span data-ttu-id="d31a9-105">Атрибут времени распространения MS-DNS</span><span class="sxs-lookup"><span data-stu-id="d31a9-105">ms-DNS-Propagation-Time attribute</span></span>

<span data-ttu-id="d31a9-106">Атрибут, используемый для определения в секундах ожидаемого времени, необходимого для распространения изменений зоны с помощью Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d31a9-106">An attribute used to define in seconds the expected time required to propagate zone changes through Active Directory.</span></span>



| <span data-ttu-id="d31a9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d31a9-107">Entry</span></span> | <span data-ttu-id="d31a9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d31a9-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="d31a9-109">CN</span><span class="sxs-lookup"><span data-stu-id="d31a9-109">CN</span></span>                | <span data-ttu-id="d31a9-110">MS-DNS-распространение-время</span><span class="sxs-lookup"><span data-stu-id="d31a9-110">ms-DNS-Propagation-Time</span></span>              |
| <span data-ttu-id="d31a9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d31a9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d31a9-112">msDN — Пропагатионтиме</span><span class="sxs-lookup"><span data-stu-id="d31a9-112">msDNS-PropagationTime</span></span>                |
| <span data-ttu-id="d31a9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d31a9-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="d31a9-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d31a9-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="d31a9-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d31a9-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="d31a9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d31a9-116">Attribute-Id</span></span>      | <span data-ttu-id="d31a9-117">1.2.840.113556.1.4.2147</span><span class="sxs-lookup"><span data-stu-id="d31a9-117">1.2.840.113556.1.4.2147</span></span>              |
| <span data-ttu-id="d31a9-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d31a9-118">System-Id-Guid</span></span>    | <span data-ttu-id="d31a9-119">ba340d47-2181-4ca0-a2f6-fae4479dab2a</span><span class="sxs-lookup"><span data-stu-id="d31a9-119">ba340d47-2181-4ca0-a2f6-fae4479dab2a</span></span> |
| <span data-ttu-id="d31a9-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d31a9-120">Syntax</span></span>            | [<span data-ttu-id="d31a9-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="d31a9-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="d31a9-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d31a9-122">Implementations</span></span>

-   [<span data-ttu-id="d31a9-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d31a9-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="d31a9-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d31a9-124">Windows Server 2012</span></span>



| <span data-ttu-id="d31a9-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="d31a9-125">Entry</span></span> | <span data-ttu-id="d31a9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d31a9-126">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d31a9-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d31a9-127">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="d31a9-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d31a9-128">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d31a9-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="d31a9-129">System-Only</span></span>            | <span data-ttu-id="d31a9-130">Неверно</span><span class="sxs-lookup"><span data-stu-id="d31a9-130">False</span></span>                                    |
| <span data-ttu-id="d31a9-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d31a9-131">Is-Single-Valued</span></span>       | <span data-ttu-id="d31a9-132">True</span><span class="sxs-lookup"><span data-stu-id="d31a9-132">True</span></span>                                     |
| <span data-ttu-id="d31a9-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d31a9-133">Is Indexed</span></span>             | <span data-ttu-id="d31a9-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="d31a9-134">False</span></span>                                    |
| <span data-ttu-id="d31a9-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d31a9-135">In Global Catalog</span></span>      | <span data-ttu-id="d31a9-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="d31a9-136">False</span></span>                                    |
| <span data-ttu-id="d31a9-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d31a9-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="d31a9-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d31a9-138">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d31a9-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d31a9-139">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d31a9-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d31a9-140">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d31a9-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d31a9-141">Search-Flags</span></span>           | <span data-ttu-id="d31a9-142">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d31a9-142">0x00000008</span></span>                               |
| <span data-ttu-id="d31a9-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d31a9-143">System-Flags</span></span>           | <span data-ttu-id="d31a9-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d31a9-144">0x00000010</span></span>                               |
| <span data-ttu-id="d31a9-145">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d31a9-145">Classes used in</span></span>        | [<span data-ttu-id="d31a9-146">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="d31a9-146">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





