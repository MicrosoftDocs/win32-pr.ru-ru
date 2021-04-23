---
title: ACS-с атрибутом пропускной способности и RSVP
description: Максимальная пропускная способность, которую можно зарезервировать.
ms.assetid: 18d9a5c5-e44c-49e9-a8f0-9386a7b1ff97
ms.tgt_platform: multiple
keywords:
- ACS — с атрибутом "пропускная способность", схема AD
- Схема AD атрибута Аксаллокаблерсвпбандвидс
topic_type:
- apiref
api_name:
- ACS-Allocable-RSVP-Bandwidth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6bfe98d30fb8ef959f2e75d078b3a04b325b6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103894006"
---
# <a name="acs-allocable-rsvp-bandwidth-attribute"></a><span data-ttu-id="98996-105">ACS-с атрибутом пропускной способности и RSVP</span><span class="sxs-lookup"><span data-stu-id="98996-105">ACS-Allocable-RSVP-Bandwidth attribute</span></span>

<span data-ttu-id="98996-106">Максимальная пропускная способность, которую можно зарезервировать.</span><span class="sxs-lookup"><span data-stu-id="98996-106">The maximum bandwidth that can be reserved.</span></span>



| <span data-ttu-id="98996-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="98996-107">Entry</span></span> | <span data-ttu-id="98996-108">Значение</span><span class="sxs-lookup"><span data-stu-id="98996-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="98996-109">CN</span><span class="sxs-lookup"><span data-stu-id="98996-109">CN</span></span>                | <span data-ttu-id="98996-110">ACS — с поддержкой-RSVP — пропускная способность</span><span class="sxs-lookup"><span data-stu-id="98996-110">ACS-Allocable-RSVP-Bandwidth</span></span>         |
| <span data-ttu-id="98996-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="98996-111">Ldap-Display-Name</span></span> | <span data-ttu-id="98996-112">аксаллокаблерсвпбандвидс</span><span class="sxs-lookup"><span data-stu-id="98996-112">aCSAllocableRSVPBandwidth</span></span>            |
| <span data-ttu-id="98996-113">Размер</span><span class="sxs-lookup"><span data-stu-id="98996-113">Size</span></span>              | <span data-ttu-id="98996-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="98996-114">8 bytes</span></span>                              |
| <span data-ttu-id="98996-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="98996-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="98996-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="98996-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="98996-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="98996-117">Attribute-Id</span></span>      | <span data-ttu-id="98996-118">1.2.840.113556.1.4.766</span><span class="sxs-lookup"><span data-stu-id="98996-118">1.2.840.113556.1.4.766</span></span>               |
| <span data-ttu-id="98996-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="98996-119">System-Id-Guid</span></span>    | <span data-ttu-id="98996-120">7f561283-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="98996-120">7f561283-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="98996-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98996-121">Syntax</span></span>            | [<span data-ttu-id="98996-122">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="98996-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="98996-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="98996-123">Implementations</span></span>

