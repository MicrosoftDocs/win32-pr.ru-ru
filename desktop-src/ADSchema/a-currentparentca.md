---
title: Атрибут Current-Parent-CA
description: Ссылка на центры сертификации, которые выдавали текущие сертификаты для центра сертификации.
ms.assetid: 9b851a7f-4a69-46f2-b7e2-6ee0b2d8eec1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "текущий-родительский ЦС"
- Схема AD атрибута Куррентпарентка
topic_type:
- apiref
api_name:
- Current-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26be2ccda41d998ed2b2b2c5dcddb1fcd2dcb2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989573"
---
# <a name="current-parent-ca-attribute"></a><span data-ttu-id="2e19a-105">Атрибут Current-Parent-CA</span><span class="sxs-lookup"><span data-stu-id="2e19a-105">Current-Parent-CA attribute</span></span>

<span data-ttu-id="2e19a-106">Ссылка на центры сертификации, которые выдавали текущие сертификаты для центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="2e19a-106">Reference to the certification authorities that issued the current certificates for a certification authority.</span></span>



| <span data-ttu-id="2e19a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e19a-107">Entry</span></span> | <span data-ttu-id="2e19a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2e19a-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2e19a-109">CN</span><span class="sxs-lookup"><span data-stu-id="2e19a-109">CN</span></span>                | <span data-ttu-id="2e19a-110">Текущий-родительский ЦС</span><span class="sxs-lookup"><span data-stu-id="2e19a-110">Current-Parent-CA</span></span>                       |
| <span data-ttu-id="2e19a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2e19a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2e19a-112">куррентпарентка</span><span class="sxs-lookup"><span data-stu-id="2e19a-112">currentParentCA</span></span>                         |
| <span data-ttu-id="2e19a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2e19a-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="2e19a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2e19a-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="2e19a-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2e19a-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2e19a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e19a-116">Attribute-Id</span></span>      | <span data-ttu-id="2e19a-117">1.2.840.113556.1.4.696</span><span class="sxs-lookup"><span data-stu-id="2e19a-117">1.2.840.113556.1.4.696</span></span>                  |
| <span data-ttu-id="2e19a-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2e19a-118">System-Id-Guid</span></span>    | <span data-ttu-id="2e19a-119">963d273f-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2e19a-119">963d273f-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="2e19a-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e19a-120">Syntax</span></span>            | [<span data-ttu-id="2e19a-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2e19a-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2e19a-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2e19a-122">Implementations</span></span>

