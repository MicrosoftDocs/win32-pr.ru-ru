---
title: атрибут нетбут-Answer-Requests
description: Позволяет серверу RIS принимать любые запросы RIS.
ms.assetid: fb57762f-d7af-45ae-80f2-5dd52b5688a9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута нетбут-Answer-Requests
- Схема AD атрибута Нетбутансверрекуестс
topic_type:
- apiref
api_name:
- netboot-Answer-Requests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3552517189635da9c2ed464e286c06bb3c8d19
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655334"
---
# <a name="netboot-answer-requests-attribute"></a><span data-ttu-id="16a9a-105">атрибут нетбут-Answer-Requests</span><span class="sxs-lookup"><span data-stu-id="16a9a-105">netboot-Answer-Requests attribute</span></span>

<span data-ttu-id="16a9a-106">Позволяет серверу RIS принимать любые запросы RIS.</span><span class="sxs-lookup"><span data-stu-id="16a9a-106">Enables the RIS server to accept any RIS requests.</span></span>



| <span data-ttu-id="16a9a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="16a9a-107">Entry</span></span> | <span data-ttu-id="16a9a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="16a9a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="16a9a-109">CN</span><span class="sxs-lookup"><span data-stu-id="16a9a-109">CN</span></span>                | <span data-ttu-id="16a9a-110">нетбут — ответы — запросы</span><span class="sxs-lookup"><span data-stu-id="16a9a-110">netboot-Answer-Requests</span></span>              |
| <span data-ttu-id="16a9a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="16a9a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="16a9a-112">нетбутансверрекуестс</span><span class="sxs-lookup"><span data-stu-id="16a9a-112">netbootAnswerRequests</span></span>                |
| <span data-ttu-id="16a9a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="16a9a-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="16a9a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="16a9a-114">Update Privilege</span></span>  | <span data-ttu-id="16a9a-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="16a9a-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="16a9a-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="16a9a-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="16a9a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="16a9a-117">Attribute-Id</span></span>      | <span data-ttu-id="16a9a-118">1.2.840.113556.1.4.853</span><span class="sxs-lookup"><span data-stu-id="16a9a-118">1.2.840.113556.1.4.853</span></span>               |
| <span data-ttu-id="16a9a-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="16a9a-119">System-Id-Guid</span></span>    | <span data-ttu-id="16a9a-120">0738307a-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="16a9a-120">0738307a-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="16a9a-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16a9a-121">Syntax</span></span>            | [<span data-ttu-id="16a9a-122">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="16a9a-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="16a9a-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="16a9a-123">Implementations</span></span>

