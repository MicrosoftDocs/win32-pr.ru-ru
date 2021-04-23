---
title: Атрибут FRS-File-Filter
description: Список расширений имен файлов, исключенных из репликации файлов.
ms.assetid: 094a393a-9e1a-4da8-a38a-161102f164fd
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута FRS-File-Filter
- Схема AD атрибута Фрсфилефилтер
topic_type:
- apiref
api_name:
- FRS-File-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234cf7d6e56e84c2ed9578fc56036e581a2f0ad2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654848"
---
# <a name="frs-file-filter-attribute"></a><span data-ttu-id="6c1f2-105">Атрибут FRS-File-Filter</span><span class="sxs-lookup"><span data-stu-id="6c1f2-105">FRS-File-Filter attribute</span></span>

<span data-ttu-id="6c1f2-106">Список расширений имен файлов, исключенных из репликации файлов.</span><span class="sxs-lookup"><span data-stu-id="6c1f2-106">A list of file name extensions excluded from file replication.</span></span>



| <span data-ttu-id="6c1f2-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c1f2-107">Entry</span></span> | <span data-ttu-id="6c1f2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6c1f2-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6c1f2-109">CN</span><span class="sxs-lookup"><span data-stu-id="6c1f2-109">CN</span></span>                | <span data-ttu-id="6c1f2-110">FRS-File-Filter</span><span class="sxs-lookup"><span data-stu-id="6c1f2-110">FRS-File-Filter</span></span>                             |
| <span data-ttu-id="6c1f2-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6c1f2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6c1f2-112">фрсфилефилтер</span><span class="sxs-lookup"><span data-stu-id="6c1f2-112">fRSFileFilter</span></span>                               |
| <span data-ttu-id="6c1f2-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6c1f2-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="6c1f2-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6c1f2-114">Update Privilege</span></span>  | <span data-ttu-id="6c1f2-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="6c1f2-115">Domain administrator</span></span>                        |
| <span data-ttu-id="6c1f2-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6c1f2-116">Update Frequency</span></span>  | <span data-ttu-id="6c1f2-117">При установке репликации.</span><span class="sxs-lookup"><span data-stu-id="6c1f2-117">When replication is setup.</span></span>                  |
| <span data-ttu-id="6c1f2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6c1f2-118">Attribute-Id</span></span>      | <span data-ttu-id="6c1f2-119">1.2.840.113556.1.4.483</span><span class="sxs-lookup"><span data-stu-id="6c1f2-119">1.2.840.113556.1.4.483</span></span>                      |
| <span data-ttu-id="6c1f2-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6c1f2-120">System-Id-Guid</span></span>    | <span data-ttu-id="6c1f2-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="6c1f2-121">1be8f170-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="6c1f2-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c1f2-122">Syntax</span></span>            | [<span data-ttu-id="6c1f2-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6c1f2-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6c1f2-124">Implementations</span></span>

