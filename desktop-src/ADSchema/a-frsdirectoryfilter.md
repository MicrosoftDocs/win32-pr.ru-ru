---
title: Атрибут фильтра FRS-Directory
description: Список каталогов, исключаемых из репликации файлов, например TEMP или obj.
ms.assetid: 3ce37a96-0cb2-46bf-aad1-80fc1304855d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов фильтра FRS-Directory
- Схема AD атрибута Фрсдиректорифилтер
topic_type:
- apiref
api_name:
- FRS-Directory-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b547cd431d7f51af698a137b7edd7dd299a3ec2f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493524"
---
# <a name="frs-directory-filter-attribute"></a><span data-ttu-id="6b99b-105">Атрибут фильтра FRS-Directory</span><span class="sxs-lookup"><span data-stu-id="6b99b-105">FRS-Directory-Filter attribute</span></span>

<span data-ttu-id="6b99b-106">Список каталогов, исключаемых из репликации файлов, например TEMP или obj.</span><span class="sxs-lookup"><span data-stu-id="6b99b-106">The list of directories excluded from file replication, for example, temp, or obj.</span></span>



| <span data-ttu-id="6b99b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6b99b-107">Entry</span></span> | <span data-ttu-id="6b99b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6b99b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6b99b-109">CN</span><span class="sxs-lookup"><span data-stu-id="6b99b-109">CN</span></span>                | <span data-ttu-id="6b99b-110">FRS-каталог — фильтр</span><span class="sxs-lookup"><span data-stu-id="6b99b-110">FRS-Directory-Filter</span></span>                        |
| <span data-ttu-id="6b99b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6b99b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6b99b-112">фрсдиректорифилтер</span><span class="sxs-lookup"><span data-stu-id="6b99b-112">fRSDirectoryFilter</span></span>                          |
| <span data-ttu-id="6b99b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6b99b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="6b99b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6b99b-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6b99b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6b99b-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6b99b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6b99b-116">Attribute-Id</span></span>      | <span data-ttu-id="6b99b-117">1.2.840.113556.1.4.484</span><span class="sxs-lookup"><span data-stu-id="6b99b-117">1.2.840.113556.1.4.484</span></span>                      |
| <span data-ttu-id="6b99b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6b99b-118">System-Id-Guid</span></span>    | <span data-ttu-id="6b99b-119">1be8f171-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="6b99b-119">1be8f171-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="6b99b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b99b-120">Syntax</span></span>            | [<span data-ttu-id="6b99b-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="6b99b-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6b99b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6b99b-122">Implementations</span></span>

-   [<span data-ttu-id="6b99b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6b99b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6b99b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6b99b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6b99b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6b99b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6b99b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6b99b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6b99b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6b99b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6b99b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6b99b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6b99b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6b99b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6b99b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="6b99b-130">Entry</span></span> | <span data-ttu-id="6b99b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6b99b-131">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6b99b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6b99b-132">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b99b-133">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b99b-134">System-Only</span></span>            | <span data-ttu-id="6b99b-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-135">False</span></span>                                                     |
| <span data-ttu-id="6b99b-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6b99b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6b99b-137">True</span><span class="sxs-lookup"><span data-stu-id="6b99b-137">True</span></span>                                                      |
| <span data-ttu-id="6b99b-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6b99b-138">Is Indexed</span></span>             | <span data-ttu-id="6b99b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-139">False</span></span>                                                     |
| <span data-ttu-id="6b99b-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6b99b-140">In Global Catalog</span></span>      | <span data-ttu-id="6b99b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-141">False</span></span>                                                     |
| <span data-ttu-id="6b99b-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6b99b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b99b-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6b99b-143">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6b99b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b99b-144">Range-Lower</span></span>            | <span data-ttu-id="6b99b-145">0</span><span class="sxs-lookup"><span data-stu-id="6b99b-145">0</span></span>                                                         |
| <span data-ttu-id="6b99b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b99b-146">Range-Upper</span></span>            | <span data-ttu-id="6b99b-147">2048</span><span class="sxs-lookup"><span data-stu-id="6b99b-147">2048</span></span>                                                      |
| <span data-ttu-id="6b99b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-148">Search-Flags</span></span>           | <span data-ttu-id="6b99b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b99b-149">0x00000000</span></span>                                                |
| <span data-ttu-id="6b99b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-150">System-Flags</span></span>           | <span data-ttu-id="6b99b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b99b-151">0x00000010</span></span>                                                |
| <span data-ttu-id="6b99b-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6b99b-152">Classes used in</span></span>        | [<span data-ttu-id="6b99b-153">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6b99b-153">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6b99b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b99b-154">Windows Server 2003</span></span>



| <span data-ttu-id="6b99b-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="6b99b-155">Entry</span></span> | <span data-ttu-id="6b99b-156">Значение</span><span class="sxs-lookup"><span data-stu-id="6b99b-156">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6b99b-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6b99b-157">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b99b-158">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b99b-159">System-Only</span></span>            | <span data-ttu-id="6b99b-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-160">False</span></span>                                                     |
| <span data-ttu-id="6b99b-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6b99b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="6b99b-162">True</span><span class="sxs-lookup"><span data-stu-id="6b99b-162">True</span></span>                                                      |
| <span data-ttu-id="6b99b-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6b99b-163">Is Indexed</span></span>             | <span data-ttu-id="6b99b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-164">False</span></span>                                                     |
| <span data-ttu-id="6b99b-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6b99b-165">In Global Catalog</span></span>      | <span data-ttu-id="6b99b-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-166">False</span></span>                                                     |
| <span data-ttu-id="6b99b-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6b99b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b99b-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6b99b-168">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6b99b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b99b-169">Range-Lower</span></span>            | <span data-ttu-id="6b99b-170">0</span><span class="sxs-lookup"><span data-stu-id="6b99b-170">0</span></span>                                                         |
| <span data-ttu-id="6b99b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b99b-171">Range-Upper</span></span>            | <span data-ttu-id="6b99b-172">2048</span><span class="sxs-lookup"><span data-stu-id="6b99b-172">2048</span></span>                                                      |
| <span data-ttu-id="6b99b-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-173">Search-Flags</span></span>           | <span data-ttu-id="6b99b-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b99b-174">0x00000000</span></span>                                                |
| <span data-ttu-id="6b99b-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-175">System-Flags</span></span>           | <span data-ttu-id="6b99b-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b99b-176">0x00000010</span></span>                                                |
| <span data-ttu-id="6b99b-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6b99b-177">Classes used in</span></span>        | [<span data-ttu-id="6b99b-178">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6b99b-178">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6b99b-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6b99b-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6b99b-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="6b99b-180">Entry</span></span> | <span data-ttu-id="6b99b-181">Значение</span><span class="sxs-lookup"><span data-stu-id="6b99b-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6b99b-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6b99b-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b99b-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b99b-184">System-Only</span></span>            | <span data-ttu-id="6b99b-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-185">False</span></span>                                                     |
| <span data-ttu-id="6b99b-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6b99b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6b99b-187">True</span><span class="sxs-lookup"><span data-stu-id="6b99b-187">True</span></span>                                                      |
| <span data-ttu-id="6b99b-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6b99b-188">Is Indexed</span></span>             | <span data-ttu-id="6b99b-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-189">False</span></span>                                                     |
| <span data-ttu-id="6b99b-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6b99b-190">In Global Catalog</span></span>      | <span data-ttu-id="6b99b-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-191">False</span></span>                                                     |
| <span data-ttu-id="6b99b-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6b99b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b99b-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6b99b-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6b99b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b99b-194">Range-Lower</span></span>            | <span data-ttu-id="6b99b-195">0</span><span class="sxs-lookup"><span data-stu-id="6b99b-195">0</span></span>                                                         |
| <span data-ttu-id="6b99b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b99b-196">Range-Upper</span></span>            | <span data-ttu-id="6b99b-197">2048</span><span class="sxs-lookup"><span data-stu-id="6b99b-197">2048</span></span>                                                      |
| <span data-ttu-id="6b99b-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-198">Search-Flags</span></span>           | <span data-ttu-id="6b99b-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b99b-199">0x00000000</span></span>                                                |
| <span data-ttu-id="6b99b-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-200">System-Flags</span></span>           | <span data-ttu-id="6b99b-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b99b-201">0x00000010</span></span>                                                |
| <span data-ttu-id="6b99b-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6b99b-202">Classes used in</span></span>        | [<span data-ttu-id="6b99b-203">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6b99b-203">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6b99b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b99b-204">Windows Server 2008</span></span>



| <span data-ttu-id="6b99b-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="6b99b-205">Entry</span></span> | <span data-ttu-id="6b99b-206">Значение</span><span class="sxs-lookup"><span data-stu-id="6b99b-206">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6b99b-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6b99b-207">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b99b-208">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b99b-209">System-Only</span></span>            | <span data-ttu-id="6b99b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-210">False</span></span>                                                     |
| <span data-ttu-id="6b99b-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6b99b-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6b99b-212">True</span><span class="sxs-lookup"><span data-stu-id="6b99b-212">True</span></span>                                                      |
| <span data-ttu-id="6b99b-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6b99b-213">Is Indexed</span></span>             | <span data-ttu-id="6b99b-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-214">False</span></span>                                                     |
| <span data-ttu-id="6b99b-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6b99b-215">In Global Catalog</span></span>      | <span data-ttu-id="6b99b-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-216">False</span></span>                                                     |
| <span data-ttu-id="6b99b-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6b99b-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b99b-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6b99b-218">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6b99b-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b99b-219">Range-Lower</span></span>            | <span data-ttu-id="6b99b-220">0</span><span class="sxs-lookup"><span data-stu-id="6b99b-220">0</span></span>                                                         |
| <span data-ttu-id="6b99b-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b99b-221">Range-Upper</span></span>            | <span data-ttu-id="6b99b-222">2048</span><span class="sxs-lookup"><span data-stu-id="6b99b-222">2048</span></span>                                                      |
| <span data-ttu-id="6b99b-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-223">Search-Flags</span></span>           | <span data-ttu-id="6b99b-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b99b-224">0x00000000</span></span>                                                |
| <span data-ttu-id="6b99b-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-225">System-Flags</span></span>           | <span data-ttu-id="6b99b-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b99b-226">0x00000010</span></span>                                                |
| <span data-ttu-id="6b99b-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6b99b-227">Classes used in</span></span>        | [<span data-ttu-id="6b99b-228">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6b99b-228">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6b99b-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6b99b-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6b99b-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="6b99b-230">Entry</span></span> | <span data-ttu-id="6b99b-231">Значение</span><span class="sxs-lookup"><span data-stu-id="6b99b-231">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6b99b-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6b99b-232">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b99b-233">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b99b-234">System-Only</span></span>            | <span data-ttu-id="6b99b-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-235">False</span></span>                                                     |
| <span data-ttu-id="6b99b-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6b99b-236">Is-Single-Valued</span></span>       | <span data-ttu-id="6b99b-237">True</span><span class="sxs-lookup"><span data-stu-id="6b99b-237">True</span></span>                                                      |
| <span data-ttu-id="6b99b-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6b99b-238">Is Indexed</span></span>             | <span data-ttu-id="6b99b-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-239">False</span></span>                                                     |
| <span data-ttu-id="6b99b-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6b99b-240">In Global Catalog</span></span>      | <span data-ttu-id="6b99b-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-241">False</span></span>                                                     |
| <span data-ttu-id="6b99b-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6b99b-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b99b-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6b99b-243">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6b99b-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b99b-244">Range-Lower</span></span>            | <span data-ttu-id="6b99b-245">0</span><span class="sxs-lookup"><span data-stu-id="6b99b-245">0</span></span>                                                         |
| <span data-ttu-id="6b99b-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b99b-246">Range-Upper</span></span>            | <span data-ttu-id="6b99b-247">2048</span><span class="sxs-lookup"><span data-stu-id="6b99b-247">2048</span></span>                                                      |
| <span data-ttu-id="6b99b-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-248">Search-Flags</span></span>           | <span data-ttu-id="6b99b-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b99b-249">0x00000000</span></span>                                                |
| <span data-ttu-id="6b99b-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-250">System-Flags</span></span>           | <span data-ttu-id="6b99b-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b99b-251">0x00000010</span></span>                                                |
| <span data-ttu-id="6b99b-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6b99b-252">Classes used in</span></span>        | [<span data-ttu-id="6b99b-253">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6b99b-253">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6b99b-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6b99b-254">Windows Server 2012</span></span>



| <span data-ttu-id="6b99b-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="6b99b-255">Entry</span></span> | <span data-ttu-id="6b99b-256">Значение</span><span class="sxs-lookup"><span data-stu-id="6b99b-256">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6b99b-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6b99b-257">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b99b-258">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6b99b-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b99b-259">System-Only</span></span>            | <span data-ttu-id="6b99b-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-260">False</span></span>                                                     |
| <span data-ttu-id="6b99b-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6b99b-261">Is-Single-Valued</span></span>       | <span data-ttu-id="6b99b-262">True</span><span class="sxs-lookup"><span data-stu-id="6b99b-262">True</span></span>                                                      |
| <span data-ttu-id="6b99b-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6b99b-263">Is Indexed</span></span>             | <span data-ttu-id="6b99b-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-264">False</span></span>                                                     |
| <span data-ttu-id="6b99b-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6b99b-265">In Global Catalog</span></span>      | <span data-ttu-id="6b99b-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="6b99b-266">False</span></span>                                                     |
| <span data-ttu-id="6b99b-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6b99b-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b99b-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6b99b-268">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6b99b-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b99b-269">Range-Lower</span></span>            | <span data-ttu-id="6b99b-270">0</span><span class="sxs-lookup"><span data-stu-id="6b99b-270">0</span></span>                                                         |
| <span data-ttu-id="6b99b-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b99b-271">Range-Upper</span></span>            | <span data-ttu-id="6b99b-272">2048</span><span class="sxs-lookup"><span data-stu-id="6b99b-272">2048</span></span>                                                      |
| <span data-ttu-id="6b99b-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-273">Search-Flags</span></span>           | <span data-ttu-id="6b99b-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b99b-274">0x00000000</span></span>                                                |
| <span data-ttu-id="6b99b-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b99b-275">System-Flags</span></span>           | <span data-ttu-id="6b99b-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6b99b-276">0x00000010</span></span>                                                |
| <span data-ttu-id="6b99b-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6b99b-277">Classes used in</span></span>        | [<span data-ttu-id="6b99b-278">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6b99b-278">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





