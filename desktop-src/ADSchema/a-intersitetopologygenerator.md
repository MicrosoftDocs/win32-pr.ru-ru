---
title: Атрибут межсайтовой топологии — генератор
description: Этот атрибут будет использоваться для поддержки отработки отказа на компьютере, обозначенном как тот, который выполняет создание межсайтовой топологии с помощью средства проверки согласованности знаний на данном сайте.
ms.assetid: 077f4331-ead9-4f17-942e-d55cf253d03b
ms.tgt_platform: multiple
keywords:
- Межсайтовая топология-схема AD атрибута для генератора
- Схема AD атрибута Интерситетопологиженератор
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Generator
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7b354d05e882373715e4c49498c9daff41652
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138130"
---
# <a name="inter-site-topology-generator-attribute"></a><span data-ttu-id="36554-105">Атрибут межсайтовой топологии — генератор</span><span class="sxs-lookup"><span data-stu-id="36554-105">Inter-Site-Topology-Generator attribute</span></span>

<span data-ttu-id="36554-106">Этот атрибут будет использоваться для поддержки отработки отказа на компьютере, обозначенном как тот, который выполняет создание межсайтовой топологии с помощью средства проверки согласованности знаний на данном сайте.</span><span class="sxs-lookup"><span data-stu-id="36554-106">This attribute will be used to support failover for the computer designated as the one that runs Knowledge Consistency Checker inter-site topology generation in a given site.</span></span>



