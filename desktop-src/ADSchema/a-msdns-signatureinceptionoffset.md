---
title: атрибут MS-DNS-Signature-InAttribute-offset
description: Атрибут, который определяет время в секундах, которое должно начинаться в течение прошлых периодов действия подписи DNSSEC при подписывании зоны DNS.
ms.assetid: 2d929ec8-38ff-481e-a926-eb1251dd7a86
ms.tgt_platform: multiple
keywords:
- MS-DNS-подпись — схема AD атрибута offset
- msDN — схема AD атрибута Сигнатуреинцептионоффсет
topic_type:
- apiref
api_name:
- ms-DNS-Signature-Inception-Offset
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f81e3e278b3c37531a4e537fe45583421bce8928
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494055"
---
# <a name="ms-dns-signature-inception-offset-attribute"></a><span data-ttu-id="b52c7-105">атрибут MS-DNS-Signature-InAttribute-offset</span><span class="sxs-lookup"><span data-stu-id="b52c7-105">ms-DNS-Signature-Inception-Offset attribute</span></span>

<span data-ttu-id="b52c7-106">Атрибут, который определяет время в секундах, которое должно начинаться в течение прошлых периодов действия подписи DNSSEC при подписывании зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="b52c7-106">An attribute that defines in seconds how far in the past DNSSEC signature validity periods should begin when signing the DNS zone.</span></span>



| <span data-ttu-id="b52c7-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b52c7-107">Entry</span></span> | <span data-ttu-id="b52c7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b52c7-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b52c7-109">CN</span><span class="sxs-lookup"><span data-stu-id="b52c7-109">CN</span></span>                | <span data-ttu-id="b52c7-110">MS-DNS-"начало подписи"-смещение</span><span class="sxs-lookup"><span data-stu-id="b52c7-110">ms-DNS-Signature-Inception-Offset</span></span>    |
| <span data-ttu-id="b52c7-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b52c7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b52c7-112">msDN — Сигнатуреинцептионоффсет</span><span class="sxs-lookup"><span data-stu-id="b52c7-112">msDNS-SignatureInceptionOffset</span></span>       |
| <span data-ttu-id="b52c7-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b52c7-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="b52c7-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b52c7-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b52c7-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b52c7-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b52c7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b52c7-116">Attribute-Id</span></span>      | <span data-ttu-id="b52c7-117">1.2.840.113556.1.4.2141</span><span class="sxs-lookup"><span data-stu-id="b52c7-117">1.2.840.113556.1.4.2141</span></span>              |
| <span data-ttu-id="b52c7-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b52c7-118">System-Id-Guid</span></span>    | <span data-ttu-id="b52c7-119">03d4c32e-e217-4a61-9699-7bbc4729a026</span><span class="sxs-lookup"><span data-stu-id="b52c7-119">03d4c32e-e217-4a61-9699-7bbc4729a026</span></span> |
| <span data-ttu-id="b52c7-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b52c7-120">Syntax</span></span>            | [<span data-ttu-id="b52c7-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="b52c7-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="b52c7-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b52c7-122">Implementations</span></span>

-   [<span data-ttu-id="b52c7-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b52c7-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="b52c7-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b52c7-124">Windows Server 2012</span></span>



| <span data-ttu-id="b52c7-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="b52c7-125">Entry</span></span> | <span data-ttu-id="b52c7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b52c7-126">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b52c7-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b52c7-127">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="b52c7-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b52c7-128">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="b52c7-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="b52c7-129">System-Only</span></span>            | <span data-ttu-id="b52c7-130">Неверно</span><span class="sxs-lookup"><span data-stu-id="b52c7-130">False</span></span>                                    |
| <span data-ttu-id="b52c7-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b52c7-131">Is-Single-Valued</span></span>       | <span data-ttu-id="b52c7-132">True</span><span class="sxs-lookup"><span data-stu-id="b52c7-132">True</span></span>                                     |
| <span data-ttu-id="b52c7-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b52c7-133">Is Indexed</span></span>             | <span data-ttu-id="b52c7-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="b52c7-134">False</span></span>                                    |
| <span data-ttu-id="b52c7-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b52c7-135">In Global Catalog</span></span>      | <span data-ttu-id="b52c7-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="b52c7-136">False</span></span>                                    |
| <span data-ttu-id="b52c7-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b52c7-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="b52c7-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b52c7-138">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b52c7-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b52c7-139">Range-Lower</span></span>            | <span data-ttu-id="b52c7-140">0</span><span class="sxs-lookup"><span data-stu-id="b52c7-140">0</span></span>                                        |
| <span data-ttu-id="b52c7-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b52c7-141">Range-Upper</span></span>            | <span data-ttu-id="b52c7-142">2592000</span><span class="sxs-lookup"><span data-stu-id="b52c7-142">2592000</span></span>                                  |
| <span data-ttu-id="b52c7-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b52c7-143">Search-Flags</span></span>           | <span data-ttu-id="b52c7-144">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b52c7-144">0x00000008</span></span>                               |
| <span data-ttu-id="b52c7-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b52c7-145">System-Flags</span></span>           | <span data-ttu-id="b52c7-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b52c7-146">0x00000010</span></span>                               |
| <span data-ttu-id="b52c7-147">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b52c7-147">Classes used in</span></span>        | [<span data-ttu-id="b52c7-148">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="b52c7-148">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





