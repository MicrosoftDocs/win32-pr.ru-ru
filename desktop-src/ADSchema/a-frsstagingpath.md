---
title: Атрибут «промежуточный путь FRS»
description: Путь к промежуточной области репликации файлов.
ms.assetid: f4b5ec14-3510-4b0e-954e-7793563754f2
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута пути промежуточного хранения FRS
- Схема AD атрибута Фрсстагингпас
topic_type:
- apiref
api_name:
- FRS-Staging-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7254b076daa4cd89216cd795fa6f7d21eb124843
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893610"
---
# <a name="frs-staging-path-attribute"></a><span data-ttu-id="c4993-105">Атрибут «промежуточный путь FRS»</span><span class="sxs-lookup"><span data-stu-id="c4993-105">FRS-Staging-Path attribute</span></span>

<span data-ttu-id="c4993-106">Путь к промежуточной области репликации файлов.</span><span class="sxs-lookup"><span data-stu-id="c4993-106">The path to the file replication staging area.</span></span>



| <span data-ttu-id="c4993-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c4993-107">Entry</span></span> | <span data-ttu-id="c4993-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c4993-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c4993-109">CN</span><span class="sxs-lookup"><span data-stu-id="c4993-109">CN</span></span>                | <span data-ttu-id="c4993-110">Каталог FRS-промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="c4993-110">FRS-Staging-Path</span></span>                            |
| <span data-ttu-id="c4993-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c4993-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c4993-112">фрсстагингпас</span><span class="sxs-lookup"><span data-stu-id="c4993-112">fRSStagingPath</span></span>                              |
| <span data-ttu-id="c4993-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c4993-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c4993-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c4993-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="c4993-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c4993-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c4993-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4993-116">Attribute-Id</span></span>      | <span data-ttu-id="c4993-117">1.2.840.113556.1.4.488</span><span class="sxs-lookup"><span data-stu-id="c4993-117">1.2.840.113556.1.4.488</span></span>                      |
| <span data-ttu-id="c4993-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c4993-118">System-Id-Guid</span></span>    | <span data-ttu-id="c4993-119">1be8f175-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c4993-119">1be8f175-a9ff-11d0-afe2-00c04fd930c9</span></span>        |
| <span data-ttu-id="c4993-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4993-120">Syntax</span></span>            | [<span data-ttu-id="c4993-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="c4993-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c4993-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c4993-122">Implementations</span></span>

-   [<span data-ttu-id="c4993-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c4993-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c4993-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c4993-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c4993-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4993-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4993-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4993-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4993-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4993-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4993-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4993-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c4993-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c4993-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c4993-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="c4993-130">Entry</span></span> | <span data-ttu-id="c4993-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c4993-131">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c4993-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c4993-132">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4993-133">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4993-134">System-Only</span></span>            | <span data-ttu-id="c4993-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-135">False</span></span>                                                    |
| <span data-ttu-id="c4993-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c4993-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c4993-137">True</span><span class="sxs-lookup"><span data-stu-id="c4993-137">True</span></span>                                                     |
| <span data-ttu-id="c4993-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c4993-138">Is Indexed</span></span>             | <span data-ttu-id="c4993-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-139">False</span></span>                                                    |
| <span data-ttu-id="c4993-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c4993-140">In Global Catalog</span></span>      | <span data-ttu-id="c4993-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-141">False</span></span>                                                    |
| <span data-ttu-id="c4993-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c4993-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4993-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4993-143">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c4993-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4993-144">Range-Lower</span></span>            | <span data-ttu-id="c4993-145">0</span><span class="sxs-lookup"><span data-stu-id="c4993-145">0</span></span>                                                        |
| <span data-ttu-id="c4993-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4993-146">Range-Upper</span></span>            | <span data-ttu-id="c4993-147">2048</span><span class="sxs-lookup"><span data-stu-id="c4993-147">2048</span></span>                                                     |
| <span data-ttu-id="c4993-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-148">Search-Flags</span></span>           | <span data-ttu-id="c4993-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4993-149">0x00000000</span></span>                                               |
| <span data-ttu-id="c4993-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-150">System-Flags</span></span>           | <span data-ttu-id="c4993-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4993-151">0x00000010</span></span>                                               |
| <span data-ttu-id="c4993-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c4993-152">Classes used in</span></span>        | [<span data-ttu-id="c4993-153">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="c4993-153">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c4993-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4993-154">Windows Server 2003</span></span>



| <span data-ttu-id="c4993-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="c4993-155">Entry</span></span> | <span data-ttu-id="c4993-156">Значение</span><span class="sxs-lookup"><span data-stu-id="c4993-156">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c4993-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c4993-157">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4993-158">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4993-159">System-Only</span></span>            | <span data-ttu-id="c4993-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-160">False</span></span>                                                    |
| <span data-ttu-id="c4993-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c4993-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c4993-162">True</span><span class="sxs-lookup"><span data-stu-id="c4993-162">True</span></span>                                                     |
| <span data-ttu-id="c4993-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c4993-163">Is Indexed</span></span>             | <span data-ttu-id="c4993-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-164">False</span></span>                                                    |
| <span data-ttu-id="c4993-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c4993-165">In Global Catalog</span></span>      | <span data-ttu-id="c4993-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-166">False</span></span>                                                    |
| <span data-ttu-id="c4993-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c4993-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4993-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4993-168">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c4993-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4993-169">Range-Lower</span></span>            | <span data-ttu-id="c4993-170">0</span><span class="sxs-lookup"><span data-stu-id="c4993-170">0</span></span>                                                        |
| <span data-ttu-id="c4993-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4993-171">Range-Upper</span></span>            | <span data-ttu-id="c4993-172">2048</span><span class="sxs-lookup"><span data-stu-id="c4993-172">2048</span></span>                                                     |
| <span data-ttu-id="c4993-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-173">Search-Flags</span></span>           | <span data-ttu-id="c4993-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4993-174">0x00000000</span></span>                                               |
| <span data-ttu-id="c4993-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-175">System-Flags</span></span>           | <span data-ttu-id="c4993-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4993-176">0x00000010</span></span>                                               |
| <span data-ttu-id="c4993-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c4993-177">Classes used in</span></span>        | [<span data-ttu-id="c4993-178">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="c4993-178">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4993-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4993-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4993-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="c4993-180">Entry</span></span> | <span data-ttu-id="c4993-181">Значение</span><span class="sxs-lookup"><span data-stu-id="c4993-181">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c4993-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c4993-182">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4993-183">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4993-184">System-Only</span></span>            | <span data-ttu-id="c4993-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-185">False</span></span>                                                    |
| <span data-ttu-id="c4993-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c4993-186">Is-Single-Valued</span></span>       | <span data-ttu-id="c4993-187">True</span><span class="sxs-lookup"><span data-stu-id="c4993-187">True</span></span>                                                     |
| <span data-ttu-id="c4993-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c4993-188">Is Indexed</span></span>             | <span data-ttu-id="c4993-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-189">False</span></span>                                                    |
| <span data-ttu-id="c4993-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c4993-190">In Global Catalog</span></span>      | <span data-ttu-id="c4993-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-191">False</span></span>                                                    |
| <span data-ttu-id="c4993-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c4993-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4993-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4993-193">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c4993-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4993-194">Range-Lower</span></span>            | <span data-ttu-id="c4993-195">0</span><span class="sxs-lookup"><span data-stu-id="c4993-195">0</span></span>                                                        |
| <span data-ttu-id="c4993-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4993-196">Range-Upper</span></span>            | <span data-ttu-id="c4993-197">2048</span><span class="sxs-lookup"><span data-stu-id="c4993-197">2048</span></span>                                                     |
| <span data-ttu-id="c4993-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-198">Search-Flags</span></span>           | <span data-ttu-id="c4993-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4993-199">0x00000000</span></span>                                               |
| <span data-ttu-id="c4993-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-200">System-Flags</span></span>           | <span data-ttu-id="c4993-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4993-201">0x00000010</span></span>                                               |
| <span data-ttu-id="c4993-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c4993-202">Classes used in</span></span>        | [<span data-ttu-id="c4993-203">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="c4993-203">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4993-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4993-204">Windows Server 2008</span></span>



| <span data-ttu-id="c4993-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="c4993-205">Entry</span></span> | <span data-ttu-id="c4993-206">Значение</span><span class="sxs-lookup"><span data-stu-id="c4993-206">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c4993-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c4993-207">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4993-208">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4993-209">System-Only</span></span>            | <span data-ttu-id="c4993-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-210">False</span></span>                                                    |
| <span data-ttu-id="c4993-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c4993-211">Is-Single-Valued</span></span>       | <span data-ttu-id="c4993-212">True</span><span class="sxs-lookup"><span data-stu-id="c4993-212">True</span></span>                                                     |
| <span data-ttu-id="c4993-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c4993-213">Is Indexed</span></span>             | <span data-ttu-id="c4993-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-214">False</span></span>                                                    |
| <span data-ttu-id="c4993-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c4993-215">In Global Catalog</span></span>      | <span data-ttu-id="c4993-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-216">False</span></span>                                                    |
| <span data-ttu-id="c4993-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c4993-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4993-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4993-218">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c4993-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4993-219">Range-Lower</span></span>            | <span data-ttu-id="c4993-220">0</span><span class="sxs-lookup"><span data-stu-id="c4993-220">0</span></span>                                                        |
| <span data-ttu-id="c4993-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4993-221">Range-Upper</span></span>            | <span data-ttu-id="c4993-222">2048</span><span class="sxs-lookup"><span data-stu-id="c4993-222">2048</span></span>                                                     |
| <span data-ttu-id="c4993-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-223">Search-Flags</span></span>           | <span data-ttu-id="c4993-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4993-224">0x00000000</span></span>                                               |
| <span data-ttu-id="c4993-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-225">System-Flags</span></span>           | <span data-ttu-id="c4993-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4993-226">0x00000010</span></span>                                               |
| <span data-ttu-id="c4993-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c4993-227">Classes used in</span></span>        | [<span data-ttu-id="c4993-228">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="c4993-228">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4993-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4993-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4993-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="c4993-230">Entry</span></span> | <span data-ttu-id="c4993-231">Значение</span><span class="sxs-lookup"><span data-stu-id="c4993-231">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c4993-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c4993-232">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4993-233">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4993-234">System-Only</span></span>            | <span data-ttu-id="c4993-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-235">False</span></span>                                                    |
| <span data-ttu-id="c4993-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c4993-236">Is-Single-Valued</span></span>       | <span data-ttu-id="c4993-237">True</span><span class="sxs-lookup"><span data-stu-id="c4993-237">True</span></span>                                                     |
| <span data-ttu-id="c4993-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c4993-238">Is Indexed</span></span>             | <span data-ttu-id="c4993-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-239">False</span></span>                                                    |
| <span data-ttu-id="c4993-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c4993-240">In Global Catalog</span></span>      | <span data-ttu-id="c4993-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-241">False</span></span>                                                    |
| <span data-ttu-id="c4993-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c4993-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4993-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4993-243">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c4993-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4993-244">Range-Lower</span></span>            | <span data-ttu-id="c4993-245">0</span><span class="sxs-lookup"><span data-stu-id="c4993-245">0</span></span>                                                        |
| <span data-ttu-id="c4993-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4993-246">Range-Upper</span></span>            | <span data-ttu-id="c4993-247">2048</span><span class="sxs-lookup"><span data-stu-id="c4993-247">2048</span></span>                                                     |
| <span data-ttu-id="c4993-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-248">Search-Flags</span></span>           | <span data-ttu-id="c4993-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4993-249">0x00000000</span></span>                                               |
| <span data-ttu-id="c4993-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-250">System-Flags</span></span>           | <span data-ttu-id="c4993-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4993-251">0x00000010</span></span>                                               |
| <span data-ttu-id="c4993-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c4993-252">Classes used in</span></span>        | [<span data-ttu-id="c4993-253">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="c4993-253">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4993-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4993-254">Windows Server 2012</span></span>



| <span data-ttu-id="c4993-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="c4993-255">Entry</span></span> | <span data-ttu-id="c4993-256">Значение</span><span class="sxs-lookup"><span data-stu-id="c4993-256">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="c4993-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c4993-257">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4993-258">MAPI-Id</span></span>                | \-                                                       |
| <span data-ttu-id="c4993-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4993-259">System-Only</span></span>            | <span data-ttu-id="c4993-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-260">False</span></span>                                                    |
| <span data-ttu-id="c4993-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c4993-261">Is-Single-Valued</span></span>       | <span data-ttu-id="c4993-262">True</span><span class="sxs-lookup"><span data-stu-id="c4993-262">True</span></span>                                                     |
| <span data-ttu-id="c4993-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c4993-263">Is Indexed</span></span>             | <span data-ttu-id="c4993-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-264">False</span></span>                                                    |
| <span data-ttu-id="c4993-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c4993-265">In Global Catalog</span></span>      | <span data-ttu-id="c4993-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="c4993-266">False</span></span>                                                    |
| <span data-ttu-id="c4993-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c4993-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4993-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c4993-268">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="c4993-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4993-269">Range-Lower</span></span>            | <span data-ttu-id="c4993-270">0</span><span class="sxs-lookup"><span data-stu-id="c4993-270">0</span></span>                                                        |
| <span data-ttu-id="c4993-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4993-271">Range-Upper</span></span>            | <span data-ttu-id="c4993-272">2048</span><span class="sxs-lookup"><span data-stu-id="c4993-272">2048</span></span>                                                     |
| <span data-ttu-id="c4993-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-273">Search-Flags</span></span>           | <span data-ttu-id="c4993-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4993-274">0x00000000</span></span>                                               |
| <span data-ttu-id="c4993-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4993-275">System-Flags</span></span>           | <span data-ttu-id="c4993-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4993-276">0x00000010</span></span>                                               |
| <span data-ttu-id="c4993-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c4993-277">Classes used in</span></span>        | [<span data-ttu-id="c4993-278">**NTFRS — подписчик**</span><span class="sxs-lookup"><span data-stu-id="c4993-278">**NTFRS-Subscriber**</span></span>](c-ntfrssubscriber.md)<br/> |



 

 





