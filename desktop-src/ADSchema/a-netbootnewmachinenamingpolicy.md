---
title: нетбут-создание атрибута-компьютера-имя политики
description: Указывает схему именования, которую будут использовать новые учетные записи клиентского компьютера.
ms.assetid: e8ffc9b1-b2a2-4216-8498-85cb6c8cc7ae
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута нетбут-New-Machine-Naming-Policy
- Схема AD атрибута Нетбутневмачиненамингполици
topic_type:
- apiref
api_name:
- netboot-New-Machine-Naming-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da6cb51ced16da6510f3fb85ec80e4fa641603b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138823"
---
# <a name="netboot-new-machine-naming-policy-attribute"></a><span data-ttu-id="306e1-105">нетбут-создание атрибута-компьютера-имя политики</span><span class="sxs-lookup"><span data-stu-id="306e1-105">netboot-New-Machine-Naming-Policy attribute</span></span>

<span data-ttu-id="306e1-106">Указывает схему именования, которую будут использовать новые учетные записи клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="306e1-106">Indicates the naming scheme which new client computer accounts will use.</span></span>



| <span data-ttu-id="306e1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="306e1-107">Entry</span></span> | <span data-ttu-id="306e1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="306e1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="306e1-109">CN</span><span class="sxs-lookup"><span data-stu-id="306e1-109">CN</span></span>                | <span data-ttu-id="306e1-110">нетбут — создание политики именования компьютеров</span><span class="sxs-lookup"><span data-stu-id="306e1-110">netboot-New-Machine-Naming-Policy</span></span>           |
| <span data-ttu-id="306e1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="306e1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="306e1-112">нетбутневмачиненамингполици</span><span class="sxs-lookup"><span data-stu-id="306e1-112">netbootNewMachineNamingPolicy</span></span>               |
| <span data-ttu-id="306e1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="306e1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="306e1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="306e1-114">Update Privilege</span></span>  | <span data-ttu-id="306e1-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="306e1-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="306e1-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="306e1-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="306e1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="306e1-117">Attribute-Id</span></span>      | <span data-ttu-id="306e1-118">1.2.840.113556.1.4.855</span><span class="sxs-lookup"><span data-stu-id="306e1-118">1.2.840.113556.1.4.855</span></span>                      |
| <span data-ttu-id="306e1-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="306e1-119">System-Id-Guid</span></span>    | <span data-ttu-id="306e1-120">0738307c-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="306e1-120">0738307c-91df-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="306e1-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="306e1-121">Syntax</span></span>            | [<span data-ttu-id="306e1-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="306e1-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="306e1-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="306e1-123">Implementations</span></span>

-   [<span data-ttu-id="306e1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="306e1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="306e1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="306e1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="306e1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="306e1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="306e1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="306e1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="306e1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="306e1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="306e1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="306e1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="306e1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="306e1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="306e1-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="306e1-131">Entry</span></span> | <span data-ttu-id="306e1-132">Значение</span><span class="sxs-lookup"><span data-stu-id="306e1-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="306e1-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="306e1-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="306e1-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="306e1-135">System-Only</span></span>            | <span data-ttu-id="306e1-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-136">False</span></span>                                                      |
| <span data-ttu-id="306e1-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="306e1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="306e1-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-138">False</span></span>                                                      |
| <span data-ttu-id="306e1-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="306e1-139">Is Indexed</span></span>             | <span data-ttu-id="306e1-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-140">False</span></span>                                                      |
| <span data-ttu-id="306e1-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="306e1-141">In Global Catalog</span></span>      | <span data-ttu-id="306e1-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-142">False</span></span>                                                      |
| <span data-ttu-id="306e1-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="306e1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="306e1-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="306e1-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="306e1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="306e1-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="306e1-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-147">Search-Flags</span></span>           | <span data-ttu-id="306e1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="306e1-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="306e1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-149">System-Flags</span></span>           | <span data-ttu-id="306e1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="306e1-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="306e1-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="306e1-151">Classes used in</span></span>        | [<span data-ttu-id="306e1-152">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="306e1-152">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="306e1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="306e1-153">Windows Server 2003</span></span>



| <span data-ttu-id="306e1-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="306e1-154">Entry</span></span> | <span data-ttu-id="306e1-155">Значение</span><span class="sxs-lookup"><span data-stu-id="306e1-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="306e1-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="306e1-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="306e1-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="306e1-158">System-Only</span></span>            | <span data-ttu-id="306e1-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-159">False</span></span>                                                      |
| <span data-ttu-id="306e1-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="306e1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="306e1-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-161">False</span></span>                                                      |
| <span data-ttu-id="306e1-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="306e1-162">Is Indexed</span></span>             | <span data-ttu-id="306e1-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-163">False</span></span>                                                      |
| <span data-ttu-id="306e1-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="306e1-164">In Global Catalog</span></span>      | <span data-ttu-id="306e1-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-165">False</span></span>                                                      |
| <span data-ttu-id="306e1-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="306e1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="306e1-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="306e1-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="306e1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="306e1-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="306e1-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-170">Search-Flags</span></span>           | <span data-ttu-id="306e1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="306e1-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="306e1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-172">System-Flags</span></span>           | <span data-ttu-id="306e1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="306e1-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="306e1-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="306e1-174">Classes used in</span></span>        | [<span data-ttu-id="306e1-175">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="306e1-175">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="306e1-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="306e1-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="306e1-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="306e1-177">Entry</span></span> | <span data-ttu-id="306e1-178">Значение</span><span class="sxs-lookup"><span data-stu-id="306e1-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="306e1-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="306e1-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="306e1-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="306e1-181">System-Only</span></span>            | <span data-ttu-id="306e1-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-182">False</span></span>                                                      |
| <span data-ttu-id="306e1-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="306e1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="306e1-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-184">False</span></span>                                                      |
| <span data-ttu-id="306e1-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="306e1-185">Is Indexed</span></span>             | <span data-ttu-id="306e1-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-186">False</span></span>                                                      |
| <span data-ttu-id="306e1-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="306e1-187">In Global Catalog</span></span>      | <span data-ttu-id="306e1-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-188">False</span></span>                                                      |
| <span data-ttu-id="306e1-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="306e1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="306e1-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="306e1-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="306e1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="306e1-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="306e1-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-193">Search-Flags</span></span>           | <span data-ttu-id="306e1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="306e1-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="306e1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-195">System-Flags</span></span>           | <span data-ttu-id="306e1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="306e1-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="306e1-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="306e1-197">Classes used in</span></span>        | [<span data-ttu-id="306e1-198">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="306e1-198">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="306e1-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="306e1-199">Windows Server 2008</span></span>



| <span data-ttu-id="306e1-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="306e1-200">Entry</span></span> | <span data-ttu-id="306e1-201">Значение</span><span class="sxs-lookup"><span data-stu-id="306e1-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="306e1-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="306e1-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="306e1-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="306e1-204">System-Only</span></span>            | <span data-ttu-id="306e1-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-205">False</span></span>                                                      |
| <span data-ttu-id="306e1-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="306e1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="306e1-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-207">False</span></span>                                                      |
| <span data-ttu-id="306e1-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="306e1-208">Is Indexed</span></span>             | <span data-ttu-id="306e1-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-209">False</span></span>                                                      |
| <span data-ttu-id="306e1-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="306e1-210">In Global Catalog</span></span>      | <span data-ttu-id="306e1-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-211">False</span></span>                                                      |
| <span data-ttu-id="306e1-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="306e1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="306e1-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="306e1-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="306e1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="306e1-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="306e1-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-216">Search-Flags</span></span>           | <span data-ttu-id="306e1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="306e1-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="306e1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-218">System-Flags</span></span>           | <span data-ttu-id="306e1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="306e1-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="306e1-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="306e1-220">Classes used in</span></span>        | [<span data-ttu-id="306e1-221">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="306e1-221">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="306e1-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="306e1-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="306e1-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="306e1-223">Entry</span></span> | <span data-ttu-id="306e1-224">Значение</span><span class="sxs-lookup"><span data-stu-id="306e1-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="306e1-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="306e1-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="306e1-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="306e1-227">System-Only</span></span>            | <span data-ttu-id="306e1-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-228">False</span></span>                                                      |
| <span data-ttu-id="306e1-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="306e1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="306e1-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-230">False</span></span>                                                      |
| <span data-ttu-id="306e1-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="306e1-231">Is Indexed</span></span>             | <span data-ttu-id="306e1-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-232">False</span></span>                                                      |
| <span data-ttu-id="306e1-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="306e1-233">In Global Catalog</span></span>      | <span data-ttu-id="306e1-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-234">False</span></span>                                                      |
| <span data-ttu-id="306e1-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="306e1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="306e1-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="306e1-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="306e1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="306e1-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="306e1-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-239">Search-Flags</span></span>           | <span data-ttu-id="306e1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="306e1-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="306e1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-241">System-Flags</span></span>           | <span data-ttu-id="306e1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="306e1-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="306e1-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="306e1-243">Classes used in</span></span>        | [<span data-ttu-id="306e1-244">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="306e1-244">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="306e1-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="306e1-245">Windows Server 2012</span></span>



| <span data-ttu-id="306e1-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="306e1-246">Entry</span></span> | <span data-ttu-id="306e1-247">Значение</span><span class="sxs-lookup"><span data-stu-id="306e1-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="306e1-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="306e1-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="306e1-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="306e1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="306e1-250">System-Only</span></span>            | <span data-ttu-id="306e1-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-251">False</span></span>                                                      |
| <span data-ttu-id="306e1-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="306e1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="306e1-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-253">False</span></span>                                                      |
| <span data-ttu-id="306e1-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="306e1-254">Is Indexed</span></span>             | <span data-ttu-id="306e1-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-255">False</span></span>                                                      |
| <span data-ttu-id="306e1-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="306e1-256">In Global Catalog</span></span>      | <span data-ttu-id="306e1-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="306e1-257">False</span></span>                                                      |
| <span data-ttu-id="306e1-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="306e1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="306e1-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="306e1-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="306e1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="306e1-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="306e1-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="306e1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-262">Search-Flags</span></span>           | <span data-ttu-id="306e1-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="306e1-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="306e1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="306e1-264">System-Flags</span></span>           | <span data-ttu-id="306e1-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="306e1-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="306e1-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="306e1-266">Classes used in</span></span>        | [<span data-ttu-id="306e1-267">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="306e1-267">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





