---
title: Репликация между сайтами-топология — атрибут отработки отказа
description: Указывает, сколько времени должно пройти с момента последнего сохранения активности для генератора межсайтовой топологии, чтобы считаться неработающим.
ms.assetid: d351dbec-d5a3-46e1-87a9-0856d19e07c6
ms.tgt_platform: multiple
keywords:
- Топология между сайтами — схема AD для атрибута отработки отказа
- Схема AD атрибута Интерситетопологифаиловер
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Failover
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4e9cad98bade7fd69178a8fce795d0b92f35b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493893"
---
# <a name="inter-site-topology-failover-attribute"></a><span data-ttu-id="a7fb7-105">Репликация между сайтами-топология — атрибут отработки отказа</span><span class="sxs-lookup"><span data-stu-id="a7fb7-105">Inter-Site-Topology-Failover attribute</span></span>

<span data-ttu-id="a7fb7-106">Указывает, сколько времени должно пройти с момента последнего сохранения активности для генератора межсайтовой топологии, чтобы считаться неработающим.</span><span class="sxs-lookup"><span data-stu-id="a7fb7-106">Indicates how much time must transpire since the last keep-alive for the inter-site topology generator to be considered dead.</span></span>



| <span data-ttu-id="a7fb7-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a7fb7-107">Entry</span></span> | <span data-ttu-id="a7fb7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fb7-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a7fb7-109">CN</span><span class="sxs-lookup"><span data-stu-id="a7fb7-109">CN</span></span>                | <span data-ttu-id="a7fb7-110">Топология между сайтами — отработка отказа</span><span class="sxs-lookup"><span data-stu-id="a7fb7-110">Inter-Site-Topology-Failover</span></span>         |
| <span data-ttu-id="a7fb7-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a7fb7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a7fb7-112">интерситетопологифаиловер</span><span class="sxs-lookup"><span data-stu-id="a7fb7-112">interSiteTopologyFailover</span></span>            |
| <span data-ttu-id="a7fb7-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a7fb7-113">Size</span></span>              | <span data-ttu-id="a7fb7-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="a7fb7-114">4 bytes</span></span>                              |
| <span data-ttu-id="a7fb7-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a7fb7-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a7fb7-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a7fb7-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a7fb7-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a7fb7-117">Attribute-Id</span></span>      | <span data-ttu-id="a7fb7-118">1.2.840.113556.1.4.1248</span><span class="sxs-lookup"><span data-stu-id="a7fb7-118">1.2.840.113556.1.4.1248</span></span>              |
| <span data-ttu-id="a7fb7-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a7fb7-119">System-Id-Guid</span></span>    | <span data-ttu-id="a7fb7-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="a7fb7-120">b7c69e60-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="a7fb7-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7fb7-121">Syntax</span></span>            | [<span data-ttu-id="a7fb7-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a7fb7-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a7fb7-123">Implementations</span></span>