-   [<span data-ttu-id="2e19a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e19a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e19a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e19a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e19a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e19a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e19a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e19a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e19a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e19a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e19a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e19a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e19a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e19a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2e19a-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e19a-130">Entry</span></span> | <span data-ttu-id="2e19a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2e19a-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2e19a-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e19a-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e19a-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e19a-134">System-Only</span></span>            | <span data-ttu-id="2e19a-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-135">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e19a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2e19a-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-137">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e19a-138">Is Indexed</span></span>             | <span data-ttu-id="2e19a-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-139">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e19a-140">In Global Catalog</span></span>      | <span data-ttu-id="2e19a-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-141">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e19a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e19a-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e19a-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2e19a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e19a-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e19a-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-146">Search-Flags</span></span>           | <span data-ttu-id="2e19a-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e19a-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="2e19a-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-148">System-Flags</span></span>           | <span data-ttu-id="2e19a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e19a-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="2e19a-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e19a-150">Classes used in</span></span>        | [<span data-ttu-id="2e19a-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="2e19a-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e19a-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e19a-152">Windows Server 2003</span></span>



| <span data-ttu-id="2e19a-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e19a-153">Entry</span></span> | <span data-ttu-id="2e19a-154">Значение</span><span class="sxs-lookup"><span data-stu-id="2e19a-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2e19a-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e19a-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e19a-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e19a-157">System-Only</span></span>            | <span data-ttu-id="2e19a-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-158">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e19a-159">Is-Single-Valued</span></span>       | <span data-ttu-id="2e19a-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-160">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e19a-161">Is Indexed</span></span>             | <span data-ttu-id="2e19a-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-162">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e19a-163">In Global Catalog</span></span>      | <span data-ttu-id="2e19a-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-164">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e19a-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e19a-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e19a-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2e19a-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e19a-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e19a-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-169">Search-Flags</span></span>           | <span data-ttu-id="2e19a-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e19a-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="2e19a-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-171">System-Flags</span></span>           | <span data-ttu-id="2e19a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e19a-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="2e19a-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e19a-173">Classes used in</span></span>        | [<span data-ttu-id="2e19a-174">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="2e19a-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e19a-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e19a-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e19a-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e19a-176">Entry</span></span> | <span data-ttu-id="2e19a-177">Значение</span><span class="sxs-lookup"><span data-stu-id="2e19a-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2e19a-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e19a-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e19a-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e19a-180">System-Only</span></span>            | <span data-ttu-id="2e19a-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-181">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e19a-182">Is-Single-Valued</span></span>       | <span data-ttu-id="2e19a-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-183">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e19a-184">Is Indexed</span></span>             | <span data-ttu-id="2e19a-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-185">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e19a-186">In Global Catalog</span></span>      | <span data-ttu-id="2e19a-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-187">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e19a-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e19a-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e19a-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2e19a-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e19a-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e19a-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-192">Search-Flags</span></span>           | <span data-ttu-id="2e19a-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e19a-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="2e19a-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-194">System-Flags</span></span>           | <span data-ttu-id="2e19a-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e19a-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="2e19a-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e19a-196">Classes used in</span></span>        | [<span data-ttu-id="2e19a-197">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="2e19a-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e19a-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e19a-198">Windows Server 2008</span></span>



| <span data-ttu-id="2e19a-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e19a-199">Entry</span></span> | <span data-ttu-id="2e19a-200">Значение</span><span class="sxs-lookup"><span data-stu-id="2e19a-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2e19a-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e19a-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e19a-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e19a-203">System-Only</span></span>            | <span data-ttu-id="2e19a-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-204">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e19a-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2e19a-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-206">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e19a-207">Is Indexed</span></span>             | <span data-ttu-id="2e19a-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-208">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e19a-209">In Global Catalog</span></span>      | <span data-ttu-id="2e19a-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-210">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e19a-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e19a-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e19a-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2e19a-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e19a-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e19a-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-215">Search-Flags</span></span>           | <span data-ttu-id="2e19a-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e19a-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="2e19a-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-217">System-Flags</span></span>           | <span data-ttu-id="2e19a-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e19a-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="2e19a-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e19a-219">Classes used in</span></span>        | [<span data-ttu-id="2e19a-220">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="2e19a-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e19a-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e19a-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e19a-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e19a-222">Entry</span></span> | <span data-ttu-id="2e19a-223">Значение</span><span class="sxs-lookup"><span data-stu-id="2e19a-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2e19a-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e19a-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e19a-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e19a-226">System-Only</span></span>            | <span data-ttu-id="2e19a-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-227">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e19a-228">Is-Single-Valued</span></span>       | <span data-ttu-id="2e19a-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-229">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e19a-230">Is Indexed</span></span>             | <span data-ttu-id="2e19a-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-231">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e19a-232">In Global Catalog</span></span>      | <span data-ttu-id="2e19a-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-233">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e19a-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e19a-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e19a-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2e19a-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e19a-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e19a-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-238">Search-Flags</span></span>           | <span data-ttu-id="2e19a-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e19a-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="2e19a-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-240">System-Flags</span></span>           | <span data-ttu-id="2e19a-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e19a-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="2e19a-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e19a-242">Classes used in</span></span>        | [<span data-ttu-id="2e19a-243">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="2e19a-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e19a-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e19a-244">Windows Server 2012</span></span>



| <span data-ttu-id="2e19a-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e19a-245">Entry</span></span> | <span data-ttu-id="2e19a-246">Значение</span><span class="sxs-lookup"><span data-stu-id="2e19a-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2e19a-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e19a-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e19a-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="2e19a-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e19a-249">System-Only</span></span>            | <span data-ttu-id="2e19a-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-250">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e19a-251">Is-Single-Valued</span></span>       | <span data-ttu-id="2e19a-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-252">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e19a-253">Is Indexed</span></span>             | <span data-ttu-id="2e19a-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-254">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e19a-255">In Global Catalog</span></span>      | <span data-ttu-id="2e19a-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e19a-256">False</span></span>                                                                  |
| <span data-ttu-id="2e19a-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e19a-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e19a-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e19a-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="2e19a-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e19a-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e19a-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="2e19a-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-261">Search-Flags</span></span>           | <span data-ttu-id="2e19a-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e19a-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="2e19a-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e19a-263">System-Flags</span></span>           | <span data-ttu-id="2e19a-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e19a-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="2e19a-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e19a-265">Classes used in</span></span>        | [<span data-ttu-id="2e19a-266">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="2e19a-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





