---
title: С прекращением использования-REPL-DSA-сигнатуры
description: Отслеживает удостоверения предыдущей репликации DS для данного контроллера домена.
ms.assetid: 82e8b222-5635-41ad-b2ab-386c9e6aa280
ms.tgt_platform: multiple
keywords:
- С прекращением использования-REPL-DSA-схема AD атрибутов сигнатур
- Схема AD атрибута Ретиредреплдсасигнатурес
topic_type:
- apiref
api_name:
- Retired-Repl-DSA-Signatures
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9a4cb4030a8d3aa24244bc2e7a2702e83686fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416305"
---
# <a name="retired-repl-dsa-signatures-attribute"></a><span data-ttu-id="c43bd-105">С прекращением использования-REPL-DSA-сигнатуры</span><span class="sxs-lookup"><span data-stu-id="c43bd-105">Retired-Repl-DSA-Signatures attribute</span></span>

<span data-ttu-id="c43bd-106">Отслеживает удостоверения предыдущей репликации DS для данного контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="c43bd-106">Tracks the past DS replication identities of a given DC.</span></span>



| <span data-ttu-id="c43bd-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c43bd-107">Entry</span></span> | <span data-ttu-id="c43bd-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c43bd-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c43bd-109">CN</span><span class="sxs-lookup"><span data-stu-id="c43bd-109">CN</span></span>                | <span data-ttu-id="c43bd-110">Отменено-REPL-DSA-Signatures</span><span class="sxs-lookup"><span data-stu-id="c43bd-110">Retired-Repl-DSA-Signatures</span></span>                                                         |
| <span data-ttu-id="c43bd-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c43bd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c43bd-112">ретиредреплдсасигнатурес</span><span class="sxs-lookup"><span data-stu-id="c43bd-112">retiredReplDSASignatures</span></span>                                                            |
| <span data-ttu-id="c43bd-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c43bd-113">Size</span></span>              | <span data-ttu-id="c43bd-114">Длина пропорциональна количеству восстановлений контроллера домена из резервной копии.</span><span class="sxs-lookup"><span data-stu-id="c43bd-114">Length is proportional to the number of times the DC has been restored from backup.</span></span> |
| <span data-ttu-id="c43bd-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c43bd-115">Update Privilege</span></span>  | <span data-ttu-id="c43bd-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="c43bd-116">This value is set by the system.</span></span>                                                    |
| <span data-ttu-id="c43bd-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c43bd-117">Update Frequency</span></span>  | \-                                                                                  |
| <span data-ttu-id="c43bd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c43bd-118">Attribute-Id</span></span>      | <span data-ttu-id="c43bd-119">1.2.840.113556.1.4.673</span><span class="sxs-lookup"><span data-stu-id="c43bd-119">1.2.840.113556.1.4.673</span></span>                                                              |
| <span data-ttu-id="c43bd-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c43bd-120">System-Id-Guid</span></span>    | <span data-ttu-id="c43bd-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c43bd-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span></span>                                                |
| <span data-ttu-id="c43bd-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c43bd-122">Syntax</span></span>            | [<span data-ttu-id="c43bd-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="c43bd-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                               |



## <a name="implementations"></a><span data-ttu-id="c43bd-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c43bd-124">Implementations</span></span>

-   [<span data-ttu-id="c43bd-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c43bd-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c43bd-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c43bd-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c43bd-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c43bd-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c43bd-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c43bd-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c43bd-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c43bd-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c43bd-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c43bd-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c43bd-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c43bd-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c43bd-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c43bd-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c43bd-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="c43bd-133">Entry</span></span> | <span data-ttu-id="c43bd-134">Значение</span><span class="sxs-lookup"><span data-stu-id="c43bd-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c43bd-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c43bd-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43bd-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43bd-137">System-Only</span></span>            | <span data-ttu-id="c43bd-138">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-138">True</span></span>                                     |
| <span data-ttu-id="c43bd-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c43bd-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c43bd-140">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-140">True</span></span>                                     |
| <span data-ttu-id="c43bd-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c43bd-141">Is Indexed</span></span>             | <span data-ttu-id="c43bd-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-142">False</span></span>                                    |
| <span data-ttu-id="c43bd-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c43bd-143">In Global Catalog</span></span>      | <span data-ttu-id="c43bd-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-144">False</span></span>                                    |
| <span data-ttu-id="c43bd-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c43bd-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43bd-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c43bd-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c43bd-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43bd-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43bd-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-149">Search-Flags</span></span>           | <span data-ttu-id="c43bd-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c43bd-150">0x00000000</span></span>                               |
| <span data-ttu-id="c43bd-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-151">System-Flags</span></span>           | <span data-ttu-id="c43bd-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43bd-152">0x00000010</span></span>                               |
| <span data-ttu-id="c43bd-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c43bd-153">Classes used in</span></span>        | [<span data-ttu-id="c43bd-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c43bd-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c43bd-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c43bd-155">Windows Server 2003</span></span>



| <span data-ttu-id="c43bd-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="c43bd-156">Entry</span></span> | <span data-ttu-id="c43bd-157">Значение</span><span class="sxs-lookup"><span data-stu-id="c43bd-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c43bd-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c43bd-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43bd-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43bd-160">System-Only</span></span>            | <span data-ttu-id="c43bd-161">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-161">True</span></span>                                     |
| <span data-ttu-id="c43bd-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c43bd-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c43bd-163">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-163">True</span></span>                                     |
| <span data-ttu-id="c43bd-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c43bd-164">Is Indexed</span></span>             | <span data-ttu-id="c43bd-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-165">False</span></span>                                    |
| <span data-ttu-id="c43bd-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c43bd-166">In Global Catalog</span></span>      | <span data-ttu-id="c43bd-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-167">False</span></span>                                    |
| <span data-ttu-id="c43bd-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c43bd-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43bd-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c43bd-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c43bd-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43bd-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43bd-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-172">Search-Flags</span></span>           | <span data-ttu-id="c43bd-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c43bd-173">0x00000000</span></span>                               |
| <span data-ttu-id="c43bd-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-174">System-Flags</span></span>           | <span data-ttu-id="c43bd-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43bd-175">0x00000010</span></span>                               |
| <span data-ttu-id="c43bd-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c43bd-176">Classes used in</span></span>        | [<span data-ttu-id="c43bd-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c43bd-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c43bd-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="c43bd-178">ADAM</span></span>



| <span data-ttu-id="c43bd-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="c43bd-179">Entry</span></span> | <span data-ttu-id="c43bd-180">Значение</span><span class="sxs-lookup"><span data-stu-id="c43bd-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c43bd-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c43bd-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43bd-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43bd-183">System-Only</span></span>            | <span data-ttu-id="c43bd-184">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-184">True</span></span>                                     |
| <span data-ttu-id="c43bd-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c43bd-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c43bd-186">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-186">True</span></span>                                     |
| <span data-ttu-id="c43bd-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c43bd-187">Is Indexed</span></span>             | <span data-ttu-id="c43bd-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-188">False</span></span>                                    |
| <span data-ttu-id="c43bd-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c43bd-189">In Global Catalog</span></span>      | <span data-ttu-id="c43bd-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-190">False</span></span>                                    |
| <span data-ttu-id="c43bd-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c43bd-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43bd-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c43bd-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c43bd-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43bd-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43bd-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-195">Search-Flags</span></span>           | <span data-ttu-id="c43bd-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c43bd-196">0x00000000</span></span>                               |
| <span data-ttu-id="c43bd-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-197">System-Flags</span></span>           | <span data-ttu-id="c43bd-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43bd-198">0x00000010</span></span>                               |
| <span data-ttu-id="c43bd-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c43bd-199">Classes used in</span></span>        | [<span data-ttu-id="c43bd-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c43bd-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c43bd-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c43bd-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c43bd-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="c43bd-202">Entry</span></span> | <span data-ttu-id="c43bd-203">Значение</span><span class="sxs-lookup"><span data-stu-id="c43bd-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c43bd-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c43bd-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43bd-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43bd-206">System-Only</span></span>            | <span data-ttu-id="c43bd-207">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-207">True</span></span>                                     |
| <span data-ttu-id="c43bd-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c43bd-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c43bd-209">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-209">True</span></span>                                     |
| <span data-ttu-id="c43bd-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c43bd-210">Is Indexed</span></span>             | <span data-ttu-id="c43bd-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-211">False</span></span>                                    |
| <span data-ttu-id="c43bd-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c43bd-212">In Global Catalog</span></span>      | <span data-ttu-id="c43bd-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-213">False</span></span>                                    |
| <span data-ttu-id="c43bd-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c43bd-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43bd-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c43bd-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c43bd-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43bd-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43bd-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-218">Search-Flags</span></span>           | <span data-ttu-id="c43bd-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c43bd-219">0x00000000</span></span>                               |
| <span data-ttu-id="c43bd-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-220">System-Flags</span></span>           | <span data-ttu-id="c43bd-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43bd-221">0x00000010</span></span>                               |
| <span data-ttu-id="c43bd-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c43bd-222">Classes used in</span></span>        | [<span data-ttu-id="c43bd-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c43bd-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c43bd-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c43bd-224">Windows Server 2008</span></span>



| <span data-ttu-id="c43bd-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="c43bd-225">Entry</span></span> | <span data-ttu-id="c43bd-226">Значение</span><span class="sxs-lookup"><span data-stu-id="c43bd-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c43bd-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c43bd-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43bd-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43bd-229">System-Only</span></span>            | <span data-ttu-id="c43bd-230">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-230">True</span></span>                                     |
| <span data-ttu-id="c43bd-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c43bd-231">Is-Single-Valued</span></span>       | <span data-ttu-id="c43bd-232">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-232">True</span></span>                                     |
| <span data-ttu-id="c43bd-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c43bd-233">Is Indexed</span></span>             | <span data-ttu-id="c43bd-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-234">False</span></span>                                    |
| <span data-ttu-id="c43bd-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c43bd-235">In Global Catalog</span></span>      | <span data-ttu-id="c43bd-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-236">False</span></span>                                    |
| <span data-ttu-id="c43bd-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c43bd-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43bd-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c43bd-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c43bd-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43bd-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43bd-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-241">Search-Flags</span></span>           | <span data-ttu-id="c43bd-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c43bd-242">0x00000000</span></span>                               |
| <span data-ttu-id="c43bd-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-243">System-Flags</span></span>           | <span data-ttu-id="c43bd-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43bd-244">0x00000010</span></span>                               |
| <span data-ttu-id="c43bd-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c43bd-245">Classes used in</span></span>        | [<span data-ttu-id="c43bd-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c43bd-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c43bd-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c43bd-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c43bd-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="c43bd-248">Entry</span></span> | <span data-ttu-id="c43bd-249">Значение</span><span class="sxs-lookup"><span data-stu-id="c43bd-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c43bd-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c43bd-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43bd-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43bd-252">System-Only</span></span>            | <span data-ttu-id="c43bd-253">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-253">True</span></span>                                     |
| <span data-ttu-id="c43bd-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c43bd-254">Is-Single-Valued</span></span>       | <span data-ttu-id="c43bd-255">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-255">True</span></span>                                     |
| <span data-ttu-id="c43bd-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c43bd-256">Is Indexed</span></span>             | <span data-ttu-id="c43bd-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-257">False</span></span>                                    |
| <span data-ttu-id="c43bd-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c43bd-258">In Global Catalog</span></span>      | <span data-ttu-id="c43bd-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-259">False</span></span>                                    |
| <span data-ttu-id="c43bd-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c43bd-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43bd-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c43bd-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c43bd-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43bd-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43bd-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-264">Search-Flags</span></span>           | <span data-ttu-id="c43bd-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c43bd-265">0x00000000</span></span>                               |
| <span data-ttu-id="c43bd-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-266">System-Flags</span></span>           | <span data-ttu-id="c43bd-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43bd-267">0x00000010</span></span>                               |
| <span data-ttu-id="c43bd-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c43bd-268">Classes used in</span></span>        | [<span data-ttu-id="c43bd-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c43bd-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c43bd-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c43bd-270">Windows Server 2012</span></span>



| <span data-ttu-id="c43bd-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="c43bd-271">Entry</span></span> | <span data-ttu-id="c43bd-272">Значение</span><span class="sxs-lookup"><span data-stu-id="c43bd-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="c43bd-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c43bd-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c43bd-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="c43bd-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="c43bd-275">System-Only</span></span>            | <span data-ttu-id="c43bd-276">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-276">True</span></span>                                     |
| <span data-ttu-id="c43bd-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c43bd-277">Is-Single-Valued</span></span>       | <span data-ttu-id="c43bd-278">True</span><span class="sxs-lookup"><span data-stu-id="c43bd-278">True</span></span>                                     |
| <span data-ttu-id="c43bd-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c43bd-279">Is Indexed</span></span>             | <span data-ttu-id="c43bd-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-280">False</span></span>                                    |
| <span data-ttu-id="c43bd-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c43bd-281">In Global Catalog</span></span>      | <span data-ttu-id="c43bd-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="c43bd-282">False</span></span>                                    |
| <span data-ttu-id="c43bd-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c43bd-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="c43bd-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c43bd-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="c43bd-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c43bd-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c43bd-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="c43bd-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-287">Search-Flags</span></span>           | <span data-ttu-id="c43bd-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c43bd-288">0x00000000</span></span>                               |
| <span data-ttu-id="c43bd-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c43bd-289">System-Flags</span></span>           | <span data-ttu-id="c43bd-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c43bd-290">0x00000010</span></span>                               |
| <span data-ttu-id="c43bd-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c43bd-291">Classes used in</span></span>        | [<span data-ttu-id="c43bd-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c43bd-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





