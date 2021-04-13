---
title: Атрибут Schema-Info
description: Внутреннее двоичное значение, используемое для обнаружения изменений схемы между контроллерами домена и принудительного цикла репликации NC схемы перед репликацией любого другого NC. Используется для разрешения связей при присвоении роли FSMO схемы и изменения нескольких контроллеров домена.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Schema-Info
- Схема AD атрибута schemaInfo
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca55fc8ad3f53709b3819a7333e3470a1ac35cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536167"
---
# <a name="schema-info-attribute"></a><span data-ttu-id="cf0c5-106">Атрибут Schema-Info</span><span class="sxs-lookup"><span data-stu-id="cf0c5-106">Schema-Info attribute</span></span>

<span data-ttu-id="cf0c5-107">Внутреннее двоичное значение, используемое для обнаружения изменений схемы между контроллерами домена и принудительного цикла репликации NC схемы перед репликацией любого другого NC.</span><span class="sxs-lookup"><span data-stu-id="cf0c5-107">An internal binary value used to detect schema changes between DCs and force a schema NC replication cycle before replicating any other NC.</span></span> <span data-ttu-id="cf0c5-108">Используется для разрешения связей при присвоении роли FSMO схемы и изменения нескольких контроллеров домена.</span><span class="sxs-lookup"><span data-stu-id="cf0c5-108">Used to resolve ties when the schema FSMO is seized and a change is made on more than one DC.</span></span>



