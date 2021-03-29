---
title: нетбут — атрибут "создать-компьютер-OU"
description: Указывает, где будет создана учетная запись нового клиентского компьютера.
ms.assetid: 0e1a9145-65cc-499f-a264-c56f9028341b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута нетбут-New-Machine-OU
- Схема AD атрибута Нетбутневмачинеау
topic_type:
- apiref
api_name:
- netboot-New-Machine-OU
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a3f4a8169d91dc206f6b57cba96374903077b7f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893346"
---
# <a name="netboot-new-machine-ou-attribute"></a><span data-ttu-id="e29ed-105">нетбут — атрибут "создать-компьютер-OU"</span><span class="sxs-lookup"><span data-stu-id="e29ed-105">netboot-New-Machine-OU attribute</span></span>

<span data-ttu-id="e29ed-106">Указывает, где будет создана учетная запись нового клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="e29ed-106">Indicates where the new client computer account will be created.</span></span>



| <span data-ttu-id="e29ed-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e29ed-107">Entry</span></span> | <span data-ttu-id="e29ed-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e29ed-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="e29ed-109">CN</span><span class="sxs-lookup"><span data-stu-id="e29ed-109">CN</span></span>                | <span data-ttu-id="e29ed-110">нетбут-New-Machine-OU</span><span class="sxs-lookup"><span data-stu-id="e29ed-110">netboot-New-Machine-OU</span></span>                  |
| <span data-ttu-id="e29ed-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e29ed-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e29ed-112">нетбутневмачинеау</span><span class="sxs-lookup"><span data-stu-id="e29ed-112">netbootNewMachineOU</span></span>                     |
| <span data-ttu-id="e29ed-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e29ed-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="e29ed-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e29ed-114">Update Privilege</span></span>  | <span data-ttu-id="e29ed-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="e29ed-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="e29ed-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e29ed-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="e29ed-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e29ed-117">Attribute-Id</span></span>      | <span data-ttu-id="e29ed-118">1.2.840.113556.1.4.856</span><span class="sxs-lookup"><span data-stu-id="e29ed-118">1.2.840.113556.1.4.856</span></span>                  |
| <span data-ttu-id="e29ed-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e29ed-119">System-Id-Guid</span></span>    | <span data-ttu-id="e29ed-120">0738307d-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e29ed-120">0738307d-91df-11d1-aebc-0000f80367c1</span></span>    |
| <span data-ttu-id="e29ed-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e29ed-121">Syntax</span></span>            | [<span data-ttu-id="e29ed-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e29ed-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="e29ed-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e29ed-123">Implementations</span></span>

-   [<span data-ttu-id="e29ed-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e29ed-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e29ed-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e29ed-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e29ed-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e29ed-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e29ed-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e29ed-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e29ed-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e29ed-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e29ed-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e29ed-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e29ed-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e29ed-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e29ed-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="e29ed-131">Entry</span></span> | <span data-ttu-id="e29ed-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e29ed-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="e29ed-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e29ed-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29ed-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29ed-135">System-Only</span></span>            | <span data-ttu-id="e29ed-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-136">False</span></span>                                                      |
| <span data-ttu-id="e29ed-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e29ed-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e29ed-138">True</span><span class="sxs-lookup"><span data-stu-id="e29ed-138">True</span></span>                                                       |
| <span data-ttu-id="e29ed-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e29ed-139">Is Indexed</span></span>             | <span data-ttu-id="e29ed-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-140">False</span></span>                                                      |
| <span data-ttu-id="e29ed-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e29ed-141">In Global Catalog</span></span>      | <span data-ttu-id="e29ed-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-142">False</span></span>                                                      |
| <span data-ttu-id="e29ed-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e29ed-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29ed-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e29ed-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="e29ed-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29ed-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29ed-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-147">Search-Flags</span></span>           | <span data-ttu-id="e29ed-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29ed-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="e29ed-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-149">System-Flags</span></span>           | <span data-ttu-id="e29ed-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29ed-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="e29ed-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e29ed-151">Classes used in</span></span>        | [<span data-ttu-id="e29ed-152">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="e29ed-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e29ed-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e29ed-153">Windows Server 2003</span></span>



| <span data-ttu-id="e29ed-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="e29ed-154">Entry</span></span> | <span data-ttu-id="e29ed-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e29ed-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="e29ed-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e29ed-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29ed-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29ed-158">System-Only</span></span>            | <span data-ttu-id="e29ed-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-159">False</span></span>                                                      |
| <span data-ttu-id="e29ed-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e29ed-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e29ed-161">True</span><span class="sxs-lookup"><span data-stu-id="e29ed-161">True</span></span>                                                       |
| <span data-ttu-id="e29ed-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e29ed-162">Is Indexed</span></span>             | <span data-ttu-id="e29ed-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-163">False</span></span>                                                      |
| <span data-ttu-id="e29ed-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e29ed-164">In Global Catalog</span></span>      | <span data-ttu-id="e29ed-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-165">False</span></span>                                                      |
| <span data-ttu-id="e29ed-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e29ed-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29ed-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e29ed-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="e29ed-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29ed-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29ed-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-170">Search-Flags</span></span>           | <span data-ttu-id="e29ed-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29ed-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="e29ed-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-172">System-Flags</span></span>           | <span data-ttu-id="e29ed-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29ed-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="e29ed-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e29ed-174">Classes used in</span></span>        | [<span data-ttu-id="e29ed-175">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="e29ed-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e29ed-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e29ed-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e29ed-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="e29ed-177">Entry</span></span> | <span data-ttu-id="e29ed-178">Значение</span><span class="sxs-lookup"><span data-stu-id="e29ed-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="e29ed-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e29ed-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29ed-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29ed-181">System-Only</span></span>            | <span data-ttu-id="e29ed-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-182">False</span></span>                                                      |
| <span data-ttu-id="e29ed-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e29ed-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e29ed-184">True</span><span class="sxs-lookup"><span data-stu-id="e29ed-184">True</span></span>                                                       |
| <span data-ttu-id="e29ed-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e29ed-185">Is Indexed</span></span>             | <span data-ttu-id="e29ed-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-186">False</span></span>                                                      |
| <span data-ttu-id="e29ed-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e29ed-187">In Global Catalog</span></span>      | <span data-ttu-id="e29ed-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-188">False</span></span>                                                      |
| <span data-ttu-id="e29ed-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e29ed-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29ed-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e29ed-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="e29ed-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29ed-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29ed-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-193">Search-Flags</span></span>           | <span data-ttu-id="e29ed-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29ed-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="e29ed-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-195">System-Flags</span></span>           | <span data-ttu-id="e29ed-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29ed-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="e29ed-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e29ed-197">Classes used in</span></span>        | [<span data-ttu-id="e29ed-198">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="e29ed-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e29ed-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e29ed-199">Windows Server 2008</span></span>



| <span data-ttu-id="e29ed-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="e29ed-200">Entry</span></span> | <span data-ttu-id="e29ed-201">Значение</span><span class="sxs-lookup"><span data-stu-id="e29ed-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="e29ed-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e29ed-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29ed-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29ed-204">System-Only</span></span>            | <span data-ttu-id="e29ed-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-205">False</span></span>                                                      |
| <span data-ttu-id="e29ed-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e29ed-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e29ed-207">True</span><span class="sxs-lookup"><span data-stu-id="e29ed-207">True</span></span>                                                       |
| <span data-ttu-id="e29ed-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e29ed-208">Is Indexed</span></span>             | <span data-ttu-id="e29ed-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-209">False</span></span>                                                      |
| <span data-ttu-id="e29ed-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e29ed-210">In Global Catalog</span></span>      | <span data-ttu-id="e29ed-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-211">False</span></span>                                                      |
| <span data-ttu-id="e29ed-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e29ed-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29ed-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e29ed-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="e29ed-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29ed-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29ed-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-216">Search-Flags</span></span>           | <span data-ttu-id="e29ed-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29ed-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="e29ed-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-218">System-Flags</span></span>           | <span data-ttu-id="e29ed-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29ed-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="e29ed-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e29ed-220">Classes used in</span></span>        | [<span data-ttu-id="e29ed-221">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="e29ed-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e29ed-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e29ed-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e29ed-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="e29ed-223">Entry</span></span> | <span data-ttu-id="e29ed-224">Значение</span><span class="sxs-lookup"><span data-stu-id="e29ed-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="e29ed-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e29ed-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29ed-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29ed-227">System-Only</span></span>            | <span data-ttu-id="e29ed-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-228">False</span></span>                                                      |
| <span data-ttu-id="e29ed-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e29ed-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e29ed-230">True</span><span class="sxs-lookup"><span data-stu-id="e29ed-230">True</span></span>                                                       |
| <span data-ttu-id="e29ed-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e29ed-231">Is Indexed</span></span>             | <span data-ttu-id="e29ed-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-232">False</span></span>                                                      |
| <span data-ttu-id="e29ed-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e29ed-233">In Global Catalog</span></span>      | <span data-ttu-id="e29ed-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-234">False</span></span>                                                      |
| <span data-ttu-id="e29ed-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e29ed-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29ed-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e29ed-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="e29ed-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29ed-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29ed-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-239">Search-Flags</span></span>           | <span data-ttu-id="e29ed-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29ed-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="e29ed-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-241">System-Flags</span></span>           | <span data-ttu-id="e29ed-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29ed-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="e29ed-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e29ed-243">Classes used in</span></span>        | [<span data-ttu-id="e29ed-244">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="e29ed-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e29ed-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e29ed-245">Windows Server 2012</span></span>



| <span data-ttu-id="e29ed-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="e29ed-246">Entry</span></span> | <span data-ttu-id="e29ed-247">Значение</span><span class="sxs-lookup"><span data-stu-id="e29ed-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="e29ed-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e29ed-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29ed-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="e29ed-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29ed-250">System-Only</span></span>            | <span data-ttu-id="e29ed-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-251">False</span></span>                                                      |
| <span data-ttu-id="e29ed-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e29ed-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e29ed-253">True</span><span class="sxs-lookup"><span data-stu-id="e29ed-253">True</span></span>                                                       |
| <span data-ttu-id="e29ed-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e29ed-254">Is Indexed</span></span>             | <span data-ttu-id="e29ed-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-255">False</span></span>                                                      |
| <span data-ttu-id="e29ed-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e29ed-256">In Global Catalog</span></span>      | <span data-ttu-id="e29ed-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="e29ed-257">False</span></span>                                                      |
| <span data-ttu-id="e29ed-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e29ed-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29ed-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e29ed-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="e29ed-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29ed-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29ed-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="e29ed-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-262">Search-Flags</span></span>           | <span data-ttu-id="e29ed-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29ed-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="e29ed-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29ed-264">System-Flags</span></span>           | <span data-ttu-id="e29ed-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29ed-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="e29ed-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e29ed-266">Classes used in</span></span>        | [<span data-ttu-id="e29ed-267">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="e29ed-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





