---
title: нетбут — локально установленный атрибут ОС
description: Атрибут нетбут-локально-installed-ОС зарезервирован для внутреннего использования.
ms.assetid: fb59183b-26dd-4f51-955e-32f7a706a59c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута нетбут — локально установленная ОС
- Схема AD атрибута Нетбутлокаллинсталледосес
topic_type:
- apiref
api_name:
- netboot-Locally-Installed-OSes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff07c4e4ab605a90eb2f828443c8111fd30d009
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655336"
---
# <a name="netboot-locally-installed-oses-attribute"></a><span data-ttu-id="ac744-105">нетбут — локально установленный атрибут ОС</span><span class="sxs-lookup"><span data-stu-id="ac744-105">netboot-Locally-Installed-OSes attribute</span></span>

<span data-ttu-id="ac744-106">Атрибут **нетбут-локально-installed-ОС** зарезервирован для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="ac744-106">The **netboot-Locally-Installed-OSes** attribute is reserved for internal use.</span></span>



| <span data-ttu-id="ac744-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac744-107">Entry</span></span> | <span data-ttu-id="ac744-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ac744-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ac744-109">CN</span><span class="sxs-lookup"><span data-stu-id="ac744-109">CN</span></span>                | <span data-ttu-id="ac744-110">нетбут — локально установленные — ОС</span><span class="sxs-lookup"><span data-stu-id="ac744-110">netboot-Locally-Installed-OSes</span></span>              |
| <span data-ttu-id="ac744-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ac744-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ac744-112">нетбутлокаллинсталледосес</span><span class="sxs-lookup"><span data-stu-id="ac744-112">netbootLocallyInstalledOSes</span></span>                 |
| <span data-ttu-id="ac744-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ac744-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="ac744-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ac744-114">Update Privilege</span></span>  | <span data-ttu-id="ac744-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="ac744-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="ac744-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ac744-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ac744-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac744-117">Attribute-Id</span></span>      | <span data-ttu-id="ac744-118">1.2.840.113556.1.4.859</span><span class="sxs-lookup"><span data-stu-id="ac744-118">1.2.840.113556.1.4.859</span></span>                      |
| <span data-ttu-id="ac744-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ac744-119">System-Id-Guid</span></span>    | <span data-ttu-id="ac744-120">07383080-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ac744-120">07383080-91df-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="ac744-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac744-121">Syntax</span></span>            | [<span data-ttu-id="ac744-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="ac744-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ac744-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ac744-123">Implementations</span></span>

