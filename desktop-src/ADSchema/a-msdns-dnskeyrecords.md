---
title: атрибут MS-DNS-DNSKEY-Records
description: Атрибут, содержащий набор записей DNSKEY для корня зоны DNS и записей подписи ключа подписывания корневого ключа.
ms.assetid: bc53e9fa-8ed5-46ac-a7ab-949d19aa1c66
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DNS-DNSKEY-Records
- msDN — схема AD атрибута Днскэйрекордс
topic_type:
- apiref
api_name:
- ms-DNS-DNSKEY-Records
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da8b7bfe5f55d8ad260d879f6928cf4a54bc3cc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804726"
---
# <a name="ms-dns-dnskey-records-attribute"></a><span data-ttu-id="2cb7b-105">атрибут MS-DNS-DNSKEY-Records</span><span class="sxs-lookup"><span data-stu-id="2cb7b-105">ms-DNS-DNSKEY-Records attribute</span></span>

<span data-ttu-id="2cb7b-106">Атрибут, содержащий набор записей DNSKEY для корня зоны DNS и записей подписи ключа подписывания корневого ключа.</span><span class="sxs-lookup"><span data-stu-id="2cb7b-106">An attribute that contains the DNSKEY record set for the root of the DNS zone and the root key signing key signature records.</span></span>



| <span data-ttu-id="2cb7b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2cb7b-107">Entry</span></span> | <span data-ttu-id="2cb7b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2cb7b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2cb7b-109">CN</span><span class="sxs-lookup"><span data-stu-id="2cb7b-109">CN</span></span>                | <span data-ttu-id="2cb7b-110">Записи MS-DNS-DNSKEY-</span><span class="sxs-lookup"><span data-stu-id="2cb7b-110">ms-DNS-DNSKEY-Records</span></span>                                 |
| <span data-ttu-id="2cb7b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2cb7b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2cb7b-112">msDN — Днскэйрекордс</span><span class="sxs-lookup"><span data-stu-id="2cb7b-112">msDNS-DNSKEYRecords</span></span>                                   |
| <span data-ttu-id="2cb7b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2cb7b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="2cb7b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2cb7b-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="2cb7b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2cb7b-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="2cb7b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2cb7b-116">Attribute-Id</span></span>      | <span data-ttu-id="2cb7b-117">1.2.840.113556.1.4.2145</span><span class="sxs-lookup"><span data-stu-id="2cb7b-117">1.2.840.113556.1.4.2145</span></span>                               |
| <span data-ttu-id="2cb7b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2cb7b-118">System-Id-Guid</span></span>    | <span data-ttu-id="2cb7b-119">28c458f5-602d-4ac9-a77c-b3f1be503a7e</span><span class="sxs-lookup"><span data-stu-id="2cb7b-119">28c458f5-602d-4ac9-a77c-b3f1be503a7e</span></span>                  |
| <span data-ttu-id="2cb7b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cb7b-120">Syntax</span></span>            | [<span data-ttu-id="2cb7b-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="2cb7b-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="2cb7b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2cb7b-122">Implementations</span></span>

-   [<span data-ttu-id="2cb7b-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2cb7b-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="2cb7b-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2cb7b-124">Windows Server 2012</span></span>



| <span data-ttu-id="2cb7b-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="2cb7b-125">Entry</span></span> | <span data-ttu-id="2cb7b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2cb7b-126">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2cb7b-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2cb7b-127">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2cb7b-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2cb7b-128">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2cb7b-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="2cb7b-129">System-Only</span></span>            | <span data-ttu-id="2cb7b-130">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cb7b-130">False</span></span>                                    |
| <span data-ttu-id="2cb7b-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2cb7b-131">Is-Single-Valued</span></span>       | <span data-ttu-id="2cb7b-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cb7b-132">False</span></span>                                    |
| <span data-ttu-id="2cb7b-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2cb7b-133">Is Indexed</span></span>             | <span data-ttu-id="2cb7b-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cb7b-134">False</span></span>                                    |
| <span data-ttu-id="2cb7b-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2cb7b-135">In Global Catalog</span></span>      | <span data-ttu-id="2cb7b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="2cb7b-136">False</span></span>                                    |
| <span data-ttu-id="2cb7b-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2cb7b-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="2cb7b-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2cb7b-138">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2cb7b-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2cb7b-139">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2cb7b-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2cb7b-140">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2cb7b-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb7b-141">Search-Flags</span></span>           | <span data-ttu-id="2cb7b-142">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2cb7b-142">0x00000008</span></span>                               |
| <span data-ttu-id="2cb7b-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2cb7b-143">System-Flags</span></span>           | <span data-ttu-id="2cb7b-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2cb7b-144">0x00000010</span></span>                               |
| <span data-ttu-id="2cb7b-145">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2cb7b-145">Classes used in</span></span>        | [<span data-ttu-id="2cb7b-146">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="2cb7b-146">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





