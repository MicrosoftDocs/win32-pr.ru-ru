---
title: Атрибут межсайтовой топологии-продление
description: Этот класс указывает, как часто генератор межсайтовой топологии обновляет сообщение о состоянии активности, отправляемое на контроллеры домена, находящиеся на том же сайте.
ms.assetid: 523d8161-0678-482f-8d66-55a112995fe5
ms.tgt_platform: multiple
keywords:
- Межсайтовая топология-схема AD атрибута
- Схема AD атрибута Интерситетопологиренев
topic_type:
- apiref
api_name:
- Inter-Site-Topology-Renew
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821bd294f777fd29738ff102955cd170a42205e2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655264"
---
# <a name="inter-site-topology-renew-attribute"></a><span data-ttu-id="7c948-105">Атрибут межсайтовой топологии-продление</span><span class="sxs-lookup"><span data-stu-id="7c948-105">Inter-Site-Topology-Renew attribute</span></span>

<span data-ttu-id="7c948-106">Этот класс указывает, как часто генератор межсайтовой топологии обновляет сообщение о состоянии активности, отправляемое на контроллеры домена, находящиеся на том же сайте.</span><span class="sxs-lookup"><span data-stu-id="7c948-106">This class indicates how often the intersite topology generator updates the keep-alive message that is sent to domain controllers contained in the same site.</span></span>



| <span data-ttu-id="7c948-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c948-107">Entry</span></span> | <span data-ttu-id="7c948-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7c948-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7c948-109">CN</span><span class="sxs-lookup"><span data-stu-id="7c948-109">CN</span></span>                | <span data-ttu-id="7c948-110">Топология между сайтами — продление</span><span class="sxs-lookup"><span data-stu-id="7c948-110">Inter-Site-Topology-Renew</span></span>            |
| <span data-ttu-id="7c948-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7c948-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7c948-112">интерситетопологиренев</span><span class="sxs-lookup"><span data-stu-id="7c948-112">interSiteTopologyRenew</span></span>               |
| <span data-ttu-id="7c948-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7c948-113">Size</span></span>              | <span data-ttu-id="7c948-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="7c948-114">4 bytes</span></span>                              |
| <span data-ttu-id="7c948-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7c948-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7c948-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7c948-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7c948-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7c948-117">Attribute-Id</span></span>      | <span data-ttu-id="7c948-118">1.2.840.113556.1.4.1247</span><span class="sxs-lookup"><span data-stu-id="7c948-118">1.2.840.113556.1.4.1247</span></span>              |
| <span data-ttu-id="7c948-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7c948-119">System-Id-Guid</span></span>    | <span data-ttu-id="7c948-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="7c948-120">b7c69e5f-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="7c948-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c948-121">Syntax</span></span>            | [<span data-ttu-id="7c948-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="7c948-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7c948-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7c948-123">Implementations</span></span>