| <span data-ttu-id="cf0c5-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0c5-109">Entry</span></span> | <span data-ttu-id="cf0c5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0c5-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="cf0c5-111">CN</span><span class="sxs-lookup"><span data-stu-id="cf0c5-111">CN</span></span>                | <span data-ttu-id="cf0c5-112">Schema-Info</span><span class="sxs-lookup"><span data-stu-id="cf0c5-112">Schema-Info</span></span>                                           |
| <span data-ttu-id="cf0c5-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cf0c5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cf0c5-114">schemaInfo</span><span class="sxs-lookup"><span data-stu-id="cf0c5-114">schemaInfo</span></span>                                            |
| <span data-ttu-id="cf0c5-115">Размер</span><span class="sxs-lookup"><span data-stu-id="cf0c5-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="cf0c5-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cf0c5-116">Update Privilege</span></span>  | <span data-ttu-id="cf0c5-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="cf0c5-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="cf0c5-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cf0c5-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="cf0c5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf0c5-119">Attribute-Id</span></span>      | <span data-ttu-id="cf0c5-120">1.2.840.113556.1.4.1358</span><span class="sxs-lookup"><span data-stu-id="cf0c5-120">1.2.840.113556.1.4.1358</span></span>                               |
| <span data-ttu-id="cf0c5-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cf0c5-121">System-Id-Guid</span></span>    | <span data-ttu-id="cf0c5-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="cf0c5-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span></span>                  |
| <span data-ttu-id="cf0c5-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf0c5-123">Syntax</span></span>            | [<span data-ttu-id="cf0c5-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="cf0c5-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cf0c5-125">Implementations</span></span>

-   [<span data-ttu-id="cf0c5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf0c5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf0c5-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cf0c5-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf0c5-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf0c5-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf0c5-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf0c5-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf0c5-133">Windows 2000 Server</span></span>



| <span data-ttu-id="cf0c5-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0c5-134">Entry</span></span> | <span data-ttu-id="cf0c5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0c5-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0c5-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0c5-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0c5-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0c5-138">System-Only</span></span>            | <span data-ttu-id="cf0c5-139">True</span><span class="sxs-lookup"><span data-stu-id="cf0c5-139">True</span></span>                            |
| <span data-ttu-id="cf0c5-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0c5-140">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0c5-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-141">False</span></span>                           |
| <span data-ttu-id="cf0c5-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0c5-142">Is Indexed</span></span>             | <span data-ttu-id="cf0c5-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-143">False</span></span>                           |
| <span data-ttu-id="cf0c5-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0c5-144">In Global Catalog</span></span>      | <span data-ttu-id="cf0c5-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-145">False</span></span>                           |
| <span data-ttu-id="cf0c5-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0c5-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0c5-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0c5-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0c5-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0c5-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0c5-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-150">Search-Flags</span></span>           | <span data-ttu-id="cf0c5-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0c5-151">0x00000000</span></span>                      |
| <span data-ttu-id="cf0c5-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-152">System-Flags</span></span>           | <span data-ttu-id="cf0c5-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0c5-153">0x00000010</span></span>                      |
| <span data-ttu-id="cf0c5-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0c5-154">Classes used in</span></span>        | [<span data-ttu-id="cf0c5-155">**дмд**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf0c5-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf0c5-156">Windows Server 2003</span></span>



| <span data-ttu-id="cf0c5-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0c5-157">Entry</span></span> | <span data-ttu-id="cf0c5-158">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0c5-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0c5-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0c5-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0c5-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0c5-161">System-Only</span></span>            | <span data-ttu-id="cf0c5-162">True</span><span class="sxs-lookup"><span data-stu-id="cf0c5-162">True</span></span>                            |
| <span data-ttu-id="cf0c5-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0c5-163">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0c5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-164">False</span></span>                           |
| <span data-ttu-id="cf0c5-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0c5-165">Is Indexed</span></span>             | <span data-ttu-id="cf0c5-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-166">False</span></span>                           |
| <span data-ttu-id="cf0c5-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0c5-167">In Global Catalog</span></span>      | <span data-ttu-id="cf0c5-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-168">False</span></span>                           |
| <span data-ttu-id="cf0c5-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0c5-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0c5-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0c5-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0c5-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0c5-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0c5-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-173">Search-Flags</span></span>           | <span data-ttu-id="cf0c5-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0c5-174">0x00000000</span></span>                      |
| <span data-ttu-id="cf0c5-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-175">System-Flags</span></span>           | <span data-ttu-id="cf0c5-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0c5-176">0x00000010</span></span>                      |
| <span data-ttu-id="cf0c5-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0c5-177">Classes used in</span></span>        | [<span data-ttu-id="cf0c5-178">**дмд**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-178">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cf0c5-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="cf0c5-179">ADAM</span></span>



| <span data-ttu-id="cf0c5-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0c5-180">Entry</span></span> | <span data-ttu-id="cf0c5-181">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0c5-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0c5-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0c5-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0c5-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0c5-184">System-Only</span></span>            | <span data-ttu-id="cf0c5-185">True</span><span class="sxs-lookup"><span data-stu-id="cf0c5-185">True</span></span>                            |
| <span data-ttu-id="cf0c5-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0c5-186">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0c5-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-187">False</span></span>                           |
| <span data-ttu-id="cf0c5-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0c5-188">Is Indexed</span></span>             | <span data-ttu-id="cf0c5-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-189">False</span></span>                           |
| <span data-ttu-id="cf0c5-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0c5-190">In Global Catalog</span></span>      | <span data-ttu-id="cf0c5-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-191">False</span></span>                           |
| <span data-ttu-id="cf0c5-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0c5-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0c5-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0c5-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0c5-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0c5-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0c5-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-196">Search-Flags</span></span>           | <span data-ttu-id="cf0c5-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0c5-197">0x00000000</span></span>                      |
| <span data-ttu-id="cf0c5-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-198">System-Flags</span></span>           | <span data-ttu-id="cf0c5-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0c5-199">0x00000010</span></span>                      |
| <span data-ttu-id="cf0c5-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0c5-200">Classes used in</span></span>        | [<span data-ttu-id="cf0c5-201">**дмд**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-201">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf0c5-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf0c5-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf0c5-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0c5-203">Entry</span></span> | <span data-ttu-id="cf0c5-204">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0c5-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0c5-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0c5-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0c5-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0c5-207">System-Only</span></span>            | <span data-ttu-id="cf0c5-208">True</span><span class="sxs-lookup"><span data-stu-id="cf0c5-208">True</span></span>                            |
| <span data-ttu-id="cf0c5-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0c5-209">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0c5-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-210">False</span></span>                           |
| <span data-ttu-id="cf0c5-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0c5-211">Is Indexed</span></span>             | <span data-ttu-id="cf0c5-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-212">False</span></span>                           |
| <span data-ttu-id="cf0c5-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0c5-213">In Global Catalog</span></span>      | <span data-ttu-id="cf0c5-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-214">False</span></span>                           |
| <span data-ttu-id="cf0c5-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0c5-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0c5-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0c5-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0c5-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0c5-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0c5-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-219">Search-Flags</span></span>           | <span data-ttu-id="cf0c5-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0c5-220">0x00000000</span></span>                      |
| <span data-ttu-id="cf0c5-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-221">System-Flags</span></span>           | <span data-ttu-id="cf0c5-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0c5-222">0x00000010</span></span>                      |
| <span data-ttu-id="cf0c5-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0c5-223">Classes used in</span></span>        | [<span data-ttu-id="cf0c5-224">**дмд**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-224">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf0c5-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf0c5-225">Windows Server 2008</span></span>



| <span data-ttu-id="cf0c5-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0c5-226">Entry</span></span> | <span data-ttu-id="cf0c5-227">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0c5-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0c5-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0c5-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0c5-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0c5-230">System-Only</span></span>            | <span data-ttu-id="cf0c5-231">True</span><span class="sxs-lookup"><span data-stu-id="cf0c5-231">True</span></span>                            |
| <span data-ttu-id="cf0c5-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0c5-232">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0c5-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-233">False</span></span>                           |
| <span data-ttu-id="cf0c5-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0c5-234">Is Indexed</span></span>             | <span data-ttu-id="cf0c5-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-235">False</span></span>                           |
| <span data-ttu-id="cf0c5-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0c5-236">In Global Catalog</span></span>      | <span data-ttu-id="cf0c5-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-237">False</span></span>                           |
| <span data-ttu-id="cf0c5-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0c5-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0c5-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0c5-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0c5-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0c5-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0c5-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-242">Search-Flags</span></span>           | <span data-ttu-id="cf0c5-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0c5-243">0x00000000</span></span>                      |
| <span data-ttu-id="cf0c5-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-244">System-Flags</span></span>           | <span data-ttu-id="cf0c5-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0c5-245">0x00000010</span></span>                      |
| <span data-ttu-id="cf0c5-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0c5-246">Classes used in</span></span>        | [<span data-ttu-id="cf0c5-247">**дмд**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-247">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf0c5-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf0c5-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf0c5-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0c5-249">Entry</span></span> | <span data-ttu-id="cf0c5-250">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0c5-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0c5-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0c5-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0c5-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0c5-253">System-Only</span></span>            | <span data-ttu-id="cf0c5-254">True</span><span class="sxs-lookup"><span data-stu-id="cf0c5-254">True</span></span>                            |
| <span data-ttu-id="cf0c5-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0c5-255">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0c5-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-256">False</span></span>                           |
| <span data-ttu-id="cf0c5-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0c5-257">Is Indexed</span></span>             | <span data-ttu-id="cf0c5-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-258">False</span></span>                           |
| <span data-ttu-id="cf0c5-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0c5-259">In Global Catalog</span></span>      | <span data-ttu-id="cf0c5-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-260">False</span></span>                           |
| <span data-ttu-id="cf0c5-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0c5-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0c5-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0c5-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0c5-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0c5-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0c5-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-265">Search-Flags</span></span>           | <span data-ttu-id="cf0c5-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0c5-266">0x00000000</span></span>                      |
| <span data-ttu-id="cf0c5-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-267">System-Flags</span></span>           | <span data-ttu-id="cf0c5-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0c5-268">0x00000010</span></span>                      |
| <span data-ttu-id="cf0c5-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0c5-269">Classes used in</span></span>        | [<span data-ttu-id="cf0c5-270">**дмд**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-270">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf0c5-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf0c5-271">Windows Server 2012</span></span>



| <span data-ttu-id="cf0c5-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf0c5-272">Entry</span></span> | <span data-ttu-id="cf0c5-273">Значение</span><span class="sxs-lookup"><span data-stu-id="cf0c5-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="cf0c5-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf0c5-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf0c5-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="cf0c5-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf0c5-276">System-Only</span></span>            | <span data-ttu-id="cf0c5-277">True</span><span class="sxs-lookup"><span data-stu-id="cf0c5-277">True</span></span>                            |
| <span data-ttu-id="cf0c5-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf0c5-278">Is-Single-Valued</span></span>       | <span data-ttu-id="cf0c5-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-279">False</span></span>                           |
| <span data-ttu-id="cf0c5-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf0c5-280">Is Indexed</span></span>             | <span data-ttu-id="cf0c5-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-281">False</span></span>                           |
| <span data-ttu-id="cf0c5-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf0c5-282">In Global Catalog</span></span>      | <span data-ttu-id="cf0c5-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf0c5-283">False</span></span>                           |
| <span data-ttu-id="cf0c5-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf0c5-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf0c5-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf0c5-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="cf0c5-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf0c5-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf0c5-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="cf0c5-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-288">Search-Flags</span></span>           | <span data-ttu-id="cf0c5-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf0c5-289">0x00000000</span></span>                      |
| <span data-ttu-id="cf0c5-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf0c5-290">System-Flags</span></span>           | <span data-ttu-id="cf0c5-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf0c5-291">0x00000010</span></span>                      |
| <span data-ttu-id="cf0c5-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf0c5-292">Classes used in</span></span>        | [<span data-ttu-id="cf0c5-293">**дмд**</span><span class="sxs-lookup"><span data-stu-id="cf0c5-293">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