-   [<span data-ttu-id="98996-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="98996-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="98996-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="98996-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="98996-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="98996-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="98996-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="98996-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="98996-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="98996-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="98996-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="98996-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="98996-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98996-130">Windows 2000 Server</span></span>



| <span data-ttu-id="98996-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="98996-131">Entry</span></span> | <span data-ttu-id="98996-132">Значение</span><span class="sxs-lookup"><span data-stu-id="98996-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98996-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="98996-133">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98996-134">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="98996-135">System-Only</span></span>            | <span data-ttu-id="98996-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-136">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="98996-137">Is-Single-Valued</span></span>       | <span data-ttu-id="98996-138">True</span><span class="sxs-lookup"><span data-stu-id="98996-138">True</span></span>                                                                                                       |
| <span data-ttu-id="98996-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="98996-139">Is Indexed</span></span>             | <span data-ttu-id="98996-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-140">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="98996-141">In Global Catalog</span></span>      | <span data-ttu-id="98996-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-142">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="98996-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="98996-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="98996-144">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="98996-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98996-145">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98996-146">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-147">Search-Flags</span></span>           | <span data-ttu-id="98996-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98996-148">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="98996-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-149">System-Flags</span></span>           | <span data-ttu-id="98996-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98996-150">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="98996-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="98996-151">Classes used in</span></span>        | [<span data-ttu-id="98996-152">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="98996-152">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="98996-153">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="98996-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="98996-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="98996-154">Windows Server 2003</span></span>



| <span data-ttu-id="98996-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="98996-155">Entry</span></span> | <span data-ttu-id="98996-156">Значение</span><span class="sxs-lookup"><span data-stu-id="98996-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98996-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="98996-157">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98996-158">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="98996-159">System-Only</span></span>            | <span data-ttu-id="98996-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-160">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="98996-161">Is-Single-Valued</span></span>       | <span data-ttu-id="98996-162">True</span><span class="sxs-lookup"><span data-stu-id="98996-162">True</span></span>                                                                                                       |
| <span data-ttu-id="98996-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="98996-163">Is Indexed</span></span>             | <span data-ttu-id="98996-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-164">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="98996-165">In Global Catalog</span></span>      | <span data-ttu-id="98996-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-166">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="98996-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="98996-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="98996-168">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="98996-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98996-169">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98996-170">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-171">Search-Flags</span></span>           | <span data-ttu-id="98996-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98996-172">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="98996-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-173">System-Flags</span></span>           | <span data-ttu-id="98996-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98996-174">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="98996-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="98996-175">Classes used in</span></span>        | [<span data-ttu-id="98996-176">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="98996-176">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="98996-177">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="98996-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="98996-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="98996-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="98996-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="98996-179">Entry</span></span> | <span data-ttu-id="98996-180">Значение</span><span class="sxs-lookup"><span data-stu-id="98996-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98996-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="98996-181">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98996-182">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="98996-183">System-Only</span></span>            | <span data-ttu-id="98996-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-184">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="98996-185">Is-Single-Valued</span></span>       | <span data-ttu-id="98996-186">True</span><span class="sxs-lookup"><span data-stu-id="98996-186">True</span></span>                                                                                                       |
| <span data-ttu-id="98996-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="98996-187">Is Indexed</span></span>             | <span data-ttu-id="98996-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-188">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="98996-189">In Global Catalog</span></span>      | <span data-ttu-id="98996-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-190">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="98996-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="98996-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="98996-192">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="98996-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98996-193">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98996-194">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-195">Search-Flags</span></span>           | <span data-ttu-id="98996-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98996-196">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="98996-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-197">System-Flags</span></span>           | <span data-ttu-id="98996-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98996-198">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="98996-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="98996-199">Classes used in</span></span>        | [<span data-ttu-id="98996-200">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="98996-200">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="98996-201">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="98996-201">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="98996-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98996-202">Windows Server 2008</span></span>



| <span data-ttu-id="98996-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="98996-203">Entry</span></span> | <span data-ttu-id="98996-204">Значение</span><span class="sxs-lookup"><span data-stu-id="98996-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98996-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="98996-205">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98996-206">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="98996-207">System-Only</span></span>            | <span data-ttu-id="98996-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-208">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="98996-209">Is-Single-Valued</span></span>       | <span data-ttu-id="98996-210">True</span><span class="sxs-lookup"><span data-stu-id="98996-210">True</span></span>                                                                                                       |
| <span data-ttu-id="98996-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="98996-211">Is Indexed</span></span>             | <span data-ttu-id="98996-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-212">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="98996-213">In Global Catalog</span></span>      | <span data-ttu-id="98996-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-214">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="98996-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="98996-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="98996-216">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="98996-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98996-217">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98996-218">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-219">Search-Flags</span></span>           | <span data-ttu-id="98996-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98996-220">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="98996-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-221">System-Flags</span></span>           | <span data-ttu-id="98996-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98996-222">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="98996-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="98996-223">Classes used in</span></span>        | [<span data-ttu-id="98996-224">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="98996-224">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="98996-225">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="98996-225">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="98996-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="98996-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="98996-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="98996-227">Entry</span></span> | <span data-ttu-id="98996-228">Значение</span><span class="sxs-lookup"><span data-stu-id="98996-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98996-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="98996-229">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98996-230">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="98996-231">System-Only</span></span>            | <span data-ttu-id="98996-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-232">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="98996-233">Is-Single-Valued</span></span>       | <span data-ttu-id="98996-234">True</span><span class="sxs-lookup"><span data-stu-id="98996-234">True</span></span>                                                                                                       |
| <span data-ttu-id="98996-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="98996-235">Is Indexed</span></span>             | <span data-ttu-id="98996-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-236">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="98996-237">In Global Catalog</span></span>      | <span data-ttu-id="98996-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-238">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="98996-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="98996-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="98996-240">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="98996-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98996-241">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98996-242">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-243">Search-Flags</span></span>           | <span data-ttu-id="98996-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98996-244">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="98996-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-245">System-Flags</span></span>           | <span data-ttu-id="98996-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98996-246">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="98996-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="98996-247">Classes used in</span></span>        | [<span data-ttu-id="98996-248">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="98996-248">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="98996-249">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="98996-249">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="98996-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="98996-250">Windows Server 2012</span></span>



| <span data-ttu-id="98996-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="98996-251">Entry</span></span> | <span data-ttu-id="98996-252">Значение</span><span class="sxs-lookup"><span data-stu-id="98996-252">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98996-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="98996-253">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="98996-254">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="98996-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="98996-255">System-Only</span></span>            | <span data-ttu-id="98996-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-256">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="98996-257">Is-Single-Valued</span></span>       | <span data-ttu-id="98996-258">True</span><span class="sxs-lookup"><span data-stu-id="98996-258">True</span></span>                                                                                                       |
| <span data-ttu-id="98996-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="98996-259">Is Indexed</span></span>             | <span data-ttu-id="98996-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-260">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="98996-261">In Global Catalog</span></span>      | <span data-ttu-id="98996-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="98996-262">False</span></span>                                                                                                      |
| <span data-ttu-id="98996-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="98996-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="98996-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="98996-264">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="98996-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="98996-265">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="98996-266">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="98996-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-267">Search-Flags</span></span>           | <span data-ttu-id="98996-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="98996-268">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="98996-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="98996-269">System-Flags</span></span>           | <span data-ttu-id="98996-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="98996-270">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="98996-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="98996-271">Classes used in</span></span>        | [<span data-ttu-id="98996-272">**ACS — ограничения ресурсов**</span><span class="sxs-lookup"><span data-stu-id="98996-272">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="98996-273">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="98996-273">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