-   [<span data-ttu-id="7c948-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7c948-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7c948-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7c948-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7c948-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7c948-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7c948-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7c948-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7c948-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7c948-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7c948-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7c948-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7c948-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7c948-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7c948-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c948-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7c948-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c948-132">Entry</span></span> | <span data-ttu-id="7c948-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7c948-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7c948-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c948-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c948-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c948-136">System-Only</span></span>            | <span data-ttu-id="7c948-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-137">False</span></span>                                                       |
| <span data-ttu-id="7c948-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c948-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7c948-139">True</span><span class="sxs-lookup"><span data-stu-id="7c948-139">True</span></span>                                                        |
| <span data-ttu-id="7c948-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c948-140">Is Indexed</span></span>             | <span data-ttu-id="7c948-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-141">False</span></span>                                                       |
| <span data-ttu-id="7c948-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c948-142">In Global Catalog</span></span>      | <span data-ttu-id="7c948-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-143">False</span></span>                                                       |
| <span data-ttu-id="7c948-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c948-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c948-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c948-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7c948-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c948-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c948-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-148">Search-Flags</span></span>           | <span data-ttu-id="7c948-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c948-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="7c948-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-150">System-Flags</span></span>           | <span data-ttu-id="7c948-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c948-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="7c948-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c948-152">Classes used in</span></span>        | [<span data-ttu-id="7c948-153">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7c948-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7c948-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c948-154">Windows Server 2003</span></span>



| <span data-ttu-id="7c948-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c948-155">Entry</span></span> | <span data-ttu-id="7c948-156">Значение</span><span class="sxs-lookup"><span data-stu-id="7c948-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7c948-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c948-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c948-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c948-159">System-Only</span></span>            | <span data-ttu-id="7c948-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-160">False</span></span>                                                       |
| <span data-ttu-id="7c948-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c948-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7c948-162">True</span><span class="sxs-lookup"><span data-stu-id="7c948-162">True</span></span>                                                        |
| <span data-ttu-id="7c948-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c948-163">Is Indexed</span></span>             | <span data-ttu-id="7c948-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-164">False</span></span>                                                       |
| <span data-ttu-id="7c948-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c948-165">In Global Catalog</span></span>      | <span data-ttu-id="7c948-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-166">False</span></span>                                                       |
| <span data-ttu-id="7c948-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c948-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c948-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c948-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7c948-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c948-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c948-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-171">Search-Flags</span></span>           | <span data-ttu-id="7c948-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c948-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="7c948-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-173">System-Flags</span></span>           | <span data-ttu-id="7c948-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c948-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="7c948-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c948-175">Classes used in</span></span>        | [<span data-ttu-id="7c948-176">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7c948-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7c948-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="7c948-177">ADAM</span></span>



| <span data-ttu-id="7c948-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c948-178">Entry</span></span> | <span data-ttu-id="7c948-179">Значение</span><span class="sxs-lookup"><span data-stu-id="7c948-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7c948-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c948-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c948-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c948-182">System-Only</span></span>            | <span data-ttu-id="7c948-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-183">False</span></span>                                                       |
| <span data-ttu-id="7c948-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c948-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7c948-185">True</span><span class="sxs-lookup"><span data-stu-id="7c948-185">True</span></span>                                                        |
| <span data-ttu-id="7c948-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c948-186">Is Indexed</span></span>             | <span data-ttu-id="7c948-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-187">False</span></span>                                                       |
| <span data-ttu-id="7c948-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c948-188">In Global Catalog</span></span>      | <span data-ttu-id="7c948-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-189">False</span></span>                                                       |
| <span data-ttu-id="7c948-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c948-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c948-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c948-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7c948-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c948-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c948-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-194">Search-Flags</span></span>           | <span data-ttu-id="7c948-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c948-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="7c948-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-196">System-Flags</span></span>           | <span data-ttu-id="7c948-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c948-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="7c948-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c948-198">Classes used in</span></span>        | [<span data-ttu-id="7c948-199">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7c948-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7c948-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7c948-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7c948-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c948-201">Entry</span></span> | <span data-ttu-id="7c948-202">Значение</span><span class="sxs-lookup"><span data-stu-id="7c948-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7c948-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c948-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c948-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c948-205">System-Only</span></span>            | <span data-ttu-id="7c948-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-206">False</span></span>                                                       |
| <span data-ttu-id="7c948-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c948-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7c948-208">True</span><span class="sxs-lookup"><span data-stu-id="7c948-208">True</span></span>                                                        |
| <span data-ttu-id="7c948-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c948-209">Is Indexed</span></span>             | <span data-ttu-id="7c948-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-210">False</span></span>                                                       |
| <span data-ttu-id="7c948-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c948-211">In Global Catalog</span></span>      | <span data-ttu-id="7c948-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-212">False</span></span>                                                       |
| <span data-ttu-id="7c948-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c948-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c948-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c948-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7c948-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c948-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c948-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-217">Search-Flags</span></span>           | <span data-ttu-id="7c948-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c948-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="7c948-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-219">System-Flags</span></span>           | <span data-ttu-id="7c948-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c948-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="7c948-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c948-221">Classes used in</span></span>        | [<span data-ttu-id="7c948-222">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7c948-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7c948-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c948-223">Windows Server 2008</span></span>



| <span data-ttu-id="7c948-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c948-224">Entry</span></span> | <span data-ttu-id="7c948-225">Значение</span><span class="sxs-lookup"><span data-stu-id="7c948-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7c948-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c948-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c948-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c948-228">System-Only</span></span>            | <span data-ttu-id="7c948-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-229">False</span></span>                                                       |
| <span data-ttu-id="7c948-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c948-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7c948-231">True</span><span class="sxs-lookup"><span data-stu-id="7c948-231">True</span></span>                                                        |
| <span data-ttu-id="7c948-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c948-232">Is Indexed</span></span>             | <span data-ttu-id="7c948-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-233">False</span></span>                                                       |
| <span data-ttu-id="7c948-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c948-234">In Global Catalog</span></span>      | <span data-ttu-id="7c948-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-235">False</span></span>                                                       |
| <span data-ttu-id="7c948-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c948-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c948-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c948-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7c948-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c948-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c948-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-240">Search-Flags</span></span>           | <span data-ttu-id="7c948-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c948-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="7c948-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-242">System-Flags</span></span>           | <span data-ttu-id="7c948-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c948-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="7c948-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c948-244">Classes used in</span></span>        | [<span data-ttu-id="7c948-245">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7c948-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7c948-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c948-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7c948-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c948-247">Entry</span></span> | <span data-ttu-id="7c948-248">Значение</span><span class="sxs-lookup"><span data-stu-id="7c948-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7c948-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c948-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c948-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c948-251">System-Only</span></span>            | <span data-ttu-id="7c948-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-252">False</span></span>                                                       |
| <span data-ttu-id="7c948-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c948-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7c948-254">True</span><span class="sxs-lookup"><span data-stu-id="7c948-254">True</span></span>                                                        |
| <span data-ttu-id="7c948-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c948-255">Is Indexed</span></span>             | <span data-ttu-id="7c948-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-256">False</span></span>                                                       |
| <span data-ttu-id="7c948-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c948-257">In Global Catalog</span></span>      | <span data-ttu-id="7c948-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-258">False</span></span>                                                       |
| <span data-ttu-id="7c948-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c948-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c948-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c948-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7c948-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c948-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c948-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-263">Search-Flags</span></span>           | <span data-ttu-id="7c948-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c948-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="7c948-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-265">System-Flags</span></span>           | <span data-ttu-id="7c948-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c948-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="7c948-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c948-267">Classes used in</span></span>        | [<span data-ttu-id="7c948-268">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7c948-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7c948-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c948-269">Windows Server 2012</span></span>



| <span data-ttu-id="7c948-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="7c948-270">Entry</span></span> | <span data-ttu-id="7c948-271">Значение</span><span class="sxs-lookup"><span data-stu-id="7c948-271">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7c948-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7c948-272">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7c948-273">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="7c948-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="7c948-274">System-Only</span></span>            | <span data-ttu-id="7c948-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-275">False</span></span>                                                       |
| <span data-ttu-id="7c948-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7c948-276">Is-Single-Valued</span></span>       | <span data-ttu-id="7c948-277">True</span><span class="sxs-lookup"><span data-stu-id="7c948-277">True</span></span>                                                        |
| <span data-ttu-id="7c948-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7c948-278">Is Indexed</span></span>             | <span data-ttu-id="7c948-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-279">False</span></span>                                                       |
| <span data-ttu-id="7c948-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7c948-280">In Global Catalog</span></span>      | <span data-ttu-id="7c948-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="7c948-281">False</span></span>                                                       |
| <span data-ttu-id="7c948-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7c948-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="7c948-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7c948-283">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="7c948-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7c948-284">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7c948-285">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="7c948-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-286">Search-Flags</span></span>           | <span data-ttu-id="7c948-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7c948-287">0x00000000</span></span>                                                  |
| <span data-ttu-id="7c948-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7c948-288">System-Flags</span></span>           | <span data-ttu-id="7c948-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7c948-289">0x00000010</span></span>                                                  |
| <span data-ttu-id="7c948-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7c948-290">Classes used in</span></span>        | [<span data-ttu-id="7c948-291">**NTDS-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="7c948-291">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