-   [<span data-ttu-id="a7fb7-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a7fb7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a7fb7-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a7fb7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a7fb7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a7fb7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a7fb7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a7fb7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7fb7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a7fb7-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="a7fb7-132">Entry</span></span> | <span data-ttu-id="a7fb7-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fb7-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a7fb7-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a7fb7-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7fb7-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7fb7-136">System-Only</span></span>            | <span data-ttu-id="a7fb7-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-137">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a7fb7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a7fb7-139">True</span><span class="sxs-lookup"><span data-stu-id="a7fb7-139">True</span></span>                                                        |
| <span data-ttu-id="a7fb7-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a7fb7-140">Is Indexed</span></span>             | <span data-ttu-id="a7fb7-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-141">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a7fb7-142">In Global Catalog</span></span>      | <span data-ttu-id="a7fb7-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-143">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a7fb7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7fb7-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7fb7-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a7fb7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7fb7-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7fb7-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-148">Search-Flags</span></span>           | <span data-ttu-id="a7fb7-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7fb7-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="a7fb7-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-150">System-Flags</span></span>           | <span data-ttu-id="a7fb7-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7fb7-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="a7fb7-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a7fb7-152">Classes used in</span></span>        | [<span data-ttu-id="a7fb7-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a7fb7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7fb7-154">Windows Server 2003</span></span>



| <span data-ttu-id="a7fb7-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="a7fb7-155">Entry</span></span> | <span data-ttu-id="a7fb7-156">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fb7-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a7fb7-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a7fb7-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7fb7-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7fb7-159">System-Only</span></span>            | <span data-ttu-id="a7fb7-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-160">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a7fb7-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a7fb7-162">True</span><span class="sxs-lookup"><span data-stu-id="a7fb7-162">True</span></span>                                                        |
| <span data-ttu-id="a7fb7-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a7fb7-163">Is Indexed</span></span>             | <span data-ttu-id="a7fb7-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-164">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a7fb7-165">In Global Catalog</span></span>      | <span data-ttu-id="a7fb7-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-166">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a7fb7-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7fb7-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7fb7-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a7fb7-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7fb7-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7fb7-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-171">Search-Flags</span></span>           | <span data-ttu-id="a7fb7-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7fb7-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="a7fb7-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-173">System-Flags</span></span>           | <span data-ttu-id="a7fb7-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7fb7-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="a7fb7-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a7fb7-175">Classes used in</span></span>        | [<span data-ttu-id="a7fb7-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a7fb7-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="a7fb7-177">ADAM</span></span>



| <span data-ttu-id="a7fb7-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="a7fb7-178">Entry</span></span> | <span data-ttu-id="a7fb7-179">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fb7-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a7fb7-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a7fb7-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7fb7-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7fb7-182">System-Only</span></span>            | <span data-ttu-id="a7fb7-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-183">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a7fb7-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a7fb7-185">True</span><span class="sxs-lookup"><span data-stu-id="a7fb7-185">True</span></span>                                                        |
| <span data-ttu-id="a7fb7-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a7fb7-186">Is Indexed</span></span>             | <span data-ttu-id="a7fb7-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-187">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a7fb7-188">In Global Catalog</span></span>      | <span data-ttu-id="a7fb7-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-189">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a7fb7-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7fb7-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7fb7-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a7fb7-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7fb7-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7fb7-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-194">Search-Flags</span></span>           | <span data-ttu-id="a7fb7-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7fb7-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="a7fb7-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-196">System-Flags</span></span>           | <span data-ttu-id="a7fb7-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7fb7-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="a7fb7-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a7fb7-198">Classes used in</span></span>        | [<span data-ttu-id="a7fb7-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a7fb7-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a7fb7-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a7fb7-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="a7fb7-201">Entry</span></span> | <span data-ttu-id="a7fb7-202">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fb7-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a7fb7-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a7fb7-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7fb7-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7fb7-205">System-Only</span></span>            | <span data-ttu-id="a7fb7-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-206">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a7fb7-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a7fb7-208">True</span><span class="sxs-lookup"><span data-stu-id="a7fb7-208">True</span></span>                                                        |
| <span data-ttu-id="a7fb7-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a7fb7-209">Is Indexed</span></span>             | <span data-ttu-id="a7fb7-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-210">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a7fb7-211">In Global Catalog</span></span>      | <span data-ttu-id="a7fb7-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-212">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a7fb7-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7fb7-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7fb7-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a7fb7-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7fb7-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7fb7-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-217">Search-Flags</span></span>           | <span data-ttu-id="a7fb7-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7fb7-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="a7fb7-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-219">System-Flags</span></span>           | <span data-ttu-id="a7fb7-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7fb7-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="a7fb7-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a7fb7-221">Classes used in</span></span>        | [<span data-ttu-id="a7fb7-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a7fb7-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7fb7-223">Windows Server 2008</span></span>



| <span data-ttu-id="a7fb7-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="a7fb7-224">Entry</span></span> | <span data-ttu-id="a7fb7-225">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fb7-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a7fb7-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a7fb7-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7fb7-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7fb7-228">System-Only</span></span>            | <span data-ttu-id="a7fb7-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-229">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a7fb7-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a7fb7-231">True</span><span class="sxs-lookup"><span data-stu-id="a7fb7-231">True</span></span>                                                        |
| <span data-ttu-id="a7fb7-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a7fb7-232">Is Indexed</span></span>             | <span data-ttu-id="a7fb7-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-233">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a7fb7-234">In Global Catalog</span></span>      | <span data-ttu-id="a7fb7-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-235">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a7fb7-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7fb7-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7fb7-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a7fb7-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7fb7-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7fb7-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-240">Search-Flags</span></span>           | <span data-ttu-id="a7fb7-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7fb7-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="a7fb7-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-242">System-Flags</span></span>           | <span data-ttu-id="a7fb7-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7fb7-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="a7fb7-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a7fb7-244">Classes used in</span></span>        | [<span data-ttu-id="a7fb7-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a7fb7-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7fb7-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a7fb7-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="a7fb7-247">Entry</span></span> | <span data-ttu-id="a7fb7-248">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fb7-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a7fb7-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a7fb7-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7fb7-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7fb7-251">System-Only</span></span>            | <span data-ttu-id="a7fb7-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-252">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a7fb7-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a7fb7-254">True</span><span class="sxs-lookup"><span data-stu-id="a7fb7-254">True</span></span>                                                        |
| <span data-ttu-id="a7fb7-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a7fb7-255">Is Indexed</span></span>             | <span data-ttu-id="a7fb7-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-256">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a7fb7-257">In Global Catalog</span></span>      | <span data-ttu-id="a7fb7-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-258">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a7fb7-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7fb7-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7fb7-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a7fb7-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7fb7-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7fb7-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-263">Search-Flags</span></span>           | <span data-ttu-id="a7fb7-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7fb7-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="a7fb7-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-265">System-Flags</span></span>           | <span data-ttu-id="a7fb7-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7fb7-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="a7fb7-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a7fb7-267">Classes used in</span></span>        | [<span data-ttu-id="a7fb7-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a7fb7-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7fb7-269">Windows Server 2012</span></span>



| <span data-ttu-id="a7fb7-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="a7fb7-270">Entry</span></span> | <span data-ttu-id="a7fb7-271">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fb7-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a7fb7-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a7fb7-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a7fb7-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a7fb7-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="a7fb7-274">System-Only</span></span>            | <span data-ttu-id="a7fb7-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-275">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a7fb7-276">Is-Single-Valued</span></span>       | <span data-ttu-id="a7fb7-277">True</span><span class="sxs-lookup"><span data-stu-id="a7fb7-277">True</span></span>                                                        |
| <span data-ttu-id="a7fb7-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a7fb7-278">Is Indexed</span></span>             | <span data-ttu-id="a7fb7-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-279">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a7fb7-280">In Global Catalog</span></span>      | <span data-ttu-id="a7fb7-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="a7fb7-281">False</span></span>                                                       |
| <span data-ttu-id="a7fb7-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a7fb7-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="a7fb7-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a7fb7-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a7fb7-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a7fb7-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a7fb7-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a7fb7-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-286">Search-Flags</span></span>           | <span data-ttu-id="a7fb7-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7fb7-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="a7fb7-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a7fb7-288">System-Flags</span></span>           | <span data-ttu-id="a7fb7-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a7fb7-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="a7fb7-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a7fb7-290">Classes used in</span></span>        | [<span data-ttu-id="a7fb7-291">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="a7fb7-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





