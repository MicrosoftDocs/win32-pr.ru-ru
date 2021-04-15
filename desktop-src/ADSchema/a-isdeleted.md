---
title: Атрибут Is-Deleted
description: Если значение — TRUE, этот объект был помечен для удаления и не может быть создан. После истечения периода захоронения он будет удален из системы.
ms.assetid: 549b5161-5d2f-47d7-8192-4480334ef13d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Is-Deleted
- Схема AD атрибута isDeleted
topic_type:
- apiref
api_name:
- Is-Deleted
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b30dec5ed139da60853324b82cc6e0f55fcc70
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654810"
---
# <a name="is-deleted-attribute"></a><span data-ttu-id="473b5-106">Атрибут Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="473b5-106">Is-Deleted attribute</span></span>

<span data-ttu-id="473b5-107">Если **значение — true**, этот объект был помечен для удаления и не может быть создан.</span><span class="sxs-lookup"><span data-stu-id="473b5-107">If **TRUE**, this object has been marked for deletion and cannot be instantiated.</span></span> <span data-ttu-id="473b5-108">После истечения периода захоронения он будет удален из системы.</span><span class="sxs-lookup"><span data-stu-id="473b5-108">After the tombstone period has expired, it will be removed from the system.</span></span>



| <span data-ttu-id="473b5-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="473b5-109">Entry</span></span> | <span data-ttu-id="473b5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="473b5-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="473b5-111">CN</span><span class="sxs-lookup"><span data-stu-id="473b5-111">CN</span></span>                | <span data-ttu-id="473b5-112">Is-Deleted</span><span class="sxs-lookup"><span data-stu-id="473b5-112">Is-Deleted</span></span>                           |
| <span data-ttu-id="473b5-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="473b5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="473b5-114">isDeleted</span><span class="sxs-lookup"><span data-stu-id="473b5-114">isDeleted</span></span>                            |
| <span data-ttu-id="473b5-115">Размер</span><span class="sxs-lookup"><span data-stu-id="473b5-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="473b5-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="473b5-116">Update Privilege</span></span>  | <span data-ttu-id="473b5-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="473b5-117">Domain administrator</span></span>                 |
| <span data-ttu-id="473b5-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="473b5-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="473b5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="473b5-119">Attribute-Id</span></span>      | <span data-ttu-id="473b5-120">1.2.840.113556.1.2.48</span><span class="sxs-lookup"><span data-stu-id="473b5-120">1.2.840.113556.1.2.48</span></span>                |
| <span data-ttu-id="473b5-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="473b5-121">System-Id-Guid</span></span>    | <span data-ttu-id="473b5-122">bf96798f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="473b5-122">bf96798f-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="473b5-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="473b5-123">Syntax</span></span>            | [<span data-ttu-id="473b5-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="473b5-124">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="473b5-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="473b5-125">Implementations</span></span>

-   [<span data-ttu-id="473b5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="473b5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="473b5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="473b5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="473b5-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="473b5-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="473b5-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="473b5-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="473b5-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="473b5-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="473b5-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="473b5-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="473b5-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="473b5-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="473b5-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="473b5-133">Windows 2000 Server</span></span>



| <span data-ttu-id="473b5-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="473b5-134">Entry</span></span> | <span data-ttu-id="473b5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="473b5-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="473b5-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="473b5-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="473b5-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="473b5-137">MAPI-Id</span></span>                | <span data-ttu-id="473b5-138">0x80C0</span><span class="sxs-lookup"><span data-stu-id="473b5-138">0x80C0</span></span>                          |
| <span data-ttu-id="473b5-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="473b5-139">System-Only</span></span>            | <span data-ttu-id="473b5-140">True</span><span class="sxs-lookup"><span data-stu-id="473b5-140">True</span></span>                            |
| <span data-ttu-id="473b5-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="473b5-141">Is-Single-Valued</span></span>       | <span data-ttu-id="473b5-142">True</span><span class="sxs-lookup"><span data-stu-id="473b5-142">True</span></span>                            |
| <span data-ttu-id="473b5-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="473b5-143">Is Indexed</span></span>             | <span data-ttu-id="473b5-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="473b5-144">False</span></span>                           |
| <span data-ttu-id="473b5-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="473b5-145">In Global Catalog</span></span>      | <span data-ttu-id="473b5-146">True</span><span class="sxs-lookup"><span data-stu-id="473b5-146">True</span></span>                            |
| <span data-ttu-id="473b5-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="473b5-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="473b5-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="473b5-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="473b5-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="473b5-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="473b5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="473b5-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="473b5-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-151">Search-Flags</span></span>           | <span data-ttu-id="473b5-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="473b5-152">0x00000000</span></span>                      |
| <span data-ttu-id="473b5-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-153">System-Flags</span></span>           | <span data-ttu-id="473b5-154">0x00000012</span><span class="sxs-lookup"><span data-stu-id="473b5-154">0x00000012</span></span>                      |
| <span data-ttu-id="473b5-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="473b5-155">Classes used in</span></span>        | [<span data-ttu-id="473b5-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="473b5-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="473b5-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="473b5-157">Windows Server 2003</span></span>



| <span data-ttu-id="473b5-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="473b5-158">Entry</span></span> | <span data-ttu-id="473b5-159">Значение</span><span class="sxs-lookup"><span data-stu-id="473b5-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="473b5-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="473b5-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="473b5-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="473b5-161">MAPI-Id</span></span>                | <span data-ttu-id="473b5-162">0x80C0</span><span class="sxs-lookup"><span data-stu-id="473b5-162">0x80C0</span></span>                          |
| <span data-ttu-id="473b5-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="473b5-163">System-Only</span></span>            | <span data-ttu-id="473b5-164">True</span><span class="sxs-lookup"><span data-stu-id="473b5-164">True</span></span>                            |
| <span data-ttu-id="473b5-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="473b5-165">Is-Single-Valued</span></span>       | <span data-ttu-id="473b5-166">True</span><span class="sxs-lookup"><span data-stu-id="473b5-166">True</span></span>                            |
| <span data-ttu-id="473b5-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="473b5-167">Is Indexed</span></span>             | <span data-ttu-id="473b5-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="473b5-168">False</span></span>                           |
| <span data-ttu-id="473b5-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="473b5-169">In Global Catalog</span></span>      | <span data-ttu-id="473b5-170">True</span><span class="sxs-lookup"><span data-stu-id="473b5-170">True</span></span>                            |
| <span data-ttu-id="473b5-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="473b5-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="473b5-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="473b5-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="473b5-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="473b5-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="473b5-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="473b5-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="473b5-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-175">Search-Flags</span></span>           | <span data-ttu-id="473b5-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="473b5-176">0x00000000</span></span>                      |
| <span data-ttu-id="473b5-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-177">System-Flags</span></span>           | <span data-ttu-id="473b5-178">0x00000012</span><span class="sxs-lookup"><span data-stu-id="473b5-178">0x00000012</span></span>                      |
| <span data-ttu-id="473b5-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="473b5-179">Classes used in</span></span>        | [<span data-ttu-id="473b5-180">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="473b5-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="473b5-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="473b5-181">ADAM</span></span>



| <span data-ttu-id="473b5-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="473b5-182">Entry</span></span> | <span data-ttu-id="473b5-183">Значение</span><span class="sxs-lookup"><span data-stu-id="473b5-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="473b5-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="473b5-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="473b5-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="473b5-185">MAPI-Id</span></span>                | <span data-ttu-id="473b5-186">0x80C0</span><span class="sxs-lookup"><span data-stu-id="473b5-186">0x80C0</span></span>                          |
| <span data-ttu-id="473b5-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="473b5-187">System-Only</span></span>            | <span data-ttu-id="473b5-188">True</span><span class="sxs-lookup"><span data-stu-id="473b5-188">True</span></span>                            |
| <span data-ttu-id="473b5-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="473b5-189">Is-Single-Valued</span></span>       | <span data-ttu-id="473b5-190">True</span><span class="sxs-lookup"><span data-stu-id="473b5-190">True</span></span>                            |
| <span data-ttu-id="473b5-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="473b5-191">Is Indexed</span></span>             | <span data-ttu-id="473b5-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="473b5-192">False</span></span>                           |
| <span data-ttu-id="473b5-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="473b5-193">In Global Catalog</span></span>      | <span data-ttu-id="473b5-194">True</span><span class="sxs-lookup"><span data-stu-id="473b5-194">True</span></span>                            |
| <span data-ttu-id="473b5-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="473b5-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="473b5-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="473b5-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="473b5-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="473b5-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="473b5-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="473b5-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="473b5-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-199">Search-Flags</span></span>           | <span data-ttu-id="473b5-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="473b5-200">0x00000000</span></span>                      |
| <span data-ttu-id="473b5-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-201">System-Flags</span></span>           | <span data-ttu-id="473b5-202">0x00000012</span><span class="sxs-lookup"><span data-stu-id="473b5-202">0x00000012</span></span>                      |
| <span data-ttu-id="473b5-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="473b5-203">Classes used in</span></span>        | [<span data-ttu-id="473b5-204">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="473b5-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="473b5-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="473b5-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="473b5-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="473b5-206">Entry</span></span> | <span data-ttu-id="473b5-207">Значение</span><span class="sxs-lookup"><span data-stu-id="473b5-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="473b5-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="473b5-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="473b5-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="473b5-209">MAPI-Id</span></span>                | <span data-ttu-id="473b5-210">0x80C0</span><span class="sxs-lookup"><span data-stu-id="473b5-210">0x80C0</span></span>                          |
| <span data-ttu-id="473b5-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="473b5-211">System-Only</span></span>            | <span data-ttu-id="473b5-212">True</span><span class="sxs-lookup"><span data-stu-id="473b5-212">True</span></span>                            |
| <span data-ttu-id="473b5-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="473b5-213">Is-Single-Valued</span></span>       | <span data-ttu-id="473b5-214">True</span><span class="sxs-lookup"><span data-stu-id="473b5-214">True</span></span>                            |
| <span data-ttu-id="473b5-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="473b5-215">Is Indexed</span></span>             | <span data-ttu-id="473b5-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="473b5-216">False</span></span>                           |
| <span data-ttu-id="473b5-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="473b5-217">In Global Catalog</span></span>      | <span data-ttu-id="473b5-218">True</span><span class="sxs-lookup"><span data-stu-id="473b5-218">True</span></span>                            |
| <span data-ttu-id="473b5-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="473b5-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="473b5-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="473b5-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="473b5-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="473b5-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="473b5-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="473b5-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="473b5-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-223">Search-Flags</span></span>           | <span data-ttu-id="473b5-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="473b5-224">0x00000000</span></span>                      |
| <span data-ttu-id="473b5-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-225">System-Flags</span></span>           | <span data-ttu-id="473b5-226">0x00000012</span><span class="sxs-lookup"><span data-stu-id="473b5-226">0x00000012</span></span>                      |
| <span data-ttu-id="473b5-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="473b5-227">Classes used in</span></span>        | [<span data-ttu-id="473b5-228">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="473b5-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="473b5-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="473b5-229">Windows Server 2008</span></span>



| <span data-ttu-id="473b5-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="473b5-230">Entry</span></span> | <span data-ttu-id="473b5-231">Значение</span><span class="sxs-lookup"><span data-stu-id="473b5-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="473b5-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="473b5-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="473b5-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="473b5-233">MAPI-Id</span></span>                | <span data-ttu-id="473b5-234">0x80C0</span><span class="sxs-lookup"><span data-stu-id="473b5-234">0x80C0</span></span>                          |
| <span data-ttu-id="473b5-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="473b5-235">System-Only</span></span>            | <span data-ttu-id="473b5-236">True</span><span class="sxs-lookup"><span data-stu-id="473b5-236">True</span></span>                            |
| <span data-ttu-id="473b5-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="473b5-237">Is-Single-Valued</span></span>       | <span data-ttu-id="473b5-238">True</span><span class="sxs-lookup"><span data-stu-id="473b5-238">True</span></span>                            |
| <span data-ttu-id="473b5-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="473b5-239">Is Indexed</span></span>             | <span data-ttu-id="473b5-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="473b5-240">False</span></span>                           |
| <span data-ttu-id="473b5-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="473b5-241">In Global Catalog</span></span>      | <span data-ttu-id="473b5-242">True</span><span class="sxs-lookup"><span data-stu-id="473b5-242">True</span></span>                            |
| <span data-ttu-id="473b5-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="473b5-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="473b5-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="473b5-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="473b5-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="473b5-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="473b5-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="473b5-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="473b5-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-247">Search-Flags</span></span>           | <span data-ttu-id="473b5-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="473b5-248">0x00000000</span></span>                      |
| <span data-ttu-id="473b5-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-249">System-Flags</span></span>           | <span data-ttu-id="473b5-250">0x00000012</span><span class="sxs-lookup"><span data-stu-id="473b5-250">0x00000012</span></span>                      |
| <span data-ttu-id="473b5-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="473b5-251">Classes used in</span></span>        | [<span data-ttu-id="473b5-252">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="473b5-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="473b5-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="473b5-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="473b5-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="473b5-254">Entry</span></span> | <span data-ttu-id="473b5-255">Значение</span><span class="sxs-lookup"><span data-stu-id="473b5-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="473b5-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="473b5-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="473b5-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="473b5-257">MAPI-Id</span></span>                | <span data-ttu-id="473b5-258">0x80C0</span><span class="sxs-lookup"><span data-stu-id="473b5-258">0x80C0</span></span>                          |
| <span data-ttu-id="473b5-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="473b5-259">System-Only</span></span>            | <span data-ttu-id="473b5-260">True</span><span class="sxs-lookup"><span data-stu-id="473b5-260">True</span></span>                            |
| <span data-ttu-id="473b5-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="473b5-261">Is-Single-Valued</span></span>       | <span data-ttu-id="473b5-262">True</span><span class="sxs-lookup"><span data-stu-id="473b5-262">True</span></span>                            |
| <span data-ttu-id="473b5-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="473b5-263">Is Indexed</span></span>             | <span data-ttu-id="473b5-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="473b5-264">False</span></span>                           |
| <span data-ttu-id="473b5-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="473b5-265">In Global Catalog</span></span>      | <span data-ttu-id="473b5-266">True</span><span class="sxs-lookup"><span data-stu-id="473b5-266">True</span></span>                            |
| <span data-ttu-id="473b5-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="473b5-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="473b5-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="473b5-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="473b5-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="473b5-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="473b5-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="473b5-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="473b5-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-271">Search-Flags</span></span>           | <span data-ttu-id="473b5-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="473b5-272">0x00000000</span></span>                      |
| <span data-ttu-id="473b5-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-273">System-Flags</span></span>           | <span data-ttu-id="473b5-274">0x00000012</span><span class="sxs-lookup"><span data-stu-id="473b5-274">0x00000012</span></span>                      |
| <span data-ttu-id="473b5-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="473b5-275">Classes used in</span></span>        | [<span data-ttu-id="473b5-276">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="473b5-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="473b5-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="473b5-277">Windows Server 2012</span></span>



| <span data-ttu-id="473b5-278">Ввод</span><span class="sxs-lookup"><span data-stu-id="473b5-278">Entry</span></span> | <span data-ttu-id="473b5-279">Значение</span><span class="sxs-lookup"><span data-stu-id="473b5-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="473b5-280">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="473b5-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="473b5-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="473b5-281">MAPI-Id</span></span>                | <span data-ttu-id="473b5-282">0x80C0</span><span class="sxs-lookup"><span data-stu-id="473b5-282">0x80C0</span></span>                          |
| <span data-ttu-id="473b5-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="473b5-283">System-Only</span></span>            | <span data-ttu-id="473b5-284">True</span><span class="sxs-lookup"><span data-stu-id="473b5-284">True</span></span>                            |
| <span data-ttu-id="473b5-285">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="473b5-285">Is-Single-Valued</span></span>       | <span data-ttu-id="473b5-286">True</span><span class="sxs-lookup"><span data-stu-id="473b5-286">True</span></span>                            |
| <span data-ttu-id="473b5-287">Индексируется</span><span class="sxs-lookup"><span data-stu-id="473b5-287">Is Indexed</span></span>             | <span data-ttu-id="473b5-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="473b5-288">False</span></span>                           |
| <span data-ttu-id="473b5-289">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="473b5-289">In Global Catalog</span></span>      | <span data-ttu-id="473b5-290">True</span><span class="sxs-lookup"><span data-stu-id="473b5-290">True</span></span>                            |
| <span data-ttu-id="473b5-291">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="473b5-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="473b5-292">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="473b5-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="473b5-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="473b5-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="473b5-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="473b5-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="473b5-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-295">Search-Flags</span></span>           | <span data-ttu-id="473b5-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="473b5-296">0x00000000</span></span>                      |
| <span data-ttu-id="473b5-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="473b5-297">System-Flags</span></span>           | <span data-ttu-id="473b5-298">0x00000012</span><span class="sxs-lookup"><span data-stu-id="473b5-298">0x00000012</span></span>                      |
| <span data-ttu-id="473b5-299">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="473b5-299">Classes used in</span></span>        | [<span data-ttu-id="473b5-300">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="473b5-300">**Top**</span></span>](c-top.md)<br/> |



 

 