-   [<span data-ttu-id="16a9a-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="16a9a-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="16a9a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="16a9a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="16a9a-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="16a9a-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="16a9a-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="16a9a-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="16a9a-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="16a9a-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="16a9a-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="16a9a-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="16a9a-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="16a9a-130">Windows 2000 Server</span></span>



| <span data-ttu-id="16a9a-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="16a9a-131">Entry</span></span> | <span data-ttu-id="16a9a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="16a9a-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="16a9a-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16a9a-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16a9a-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="16a9a-135">System-Only</span></span>            | <span data-ttu-id="16a9a-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-136">False</span></span>                                                      |
| <span data-ttu-id="16a9a-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16a9a-137">Is-Single-Valued</span></span>       | <span data-ttu-id="16a9a-138">True</span><span class="sxs-lookup"><span data-stu-id="16a9a-138">True</span></span>                                                       |
| <span data-ttu-id="16a9a-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16a9a-139">Is Indexed</span></span>             | <span data-ttu-id="16a9a-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-140">False</span></span>                                                      |
| <span data-ttu-id="16a9a-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16a9a-141">In Global Catalog</span></span>      | <span data-ttu-id="16a9a-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-142">False</span></span>                                                      |
| <span data-ttu-id="16a9a-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16a9a-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="16a9a-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16a9a-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="16a9a-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16a9a-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16a9a-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-147">Search-Flags</span></span>           | <span data-ttu-id="16a9a-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16a9a-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="16a9a-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-149">System-Flags</span></span>           | <span data-ttu-id="16a9a-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16a9a-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="16a9a-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16a9a-151">Classes used in</span></span>        | [<span data-ttu-id="16a9a-152">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="16a9a-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="16a9a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16a9a-153">Windows Server 2003</span></span>



| <span data-ttu-id="16a9a-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="16a9a-154">Entry</span></span> | <span data-ttu-id="16a9a-155">Значение</span><span class="sxs-lookup"><span data-stu-id="16a9a-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="16a9a-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16a9a-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16a9a-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="16a9a-158">System-Only</span></span>            | <span data-ttu-id="16a9a-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-159">False</span></span>                                                      |
| <span data-ttu-id="16a9a-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16a9a-160">Is-Single-Valued</span></span>       | <span data-ttu-id="16a9a-161">True</span><span class="sxs-lookup"><span data-stu-id="16a9a-161">True</span></span>                                                       |
| <span data-ttu-id="16a9a-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16a9a-162">Is Indexed</span></span>             | <span data-ttu-id="16a9a-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-163">False</span></span>                                                      |
| <span data-ttu-id="16a9a-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16a9a-164">In Global Catalog</span></span>      | <span data-ttu-id="16a9a-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-165">False</span></span>                                                      |
| <span data-ttu-id="16a9a-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16a9a-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="16a9a-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16a9a-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="16a9a-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16a9a-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16a9a-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-170">Search-Flags</span></span>           | <span data-ttu-id="16a9a-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16a9a-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="16a9a-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-172">System-Flags</span></span>           | <span data-ttu-id="16a9a-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16a9a-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="16a9a-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16a9a-174">Classes used in</span></span>        | [<span data-ttu-id="16a9a-175">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="16a9a-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="16a9a-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="16a9a-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="16a9a-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="16a9a-177">Entry</span></span> | <span data-ttu-id="16a9a-178">Значение</span><span class="sxs-lookup"><span data-stu-id="16a9a-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="16a9a-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16a9a-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16a9a-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="16a9a-181">System-Only</span></span>            | <span data-ttu-id="16a9a-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-182">False</span></span>                                                      |
| <span data-ttu-id="16a9a-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16a9a-183">Is-Single-Valued</span></span>       | <span data-ttu-id="16a9a-184">True</span><span class="sxs-lookup"><span data-stu-id="16a9a-184">True</span></span>                                                       |
| <span data-ttu-id="16a9a-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16a9a-185">Is Indexed</span></span>             | <span data-ttu-id="16a9a-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-186">False</span></span>                                                      |
| <span data-ttu-id="16a9a-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16a9a-187">In Global Catalog</span></span>      | <span data-ttu-id="16a9a-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-188">False</span></span>                                                      |
| <span data-ttu-id="16a9a-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16a9a-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="16a9a-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16a9a-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="16a9a-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16a9a-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16a9a-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-193">Search-Flags</span></span>           | <span data-ttu-id="16a9a-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16a9a-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="16a9a-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-195">System-Flags</span></span>           | <span data-ttu-id="16a9a-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16a9a-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="16a9a-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16a9a-197">Classes used in</span></span>        | [<span data-ttu-id="16a9a-198">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="16a9a-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="16a9a-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16a9a-199">Windows Server 2008</span></span>



| <span data-ttu-id="16a9a-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="16a9a-200">Entry</span></span> | <span data-ttu-id="16a9a-201">Значение</span><span class="sxs-lookup"><span data-stu-id="16a9a-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="16a9a-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16a9a-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16a9a-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="16a9a-204">System-Only</span></span>            | <span data-ttu-id="16a9a-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-205">False</span></span>                                                      |
| <span data-ttu-id="16a9a-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16a9a-206">Is-Single-Valued</span></span>       | <span data-ttu-id="16a9a-207">True</span><span class="sxs-lookup"><span data-stu-id="16a9a-207">True</span></span>                                                       |
| <span data-ttu-id="16a9a-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16a9a-208">Is Indexed</span></span>             | <span data-ttu-id="16a9a-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-209">False</span></span>                                                      |
| <span data-ttu-id="16a9a-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16a9a-210">In Global Catalog</span></span>      | <span data-ttu-id="16a9a-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-211">False</span></span>                                                      |
| <span data-ttu-id="16a9a-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16a9a-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="16a9a-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16a9a-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="16a9a-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16a9a-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16a9a-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-216">Search-Flags</span></span>           | <span data-ttu-id="16a9a-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16a9a-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="16a9a-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-218">System-Flags</span></span>           | <span data-ttu-id="16a9a-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16a9a-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="16a9a-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16a9a-220">Classes used in</span></span>        | [<span data-ttu-id="16a9a-221">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="16a9a-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="16a9a-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16a9a-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="16a9a-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="16a9a-223">Entry</span></span> | <span data-ttu-id="16a9a-224">Значение</span><span class="sxs-lookup"><span data-stu-id="16a9a-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="16a9a-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16a9a-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16a9a-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="16a9a-227">System-Only</span></span>            | <span data-ttu-id="16a9a-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-228">False</span></span>                                                      |
| <span data-ttu-id="16a9a-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16a9a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="16a9a-230">True</span><span class="sxs-lookup"><span data-stu-id="16a9a-230">True</span></span>                                                       |
| <span data-ttu-id="16a9a-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16a9a-231">Is Indexed</span></span>             | <span data-ttu-id="16a9a-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-232">False</span></span>                                                      |
| <span data-ttu-id="16a9a-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16a9a-233">In Global Catalog</span></span>      | <span data-ttu-id="16a9a-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-234">False</span></span>                                                      |
| <span data-ttu-id="16a9a-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16a9a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="16a9a-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16a9a-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="16a9a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16a9a-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16a9a-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-239">Search-Flags</span></span>           | <span data-ttu-id="16a9a-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16a9a-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="16a9a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-241">System-Flags</span></span>           | <span data-ttu-id="16a9a-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16a9a-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="16a9a-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16a9a-243">Classes used in</span></span>        | [<span data-ttu-id="16a9a-244">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="16a9a-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="16a9a-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16a9a-245">Windows Server 2012</span></span>



| <span data-ttu-id="16a9a-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="16a9a-246">Entry</span></span> | <span data-ttu-id="16a9a-247">Значение</span><span class="sxs-lookup"><span data-stu-id="16a9a-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="16a9a-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16a9a-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16a9a-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="16a9a-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="16a9a-250">System-Only</span></span>            | <span data-ttu-id="16a9a-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-251">False</span></span>                                                      |
| <span data-ttu-id="16a9a-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16a9a-252">Is-Single-Valued</span></span>       | <span data-ttu-id="16a9a-253">True</span><span class="sxs-lookup"><span data-stu-id="16a9a-253">True</span></span>                                                       |
| <span data-ttu-id="16a9a-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16a9a-254">Is Indexed</span></span>             | <span data-ttu-id="16a9a-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-255">False</span></span>                                                      |
| <span data-ttu-id="16a9a-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16a9a-256">In Global Catalog</span></span>      | <span data-ttu-id="16a9a-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="16a9a-257">False</span></span>                                                      |
| <span data-ttu-id="16a9a-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16a9a-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="16a9a-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16a9a-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="16a9a-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16a9a-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16a9a-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="16a9a-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-262">Search-Flags</span></span>           | <span data-ttu-id="16a9a-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16a9a-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="16a9a-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16a9a-264">System-Flags</span></span>           | <span data-ttu-id="16a9a-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16a9a-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="16a9a-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16a9a-266">Classes used in</span></span>        | [<span data-ttu-id="16a9a-267">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="16a9a-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