| <span data-ttu-id="36554-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="36554-107">Entry</span></span> | <span data-ttu-id="36554-108">Значение</span><span class="sxs-lookup"><span data-stu-id="36554-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="36554-109">CN</span><span class="sxs-lookup"><span data-stu-id="36554-109">CN</span></span>                | <span data-ttu-id="36554-110">Генератор межсайтовых топологий</span><span class="sxs-lookup"><span data-stu-id="36554-110">Inter-Site-Topology-Generator</span></span>           |
| <span data-ttu-id="36554-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="36554-111">Ldap-Display-Name</span></span> | <span data-ttu-id="36554-112">интерситетопологиженератор</span><span class="sxs-lookup"><span data-stu-id="36554-112">interSiteTopologyGenerator</span></span>              |
| <span data-ttu-id="36554-113">Размер</span><span class="sxs-lookup"><span data-stu-id="36554-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="36554-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="36554-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="36554-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="36554-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="36554-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36554-116">Attribute-Id</span></span>      | <span data-ttu-id="36554-117">1.2.840.113556.1.4.1246</span><span class="sxs-lookup"><span data-stu-id="36554-117">1.2.840.113556.1.4.1246</span></span>                 |
| <span data-ttu-id="36554-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="36554-118">System-Id-Guid</span></span>    | <span data-ttu-id="36554-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="36554-119">b7c69e5e-2cc7-11d2-854e-00a0c983f608</span></span>    |
| <span data-ttu-id="36554-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36554-120">Syntax</span></span>            | [<span data-ttu-id="36554-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="36554-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="36554-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="36554-122">Implementations</span></span>

-   [<span data-ttu-id="36554-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="36554-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="36554-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="36554-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="36554-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="36554-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="36554-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="36554-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="36554-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="36554-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="36554-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="36554-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="36554-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36554-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="36554-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36554-130">Windows 2000 Server</span></span>



| <span data-ttu-id="36554-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="36554-131">Entry</span></span> | <span data-ttu-id="36554-132">Значение</span><span class="sxs-lookup"><span data-stu-id="36554-132">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36554-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36554-133">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36554-134">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="36554-135">System-Only</span></span>            | <span data-ttu-id="36554-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-136">False</span></span>                                                       |
| <span data-ttu-id="36554-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36554-137">Is-Single-Valued</span></span>       | <span data-ttu-id="36554-138">True</span><span class="sxs-lookup"><span data-stu-id="36554-138">True</span></span>                                                        |
| <span data-ttu-id="36554-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36554-139">Is Indexed</span></span>             | <span data-ttu-id="36554-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-140">False</span></span>                                                       |
| <span data-ttu-id="36554-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36554-141">In Global Catalog</span></span>      | <span data-ttu-id="36554-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-142">False</span></span>                                                       |
| <span data-ttu-id="36554-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36554-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="36554-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36554-144">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36554-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36554-145">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36554-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36554-146">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36554-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-147">Search-Flags</span></span>           | <span data-ttu-id="36554-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36554-148">0x00000000</span></span>                                                  |
| <span data-ttu-id="36554-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-149">System-Flags</span></span>           | <span data-ttu-id="36554-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36554-150">0x00000010</span></span>                                                  |
| <span data-ttu-id="36554-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36554-151">Classes used in</span></span>        | [<span data-ttu-id="36554-152">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36554-152">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="36554-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36554-153">Windows Server 2003</span></span>



| <span data-ttu-id="36554-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="36554-154">Entry</span></span> | <span data-ttu-id="36554-155">Значение</span><span class="sxs-lookup"><span data-stu-id="36554-155">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36554-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36554-156">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36554-157">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="36554-158">System-Only</span></span>            | <span data-ttu-id="36554-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-159">False</span></span>                                                       |
| <span data-ttu-id="36554-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36554-160">Is-Single-Valued</span></span>       | <span data-ttu-id="36554-161">True</span><span class="sxs-lookup"><span data-stu-id="36554-161">True</span></span>                                                        |
| <span data-ttu-id="36554-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36554-162">Is Indexed</span></span>             | <span data-ttu-id="36554-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-163">False</span></span>                                                       |
| <span data-ttu-id="36554-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36554-164">In Global Catalog</span></span>      | <span data-ttu-id="36554-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-165">False</span></span>                                                       |
| <span data-ttu-id="36554-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36554-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="36554-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36554-167">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36554-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36554-168">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36554-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36554-169">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36554-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-170">Search-Flags</span></span>           | <span data-ttu-id="36554-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36554-171">0x00000000</span></span>                                                  |
| <span data-ttu-id="36554-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-172">System-Flags</span></span>           | <span data-ttu-id="36554-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36554-173">0x00000010</span></span>                                                  |
| <span data-ttu-id="36554-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36554-174">Classes used in</span></span>        | [<span data-ttu-id="36554-175">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36554-175">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="36554-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="36554-176">ADAM</span></span>



| <span data-ttu-id="36554-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="36554-177">Entry</span></span> | <span data-ttu-id="36554-178">Значение</span><span class="sxs-lookup"><span data-stu-id="36554-178">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36554-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36554-179">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36554-180">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="36554-181">System-Only</span></span>            | <span data-ttu-id="36554-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-182">False</span></span>                                                       |
| <span data-ttu-id="36554-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36554-183">Is-Single-Valued</span></span>       | <span data-ttu-id="36554-184">True</span><span class="sxs-lookup"><span data-stu-id="36554-184">True</span></span>                                                        |
| <span data-ttu-id="36554-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36554-185">Is Indexed</span></span>             | <span data-ttu-id="36554-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-186">False</span></span>                                                       |
| <span data-ttu-id="36554-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36554-187">In Global Catalog</span></span>      | <span data-ttu-id="36554-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-188">False</span></span>                                                       |
| <span data-ttu-id="36554-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36554-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="36554-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36554-190">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36554-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36554-191">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36554-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36554-192">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36554-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-193">Search-Flags</span></span>           | <span data-ttu-id="36554-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36554-194">0x00000000</span></span>                                                  |
| <span data-ttu-id="36554-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-195">System-Flags</span></span>           | <span data-ttu-id="36554-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36554-196">0x00000010</span></span>                                                  |
| <span data-ttu-id="36554-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36554-197">Classes used in</span></span>        | [<span data-ttu-id="36554-198">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36554-198">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="36554-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="36554-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="36554-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="36554-200">Entry</span></span> | <span data-ttu-id="36554-201">Значение</span><span class="sxs-lookup"><span data-stu-id="36554-201">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36554-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36554-202">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36554-203">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="36554-204">System-Only</span></span>            | <span data-ttu-id="36554-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-205">False</span></span>                                                       |
| <span data-ttu-id="36554-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36554-206">Is-Single-Valued</span></span>       | <span data-ttu-id="36554-207">True</span><span class="sxs-lookup"><span data-stu-id="36554-207">True</span></span>                                                        |
| <span data-ttu-id="36554-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36554-208">Is Indexed</span></span>             | <span data-ttu-id="36554-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-209">False</span></span>                                                       |
| <span data-ttu-id="36554-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36554-210">In Global Catalog</span></span>      | <span data-ttu-id="36554-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-211">False</span></span>                                                       |
| <span data-ttu-id="36554-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36554-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="36554-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36554-213">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36554-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36554-214">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36554-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36554-215">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36554-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-216">Search-Flags</span></span>           | <span data-ttu-id="36554-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36554-217">0x00000000</span></span>                                                  |
| <span data-ttu-id="36554-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-218">System-Flags</span></span>           | <span data-ttu-id="36554-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36554-219">0x00000010</span></span>                                                  |
| <span data-ttu-id="36554-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36554-220">Classes used in</span></span>        | [<span data-ttu-id="36554-221">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36554-221">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="36554-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36554-222">Windows Server 2008</span></span>



| <span data-ttu-id="36554-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="36554-223">Entry</span></span> | <span data-ttu-id="36554-224">Значение</span><span class="sxs-lookup"><span data-stu-id="36554-224">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36554-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36554-225">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36554-226">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="36554-227">System-Only</span></span>            | <span data-ttu-id="36554-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-228">False</span></span>                                                       |
| <span data-ttu-id="36554-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36554-229">Is-Single-Valued</span></span>       | <span data-ttu-id="36554-230">True</span><span class="sxs-lookup"><span data-stu-id="36554-230">True</span></span>                                                        |
| <span data-ttu-id="36554-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36554-231">Is Indexed</span></span>             | <span data-ttu-id="36554-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-232">False</span></span>                                                       |
| <span data-ttu-id="36554-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36554-233">In Global Catalog</span></span>      | <span data-ttu-id="36554-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-234">False</span></span>                                                       |
| <span data-ttu-id="36554-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36554-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="36554-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36554-236">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36554-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36554-237">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36554-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36554-238">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36554-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-239">Search-Flags</span></span>           | <span data-ttu-id="36554-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36554-240">0x00000000</span></span>                                                  |
| <span data-ttu-id="36554-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-241">System-Flags</span></span>           | <span data-ttu-id="36554-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36554-242">0x00000010</span></span>                                                  |
| <span data-ttu-id="36554-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36554-243">Classes used in</span></span>        | [<span data-ttu-id="36554-244">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36554-244">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="36554-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36554-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="36554-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="36554-246">Entry</span></span> | <span data-ttu-id="36554-247">Значение</span><span class="sxs-lookup"><span data-stu-id="36554-247">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36554-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36554-248">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36554-249">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="36554-250">System-Only</span></span>            | <span data-ttu-id="36554-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-251">False</span></span>                                                       |
| <span data-ttu-id="36554-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36554-252">Is-Single-Valued</span></span>       | <span data-ttu-id="36554-253">True</span><span class="sxs-lookup"><span data-stu-id="36554-253">True</span></span>                                                        |
| <span data-ttu-id="36554-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36554-254">Is Indexed</span></span>             | <span data-ttu-id="36554-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-255">False</span></span>                                                       |
| <span data-ttu-id="36554-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36554-256">In Global Catalog</span></span>      | <span data-ttu-id="36554-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-257">False</span></span>                                                       |
| <span data-ttu-id="36554-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36554-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="36554-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36554-259">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36554-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36554-260">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36554-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36554-261">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36554-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-262">Search-Flags</span></span>           | <span data-ttu-id="36554-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36554-263">0x00000000</span></span>                                                  |
| <span data-ttu-id="36554-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-264">System-Flags</span></span>           | <span data-ttu-id="36554-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36554-265">0x00000010</span></span>                                                  |
| <span data-ttu-id="36554-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36554-266">Classes used in</span></span>        | [<span data-ttu-id="36554-267">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36554-267">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="36554-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36554-268">Windows Server 2012</span></span>



| <span data-ttu-id="36554-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="36554-269">Entry</span></span> | <span data-ttu-id="36554-270">Значение</span><span class="sxs-lookup"><span data-stu-id="36554-270">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="36554-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36554-271">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36554-272">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="36554-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="36554-273">System-Only</span></span>            | <span data-ttu-id="36554-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-274">False</span></span>                                                       |
| <span data-ttu-id="36554-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36554-275">Is-Single-Valued</span></span>       | <span data-ttu-id="36554-276">True</span><span class="sxs-lookup"><span data-stu-id="36554-276">True</span></span>                                                        |
| <span data-ttu-id="36554-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36554-277">Is Indexed</span></span>             | <span data-ttu-id="36554-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-278">False</span></span>                                                       |
| <span data-ttu-id="36554-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36554-279">In Global Catalog</span></span>      | <span data-ttu-id="36554-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="36554-280">False</span></span>                                                       |
| <span data-ttu-id="36554-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36554-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="36554-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36554-282">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="36554-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36554-283">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="36554-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36554-284">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="36554-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-285">Search-Flags</span></span>           | <span data-ttu-id="36554-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36554-286">0x00000000</span></span>                                                  |
| <span data-ttu-id="36554-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36554-287">System-Flags</span></span>           | <span data-ttu-id="36554-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36554-288">0x00000010</span></span>                                                  |
| <span data-ttu-id="36554-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36554-289">Classes used in</span></span>        | [<span data-ttu-id="36554-290">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="36554-290">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