-   [<span data-ttu-id="ac744-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ac744-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ac744-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac744-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac744-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac744-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac744-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac744-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac744-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac744-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac744-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac744-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ac744-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac744-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ac744-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac744-131">Entry</span></span> | <span data-ttu-id="ac744-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ac744-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ac744-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac744-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac744-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac744-135">System-Only</span></span>            | <span data-ttu-id="ac744-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-136">False</span></span>                                                      |
| <span data-ttu-id="ac744-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac744-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ac744-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-138">False</span></span>                                                      |
| <span data-ttu-id="ac744-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac744-139">Is Indexed</span></span>             | <span data-ttu-id="ac744-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-140">False</span></span>                                                      |
| <span data-ttu-id="ac744-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac744-141">In Global Catalog</span></span>      | <span data-ttu-id="ac744-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-142">False</span></span>                                                      |
| <span data-ttu-id="ac744-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac744-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac744-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac744-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ac744-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac744-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac744-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-147">Search-Flags</span></span>           | <span data-ttu-id="ac744-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac744-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="ac744-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-149">System-Flags</span></span>           | <span data-ttu-id="ac744-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac744-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="ac744-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac744-151">Classes used in</span></span>        | [<span data-ttu-id="ac744-152">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="ac744-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ac744-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac744-153">Windows Server 2003</span></span>



| <span data-ttu-id="ac744-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac744-154">Entry</span></span> | <span data-ttu-id="ac744-155">Значение</span><span class="sxs-lookup"><span data-stu-id="ac744-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ac744-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac744-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac744-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac744-158">System-Only</span></span>            | <span data-ttu-id="ac744-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-159">False</span></span>                                                      |
| <span data-ttu-id="ac744-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac744-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ac744-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-161">False</span></span>                                                      |
| <span data-ttu-id="ac744-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac744-162">Is Indexed</span></span>             | <span data-ttu-id="ac744-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-163">False</span></span>                                                      |
| <span data-ttu-id="ac744-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac744-164">In Global Catalog</span></span>      | <span data-ttu-id="ac744-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-165">False</span></span>                                                      |
| <span data-ttu-id="ac744-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac744-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac744-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac744-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ac744-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac744-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac744-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-170">Search-Flags</span></span>           | <span data-ttu-id="ac744-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac744-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="ac744-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-172">System-Flags</span></span>           | <span data-ttu-id="ac744-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac744-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="ac744-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac744-174">Classes used in</span></span>        | [<span data-ttu-id="ac744-175">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="ac744-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac744-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac744-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac744-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac744-177">Entry</span></span> | <span data-ttu-id="ac744-178">Значение</span><span class="sxs-lookup"><span data-stu-id="ac744-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ac744-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac744-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac744-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac744-181">System-Only</span></span>            | <span data-ttu-id="ac744-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-182">False</span></span>                                                      |
| <span data-ttu-id="ac744-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac744-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ac744-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-184">False</span></span>                                                      |
| <span data-ttu-id="ac744-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac744-185">Is Indexed</span></span>             | <span data-ttu-id="ac744-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-186">False</span></span>                                                      |
| <span data-ttu-id="ac744-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac744-187">In Global Catalog</span></span>      | <span data-ttu-id="ac744-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-188">False</span></span>                                                      |
| <span data-ttu-id="ac744-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac744-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac744-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac744-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ac744-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac744-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac744-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-193">Search-Flags</span></span>           | <span data-ttu-id="ac744-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac744-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="ac744-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-195">System-Flags</span></span>           | <span data-ttu-id="ac744-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac744-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="ac744-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac744-197">Classes used in</span></span>        | [<span data-ttu-id="ac744-198">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="ac744-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac744-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac744-199">Windows Server 2008</span></span>



| <span data-ttu-id="ac744-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac744-200">Entry</span></span> | <span data-ttu-id="ac744-201">Значение</span><span class="sxs-lookup"><span data-stu-id="ac744-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ac744-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac744-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac744-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac744-204">System-Only</span></span>            | <span data-ttu-id="ac744-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-205">False</span></span>                                                      |
| <span data-ttu-id="ac744-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac744-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ac744-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-207">False</span></span>                                                      |
| <span data-ttu-id="ac744-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac744-208">Is Indexed</span></span>             | <span data-ttu-id="ac744-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-209">False</span></span>                                                      |
| <span data-ttu-id="ac744-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac744-210">In Global Catalog</span></span>      | <span data-ttu-id="ac744-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-211">False</span></span>                                                      |
| <span data-ttu-id="ac744-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac744-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac744-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac744-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ac744-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac744-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac744-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-216">Search-Flags</span></span>           | <span data-ttu-id="ac744-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac744-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="ac744-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-218">System-Flags</span></span>           | <span data-ttu-id="ac744-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac744-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="ac744-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac744-220">Classes used in</span></span>        | [<span data-ttu-id="ac744-221">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="ac744-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac744-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac744-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac744-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac744-223">Entry</span></span> | <span data-ttu-id="ac744-224">Значение</span><span class="sxs-lookup"><span data-stu-id="ac744-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ac744-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac744-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac744-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac744-227">System-Only</span></span>            | <span data-ttu-id="ac744-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-228">False</span></span>                                                      |
| <span data-ttu-id="ac744-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac744-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ac744-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-230">False</span></span>                                                      |
| <span data-ttu-id="ac744-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac744-231">Is Indexed</span></span>             | <span data-ttu-id="ac744-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-232">False</span></span>                                                      |
| <span data-ttu-id="ac744-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac744-233">In Global Catalog</span></span>      | <span data-ttu-id="ac744-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-234">False</span></span>                                                      |
| <span data-ttu-id="ac744-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac744-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac744-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac744-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ac744-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac744-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac744-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-239">Search-Flags</span></span>           | <span data-ttu-id="ac744-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac744-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="ac744-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-241">System-Flags</span></span>           | <span data-ttu-id="ac744-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac744-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="ac744-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac744-243">Classes used in</span></span>        | [<span data-ttu-id="ac744-244">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="ac744-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac744-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac744-245">Windows Server 2012</span></span>



| <span data-ttu-id="ac744-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="ac744-246">Entry</span></span> | <span data-ttu-id="ac744-247">Значение</span><span class="sxs-lookup"><span data-stu-id="ac744-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="ac744-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ac744-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac744-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="ac744-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac744-250">System-Only</span></span>            | <span data-ttu-id="ac744-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-251">False</span></span>                                                      |
| <span data-ttu-id="ac744-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ac744-252">Is-Single-Valued</span></span>       | <span data-ttu-id="ac744-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-253">False</span></span>                                                      |
| <span data-ttu-id="ac744-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ac744-254">Is Indexed</span></span>             | <span data-ttu-id="ac744-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-255">False</span></span>                                                      |
| <span data-ttu-id="ac744-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ac744-256">In Global Catalog</span></span>      | <span data-ttu-id="ac744-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="ac744-257">False</span></span>                                                      |
| <span data-ttu-id="ac744-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ac744-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac744-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ac744-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="ac744-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac744-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac744-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="ac744-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-262">Search-Flags</span></span>           | <span data-ttu-id="ac744-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac744-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="ac744-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac744-264">System-Flags</span></span>           | <span data-ttu-id="ac744-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac744-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="ac744-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ac744-266">Classes used in</span></span>        | [<span data-ttu-id="ac744-267">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="ac744-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