-   [<span data-ttu-id="6c1f2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6c1f2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6c1f2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6c1f2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6c1f2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6c1f2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6c1f2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c1f2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6c1f2-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c1f2-132">Entry</span></span> | <span data-ttu-id="6c1f2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6c1f2-133">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6c1f2-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c1f2-134">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c1f2-135">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c1f2-136">System-Only</span></span>            | <span data-ttu-id="6c1f2-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-137">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c1f2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6c1f2-139">True</span><span class="sxs-lookup"><span data-stu-id="6c1f2-139">True</span></span>                                                      |
| <span data-ttu-id="6c1f2-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c1f2-140">Is Indexed</span></span>             | <span data-ttu-id="6c1f2-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-141">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c1f2-142">In Global Catalog</span></span>      | <span data-ttu-id="6c1f2-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-143">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c1f2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c1f2-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c1f2-145">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6c1f2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c1f2-146">Range-Lower</span></span>            | <span data-ttu-id="6c1f2-147">0</span><span class="sxs-lookup"><span data-stu-id="6c1f2-147">0</span></span>                                                         |
| <span data-ttu-id="6c1f2-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c1f2-148">Range-Upper</span></span>            | <span data-ttu-id="6c1f2-149">2048</span><span class="sxs-lookup"><span data-stu-id="6c1f2-149">2048</span></span>                                                      |
| <span data-ttu-id="6c1f2-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-150">Search-Flags</span></span>           | <span data-ttu-id="6c1f2-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c1f2-151">0x00000000</span></span>                                                |
| <span data-ttu-id="6c1f2-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-152">System-Flags</span></span>           | <span data-ttu-id="6c1f2-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c1f2-153">0x00000010</span></span>                                                |
| <span data-ttu-id="6c1f2-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c1f2-154">Classes used in</span></span>        | [<span data-ttu-id="6c1f2-155">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-155">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6c1f2-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c1f2-156">Windows Server 2003</span></span>



| <span data-ttu-id="6c1f2-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c1f2-157">Entry</span></span> | <span data-ttu-id="6c1f2-158">Значение</span><span class="sxs-lookup"><span data-stu-id="6c1f2-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6c1f2-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c1f2-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c1f2-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c1f2-161">System-Only</span></span>            | <span data-ttu-id="6c1f2-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-162">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c1f2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6c1f2-164">True</span><span class="sxs-lookup"><span data-stu-id="6c1f2-164">True</span></span>                                                      |
| <span data-ttu-id="6c1f2-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c1f2-165">Is Indexed</span></span>             | <span data-ttu-id="6c1f2-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-166">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c1f2-167">In Global Catalog</span></span>      | <span data-ttu-id="6c1f2-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-168">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c1f2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c1f2-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c1f2-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6c1f2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c1f2-171">Range-Lower</span></span>            | <span data-ttu-id="6c1f2-172">0</span><span class="sxs-lookup"><span data-stu-id="6c1f2-172">0</span></span>                                                         |
| <span data-ttu-id="6c1f2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c1f2-173">Range-Upper</span></span>            | <span data-ttu-id="6c1f2-174">2048</span><span class="sxs-lookup"><span data-stu-id="6c1f2-174">2048</span></span>                                                      |
| <span data-ttu-id="6c1f2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-175">Search-Flags</span></span>           | <span data-ttu-id="6c1f2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c1f2-176">0x00000000</span></span>                                                |
| <span data-ttu-id="6c1f2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-177">System-Flags</span></span>           | <span data-ttu-id="6c1f2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c1f2-178">0x00000010</span></span>                                                |
| <span data-ttu-id="6c1f2-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c1f2-179">Classes used in</span></span>        | [<span data-ttu-id="6c1f2-180">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-180">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6c1f2-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6c1f2-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6c1f2-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c1f2-182">Entry</span></span> | <span data-ttu-id="6c1f2-183">Значение</span><span class="sxs-lookup"><span data-stu-id="6c1f2-183">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6c1f2-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c1f2-184">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c1f2-185">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c1f2-186">System-Only</span></span>            | <span data-ttu-id="6c1f2-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-187">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c1f2-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6c1f2-189">True</span><span class="sxs-lookup"><span data-stu-id="6c1f2-189">True</span></span>                                                      |
| <span data-ttu-id="6c1f2-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c1f2-190">Is Indexed</span></span>             | <span data-ttu-id="6c1f2-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-191">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c1f2-192">In Global Catalog</span></span>      | <span data-ttu-id="6c1f2-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-193">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c1f2-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c1f2-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c1f2-195">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6c1f2-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c1f2-196">Range-Lower</span></span>            | <span data-ttu-id="6c1f2-197">0</span><span class="sxs-lookup"><span data-stu-id="6c1f2-197">0</span></span>                                                         |
| <span data-ttu-id="6c1f2-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c1f2-198">Range-Upper</span></span>            | <span data-ttu-id="6c1f2-199">2048</span><span class="sxs-lookup"><span data-stu-id="6c1f2-199">2048</span></span>                                                      |
| <span data-ttu-id="6c1f2-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-200">Search-Flags</span></span>           | <span data-ttu-id="6c1f2-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c1f2-201">0x00000000</span></span>                                                |
| <span data-ttu-id="6c1f2-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-202">System-Flags</span></span>           | <span data-ttu-id="6c1f2-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c1f2-203">0x00000010</span></span>                                                |
| <span data-ttu-id="6c1f2-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c1f2-204">Classes used in</span></span>        | [<span data-ttu-id="6c1f2-205">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-205">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6c1f2-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c1f2-206">Windows Server 2008</span></span>



| <span data-ttu-id="6c1f2-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c1f2-207">Entry</span></span> | <span data-ttu-id="6c1f2-208">Значение</span><span class="sxs-lookup"><span data-stu-id="6c1f2-208">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6c1f2-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c1f2-209">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c1f2-210">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c1f2-211">System-Only</span></span>            | <span data-ttu-id="6c1f2-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-212">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c1f2-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6c1f2-214">True</span><span class="sxs-lookup"><span data-stu-id="6c1f2-214">True</span></span>                                                      |
| <span data-ttu-id="6c1f2-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c1f2-215">Is Indexed</span></span>             | <span data-ttu-id="6c1f2-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-216">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c1f2-217">In Global Catalog</span></span>      | <span data-ttu-id="6c1f2-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-218">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c1f2-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c1f2-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c1f2-220">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6c1f2-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c1f2-221">Range-Lower</span></span>            | <span data-ttu-id="6c1f2-222">0</span><span class="sxs-lookup"><span data-stu-id="6c1f2-222">0</span></span>                                                         |
| <span data-ttu-id="6c1f2-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c1f2-223">Range-Upper</span></span>            | <span data-ttu-id="6c1f2-224">2048</span><span class="sxs-lookup"><span data-stu-id="6c1f2-224">2048</span></span>                                                      |
| <span data-ttu-id="6c1f2-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-225">Search-Flags</span></span>           | <span data-ttu-id="6c1f2-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c1f2-226">0x00000000</span></span>                                                |
| <span data-ttu-id="6c1f2-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-227">System-Flags</span></span>           | <span data-ttu-id="6c1f2-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c1f2-228">0x00000010</span></span>                                                |
| <span data-ttu-id="6c1f2-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c1f2-229">Classes used in</span></span>        | [<span data-ttu-id="6c1f2-230">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-230">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6c1f2-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c1f2-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6c1f2-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c1f2-232">Entry</span></span> | <span data-ttu-id="6c1f2-233">Значение</span><span class="sxs-lookup"><span data-stu-id="6c1f2-233">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6c1f2-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c1f2-234">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c1f2-235">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c1f2-236">System-Only</span></span>            | <span data-ttu-id="6c1f2-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-237">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c1f2-238">Is-Single-Valued</span></span>       | <span data-ttu-id="6c1f2-239">True</span><span class="sxs-lookup"><span data-stu-id="6c1f2-239">True</span></span>                                                      |
| <span data-ttu-id="6c1f2-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c1f2-240">Is Indexed</span></span>             | <span data-ttu-id="6c1f2-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-241">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c1f2-242">In Global Catalog</span></span>      | <span data-ttu-id="6c1f2-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-243">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c1f2-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c1f2-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c1f2-245">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6c1f2-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c1f2-246">Range-Lower</span></span>            | <span data-ttu-id="6c1f2-247">0</span><span class="sxs-lookup"><span data-stu-id="6c1f2-247">0</span></span>                                                         |
| <span data-ttu-id="6c1f2-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c1f2-248">Range-Upper</span></span>            | <span data-ttu-id="6c1f2-249">2048</span><span class="sxs-lookup"><span data-stu-id="6c1f2-249">2048</span></span>                                                      |
| <span data-ttu-id="6c1f2-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-250">Search-Flags</span></span>           | <span data-ttu-id="6c1f2-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c1f2-251">0x00000000</span></span>                                                |
| <span data-ttu-id="6c1f2-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-252">System-Flags</span></span>           | <span data-ttu-id="6c1f2-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c1f2-253">0x00000010</span></span>                                                |
| <span data-ttu-id="6c1f2-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c1f2-254">Classes used in</span></span>        | [<span data-ttu-id="6c1f2-255">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-255">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6c1f2-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c1f2-256">Windows Server 2012</span></span>



| <span data-ttu-id="6c1f2-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c1f2-257">Entry</span></span> | <span data-ttu-id="6c1f2-258">Значение</span><span class="sxs-lookup"><span data-stu-id="6c1f2-258">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6c1f2-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c1f2-259">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c1f2-260">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="6c1f2-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c1f2-261">System-Only</span></span>            | <span data-ttu-id="6c1f2-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-262">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c1f2-263">Is-Single-Valued</span></span>       | <span data-ttu-id="6c1f2-264">True</span><span class="sxs-lookup"><span data-stu-id="6c1f2-264">True</span></span>                                                      |
| <span data-ttu-id="6c1f2-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c1f2-265">Is Indexed</span></span>             | <span data-ttu-id="6c1f2-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-266">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c1f2-267">In Global Catalog</span></span>      | <span data-ttu-id="6c1f2-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c1f2-268">False</span></span>                                                     |
| <span data-ttu-id="6c1f2-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c1f2-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c1f2-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c1f2-270">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="6c1f2-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c1f2-271">Range-Lower</span></span>            | <span data-ttu-id="6c1f2-272">0</span><span class="sxs-lookup"><span data-stu-id="6c1f2-272">0</span></span>                                                         |
| <span data-ttu-id="6c1f2-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c1f2-273">Range-Upper</span></span>            | <span data-ttu-id="6c1f2-274">2048</span><span class="sxs-lookup"><span data-stu-id="6c1f2-274">2048</span></span>                                                      |
| <span data-ttu-id="6c1f2-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-275">Search-Flags</span></span>           | <span data-ttu-id="6c1f2-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c1f2-276">0x00000000</span></span>                                                |
| <span data-ttu-id="6c1f2-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c1f2-277">System-Flags</span></span>           | <span data-ttu-id="6c1f2-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c1f2-278">0x00000010</span></span>                                                |
| <span data-ttu-id="6c1f2-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c1f2-279">Classes used in</span></span>        | [<span data-ttu-id="6c1f2-280">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="6c1f2-280">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





