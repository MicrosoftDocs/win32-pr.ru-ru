---
title: MS-DS-site-атрибут сходства
description: Атрибут "MS-DS-site-Affinity" используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута сходства MS-DS-site
- msDS — схема AD атрибута сходства сайтов
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd3ed17b07c73d9e7a6a2d93d93463e1dea40fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893805"
---
# <a name="ms-ds-site-affinity-attribute"></a><span data-ttu-id="ae603-105">MS-DS-site-атрибут сходства</span><span class="sxs-lookup"><span data-stu-id="ae603-105">ms-DS-Site-Affinity attribute</span></span>

<span data-ttu-id="ae603-106">Атрибут " **MS-DS-site-affinity** " используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.</span><span class="sxs-lookup"><span data-stu-id="ae603-106">The **ms-DS-Site-Affinity** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="ae603-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae603-107">Entry</span></span> | <span data-ttu-id="ae603-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ae603-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae603-109">CN</span><span class="sxs-lookup"><span data-stu-id="ae603-109">CN</span></span>                | <span data-ttu-id="ae603-110">Соответствие MS-DS-site-affinity</span><span class="sxs-lookup"><span data-stu-id="ae603-110">ms-DS-Site-Affinity</span></span>                                                                     |
| <span data-ttu-id="ae603-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ae603-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ae603-112">msDS — сходство сайтов</span><span class="sxs-lookup"><span data-stu-id="ae603-112">msDS-Site-Affinity</span></span>                                                                      |
| <span data-ttu-id="ae603-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ae603-113">Size</span></span>              | <span data-ttu-id="ae603-114">Многозначный бинарный большой двоичный объект, где каждое значение имеет тип sizeof (GUID) + sizeof (большое \_ целое число).</span><span class="sxs-lookup"><span data-stu-id="ae603-114">Multiple-valued binary BLOB, where each value is sizeof(GUID) + sizeof(LARGE\_INTEGER).</span></span> |
| <span data-ttu-id="ae603-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ae603-115">Update Privilege</span></span>  | \-                                                                                      |
| <span data-ttu-id="ae603-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ae603-116">Update Frequency</span></span>  | <span data-ttu-id="ae603-117">По умолчанию — каждые три месяца.</span><span class="sxs-lookup"><span data-stu-id="ae603-117">By default once every three months.</span></span>                                                     |
| <span data-ttu-id="ae603-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ae603-118">Attribute-Id</span></span>      | <span data-ttu-id="ae603-119">1.2.840.113556.1.4.1443</span><span class="sxs-lookup"><span data-stu-id="ae603-119">1.2.840.113556.1.4.1443</span></span>                                                                 |
| <span data-ttu-id="ae603-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ae603-120">System-Id-Guid</span></span>    | <span data-ttu-id="ae603-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span><span class="sxs-lookup"><span data-stu-id="ae603-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span></span>                                                    |
| <span data-ttu-id="ae603-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae603-122">Syntax</span></span>            | [<span data-ttu-id="ae603-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="ae603-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                   |



## <a name="implementations"></a><span data-ttu-id="ae603-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ae603-124">Implementations</span></span>

-   [<span data-ttu-id="ae603-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ae603-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ae603-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ae603-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ae603-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ae603-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ae603-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ae603-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ae603-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ae603-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ae603-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ae603-130">Windows Server 2003</span></span>



| <span data-ttu-id="ae603-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae603-131">Entry</span></span> | <span data-ttu-id="ae603-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ae603-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ae603-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae603-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae603-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae603-135">System-Only</span></span>            | <span data-ttu-id="ae603-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-136">False</span></span>                             |
| <span data-ttu-id="ae603-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae603-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ae603-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-138">False</span></span>                             |
| <span data-ttu-id="ae603-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae603-139">Is Indexed</span></span>             | <span data-ttu-id="ae603-140">True</span><span class="sxs-lookup"><span data-stu-id="ae603-140">True</span></span>                              |
| <span data-ttu-id="ae603-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae603-141">In Global Catalog</span></span>      | <span data-ttu-id="ae603-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-142">False</span></span>                             |
| <span data-ttu-id="ae603-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae603-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae603-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae603-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ae603-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae603-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ae603-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae603-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ae603-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-147">Search-Flags</span></span>           | <span data-ttu-id="ae603-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ae603-148">0x00000001</span></span>                        |
| <span data-ttu-id="ae603-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-149">System-Flags</span></span>           | <span data-ttu-id="ae603-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae603-150">0x00000010</span></span>                        |
| <span data-ttu-id="ae603-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae603-151">Classes used in</span></span>        | [<span data-ttu-id="ae603-152">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="ae603-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ae603-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ae603-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ae603-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae603-154">Entry</span></span> | <span data-ttu-id="ae603-155">Значение</span><span class="sxs-lookup"><span data-stu-id="ae603-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ae603-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae603-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae603-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae603-158">System-Only</span></span>            | <span data-ttu-id="ae603-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-159">False</span></span>                             |
| <span data-ttu-id="ae603-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae603-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ae603-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-161">False</span></span>                             |
| <span data-ttu-id="ae603-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae603-162">Is Indexed</span></span>             | <span data-ttu-id="ae603-163">True</span><span class="sxs-lookup"><span data-stu-id="ae603-163">True</span></span>                              |
| <span data-ttu-id="ae603-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae603-164">In Global Catalog</span></span>      | <span data-ttu-id="ae603-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-165">False</span></span>                             |
| <span data-ttu-id="ae603-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae603-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae603-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae603-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ae603-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae603-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ae603-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae603-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ae603-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-170">Search-Flags</span></span>           | <span data-ttu-id="ae603-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ae603-171">0x00000001</span></span>                        |
| <span data-ttu-id="ae603-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-172">System-Flags</span></span>           | <span data-ttu-id="ae603-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae603-173">0x00000010</span></span>                        |
| <span data-ttu-id="ae603-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae603-174">Classes used in</span></span>        | [<span data-ttu-id="ae603-175">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="ae603-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ae603-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae603-176">Windows Server 2008</span></span>



| <span data-ttu-id="ae603-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae603-177">Entry</span></span> | <span data-ttu-id="ae603-178">Значение</span><span class="sxs-lookup"><span data-stu-id="ae603-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ae603-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae603-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae603-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae603-181">System-Only</span></span>            | <span data-ttu-id="ae603-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-182">False</span></span>                             |
| <span data-ttu-id="ae603-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae603-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ae603-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-184">False</span></span>                             |
| <span data-ttu-id="ae603-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae603-185">Is Indexed</span></span>             | <span data-ttu-id="ae603-186">True</span><span class="sxs-lookup"><span data-stu-id="ae603-186">True</span></span>                              |
| <span data-ttu-id="ae603-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae603-187">In Global Catalog</span></span>      | <span data-ttu-id="ae603-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-188">False</span></span>                             |
| <span data-ttu-id="ae603-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae603-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae603-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae603-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ae603-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae603-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ae603-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae603-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ae603-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-193">Search-Flags</span></span>           | <span data-ttu-id="ae603-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ae603-194">0x00000001</span></span>                        |
| <span data-ttu-id="ae603-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-195">System-Flags</span></span>           | <span data-ttu-id="ae603-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae603-196">0x00000010</span></span>                        |
| <span data-ttu-id="ae603-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae603-197">Classes used in</span></span>        | [<span data-ttu-id="ae603-198">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="ae603-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ae603-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae603-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ae603-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae603-200">Entry</span></span> | <span data-ttu-id="ae603-201">Значение</span><span class="sxs-lookup"><span data-stu-id="ae603-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ae603-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae603-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae603-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae603-204">System-Only</span></span>            | <span data-ttu-id="ae603-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-205">False</span></span>                             |
| <span data-ttu-id="ae603-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae603-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ae603-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-207">False</span></span>                             |
| <span data-ttu-id="ae603-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae603-208">Is Indexed</span></span>             | <span data-ttu-id="ae603-209">True</span><span class="sxs-lookup"><span data-stu-id="ae603-209">True</span></span>                              |
| <span data-ttu-id="ae603-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae603-210">In Global Catalog</span></span>      | <span data-ttu-id="ae603-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-211">False</span></span>                             |
| <span data-ttu-id="ae603-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae603-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae603-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae603-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ae603-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae603-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ae603-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae603-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ae603-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-216">Search-Flags</span></span>           | <span data-ttu-id="ae603-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ae603-217">0x00000001</span></span>                        |
| <span data-ttu-id="ae603-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-218">System-Flags</span></span>           | <span data-ttu-id="ae603-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae603-219">0x00000010</span></span>                        |
| <span data-ttu-id="ae603-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae603-220">Classes used in</span></span>        | [<span data-ttu-id="ae603-221">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="ae603-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ae603-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae603-222">Windows Server 2012</span></span>



| <span data-ttu-id="ae603-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae603-223">Entry</span></span> | <span data-ttu-id="ae603-224">Значение</span><span class="sxs-lookup"><span data-stu-id="ae603-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="ae603-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae603-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae603-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="ae603-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae603-227">System-Only</span></span>            | <span data-ttu-id="ae603-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-228">False</span></span>                             |
| <span data-ttu-id="ae603-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae603-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ae603-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-230">False</span></span>                             |
| <span data-ttu-id="ae603-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae603-231">Is Indexed</span></span>             | <span data-ttu-id="ae603-232">True</span><span class="sxs-lookup"><span data-stu-id="ae603-232">True</span></span>                              |
| <span data-ttu-id="ae603-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae603-233">In Global Catalog</span></span>      | <span data-ttu-id="ae603-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae603-234">False</span></span>                             |
| <span data-ttu-id="ae603-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae603-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae603-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae603-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="ae603-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae603-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="ae603-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae603-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="ae603-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-239">Search-Flags</span></span>           | <span data-ttu-id="ae603-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ae603-240">0x00000001</span></span>                        |
| <span data-ttu-id="ae603-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae603-241">System-Flags</span></span>           | <span data-ttu-id="ae603-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae603-242">0x00000010</span></span>                        |
| <span data-ttu-id="ae603-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae603-243">Classes used in</span></span>        | [<span data-ttu-id="ae603-244">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="ae603-244">**User**</span></span>](c-user.md)<br/> |



 

 





