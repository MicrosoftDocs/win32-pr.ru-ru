---
title: Атрибут Pek-List
description: Список ключей шифрования паролей.
ms.assetid: f214def2-5d16-4e04-b243-e5195dc7316f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Pek-List
- Схема AD атрибута Пеклист
topic_type:
- apiref
api_name:
- Pek-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cc5b718740fe20eabdca5bfa26509db7a9ed1b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893702"
---
# <a name="pek-list-attribute"></a><span data-ttu-id="9748d-105">Атрибут Pek-List</span><span class="sxs-lookup"><span data-stu-id="9748d-105">Pek-List attribute</span></span>

<span data-ttu-id="9748d-106">Список ключей шифрования паролей.</span><span class="sxs-lookup"><span data-stu-id="9748d-106">List of password encryption keys.</span></span>



| <span data-ttu-id="9748d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="9748d-107">Entry</span></span> | <span data-ttu-id="9748d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9748d-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="9748d-109">CN</span><span class="sxs-lookup"><span data-stu-id="9748d-109">CN</span></span>                | <span data-ttu-id="9748d-110">Pek-List</span><span class="sxs-lookup"><span data-stu-id="9748d-110">Pek-List</span></span>                                              |
| <span data-ttu-id="9748d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9748d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9748d-112">пеклист</span><span class="sxs-lookup"><span data-stu-id="9748d-112">pekList</span></span>                                               |
| <span data-ttu-id="9748d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="9748d-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="9748d-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9748d-114">Update Privilege</span></span>  | <span data-ttu-id="9748d-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="9748d-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="9748d-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9748d-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="9748d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9748d-117">Attribute-Id</span></span>      | <span data-ttu-id="9748d-118">1.2.840.113556.1.4.865</span><span class="sxs-lookup"><span data-stu-id="9748d-118">1.2.840.113556.1.4.865</span></span>                                |
| <span data-ttu-id="9748d-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9748d-119">System-Id-Guid</span></span>    | <span data-ttu-id="9748d-120">07383083-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9748d-120">07383083-91df-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="9748d-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9748d-121">Syntax</span></span>            | [<span data-ttu-id="9748d-122">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="9748d-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="9748d-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9748d-123">Implementations</span></span>

-   [<span data-ttu-id="9748d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9748d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9748d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9748d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9748d-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9748d-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9748d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9748d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9748d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9748d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9748d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9748d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9748d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9748d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9748d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9748d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9748d-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="9748d-132">Entry</span></span> | <span data-ttu-id="9748d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9748d-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9748d-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9748d-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9748d-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9748d-136">System-Only</span></span>            | <span data-ttu-id="9748d-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-137">False</span></span>                                        |
| <span data-ttu-id="9748d-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9748d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9748d-139">True</span><span class="sxs-lookup"><span data-stu-id="9748d-139">True</span></span>                                         |
| <span data-ttu-id="9748d-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9748d-140">Is Indexed</span></span>             | <span data-ttu-id="9748d-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-141">False</span></span>                                        |
| <span data-ttu-id="9748d-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9748d-142">In Global Catalog</span></span>      | <span data-ttu-id="9748d-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-143">False</span></span>                                        |
| <span data-ttu-id="9748d-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9748d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9748d-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9748d-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9748d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9748d-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9748d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9748d-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9748d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-148">Search-Flags</span></span>           | <span data-ttu-id="9748d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9748d-149">0x00000000</span></span>                                   |
| <span data-ttu-id="9748d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-150">System-Flags</span></span>           | <span data-ttu-id="9748d-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9748d-151">0x00000011</span></span>                                   |
| <span data-ttu-id="9748d-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9748d-152">Classes used in</span></span>        | [<span data-ttu-id="9748d-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="9748d-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9748d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9748d-154">Windows Server 2003</span></span>



| <span data-ttu-id="9748d-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="9748d-155">Entry</span></span> | <span data-ttu-id="9748d-156">Значение</span><span class="sxs-lookup"><span data-stu-id="9748d-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9748d-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9748d-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9748d-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9748d-159">System-Only</span></span>            | <span data-ttu-id="9748d-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-160">False</span></span>                                        |
| <span data-ttu-id="9748d-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9748d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9748d-162">True</span><span class="sxs-lookup"><span data-stu-id="9748d-162">True</span></span>                                         |
| <span data-ttu-id="9748d-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9748d-163">Is Indexed</span></span>             | <span data-ttu-id="9748d-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-164">False</span></span>                                        |
| <span data-ttu-id="9748d-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9748d-165">In Global Catalog</span></span>      | <span data-ttu-id="9748d-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-166">False</span></span>                                        |
| <span data-ttu-id="9748d-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9748d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9748d-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9748d-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9748d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9748d-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9748d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9748d-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9748d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-171">Search-Flags</span></span>           | <span data-ttu-id="9748d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9748d-172">0x00000000</span></span>                                   |
| <span data-ttu-id="9748d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-173">System-Flags</span></span>           | <span data-ttu-id="9748d-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9748d-174">0x00000011</span></span>                                   |
| <span data-ttu-id="9748d-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9748d-175">Classes used in</span></span>        | [<span data-ttu-id="9748d-176">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="9748d-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9748d-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="9748d-177">ADAM</span></span>



| <span data-ttu-id="9748d-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="9748d-178">Entry</span></span> | <span data-ttu-id="9748d-179">Значение</span><span class="sxs-lookup"><span data-stu-id="9748d-179">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9748d-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9748d-180">Link-Id</span></span>                | \-           |
| <span data-ttu-id="9748d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9748d-181">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="9748d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9748d-182">System-Only</span></span>            | <span data-ttu-id="9748d-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-183">False</span></span>        |
| <span data-ttu-id="9748d-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9748d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9748d-185">True</span><span class="sxs-lookup"><span data-stu-id="9748d-185">True</span></span>         |
| <span data-ttu-id="9748d-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9748d-186">Is Indexed</span></span>             | <span data-ttu-id="9748d-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-187">False</span></span>        |
| <span data-ttu-id="9748d-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9748d-188">In Global Catalog</span></span>      | <span data-ttu-id="9748d-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-189">False</span></span>        |
| <span data-ttu-id="9748d-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9748d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9748d-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9748d-191">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="9748d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9748d-192">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="9748d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9748d-193">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="9748d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-194">Search-Flags</span></span>           | <span data-ttu-id="9748d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9748d-195">0x00000000</span></span>   |
| <span data-ttu-id="9748d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-196">System-Flags</span></span>           | <span data-ttu-id="9748d-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9748d-197">0x00000011</span></span>   |
| <span data-ttu-id="9748d-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9748d-198">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9748d-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9748d-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9748d-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="9748d-200">Entry</span></span> | <span data-ttu-id="9748d-201">Значение</span><span class="sxs-lookup"><span data-stu-id="9748d-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9748d-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9748d-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9748d-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="9748d-204">System-Only</span></span>            | <span data-ttu-id="9748d-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-205">False</span></span>                                        |
| <span data-ttu-id="9748d-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9748d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="9748d-207">True</span><span class="sxs-lookup"><span data-stu-id="9748d-207">True</span></span>                                         |
| <span data-ttu-id="9748d-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9748d-208">Is Indexed</span></span>             | <span data-ttu-id="9748d-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-209">False</span></span>                                        |
| <span data-ttu-id="9748d-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9748d-210">In Global Catalog</span></span>      | <span data-ttu-id="9748d-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-211">False</span></span>                                        |
| <span data-ttu-id="9748d-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9748d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="9748d-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9748d-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9748d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9748d-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9748d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9748d-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9748d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-216">Search-Flags</span></span>           | <span data-ttu-id="9748d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9748d-217">0x00000000</span></span>                                   |
| <span data-ttu-id="9748d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-218">System-Flags</span></span>           | <span data-ttu-id="9748d-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9748d-219">0x00000011</span></span>                                   |
| <span data-ttu-id="9748d-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9748d-220">Classes used in</span></span>        | [<span data-ttu-id="9748d-221">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="9748d-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9748d-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9748d-222">Windows Server 2008</span></span>



| <span data-ttu-id="9748d-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="9748d-223">Entry</span></span> | <span data-ttu-id="9748d-224">Значение</span><span class="sxs-lookup"><span data-stu-id="9748d-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9748d-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9748d-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9748d-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="9748d-227">System-Only</span></span>            | <span data-ttu-id="9748d-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-228">False</span></span>                                        |
| <span data-ttu-id="9748d-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9748d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="9748d-230">True</span><span class="sxs-lookup"><span data-stu-id="9748d-230">True</span></span>                                         |
| <span data-ttu-id="9748d-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9748d-231">Is Indexed</span></span>             | <span data-ttu-id="9748d-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-232">False</span></span>                                        |
| <span data-ttu-id="9748d-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9748d-233">In Global Catalog</span></span>      | <span data-ttu-id="9748d-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-234">False</span></span>                                        |
| <span data-ttu-id="9748d-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9748d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="9748d-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9748d-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9748d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9748d-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9748d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9748d-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9748d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-239">Search-Flags</span></span>           | <span data-ttu-id="9748d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9748d-240">0x00000000</span></span>                                   |
| <span data-ttu-id="9748d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-241">System-Flags</span></span>           | <span data-ttu-id="9748d-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9748d-242">0x00000011</span></span>                                   |
| <span data-ttu-id="9748d-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9748d-243">Classes used in</span></span>        | [<span data-ttu-id="9748d-244">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="9748d-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9748d-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9748d-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9748d-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="9748d-246">Entry</span></span> | <span data-ttu-id="9748d-247">Значение</span><span class="sxs-lookup"><span data-stu-id="9748d-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9748d-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9748d-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9748d-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="9748d-250">System-Only</span></span>            | <span data-ttu-id="9748d-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-251">False</span></span>                                        |
| <span data-ttu-id="9748d-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9748d-252">Is-Single-Valued</span></span>       | <span data-ttu-id="9748d-253">True</span><span class="sxs-lookup"><span data-stu-id="9748d-253">True</span></span>                                         |
| <span data-ttu-id="9748d-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9748d-254">Is Indexed</span></span>             | <span data-ttu-id="9748d-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-255">False</span></span>                                        |
| <span data-ttu-id="9748d-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9748d-256">In Global Catalog</span></span>      | <span data-ttu-id="9748d-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-257">False</span></span>                                        |
| <span data-ttu-id="9748d-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9748d-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="9748d-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9748d-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9748d-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9748d-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9748d-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9748d-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9748d-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-262">Search-Flags</span></span>           | <span data-ttu-id="9748d-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9748d-263">0x00000000</span></span>                                   |
| <span data-ttu-id="9748d-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-264">System-Flags</span></span>           | <span data-ttu-id="9748d-265">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9748d-265">0x00000011</span></span>                                   |
| <span data-ttu-id="9748d-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9748d-266">Classes used in</span></span>        | [<span data-ttu-id="9748d-267">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="9748d-267">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9748d-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9748d-268">Windows Server 2012</span></span>



| <span data-ttu-id="9748d-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="9748d-269">Entry</span></span> | <span data-ttu-id="9748d-270">Значение</span><span class="sxs-lookup"><span data-stu-id="9748d-270">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="9748d-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9748d-271">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9748d-272">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="9748d-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="9748d-273">System-Only</span></span>            | <span data-ttu-id="9748d-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-274">False</span></span>                                        |
| <span data-ttu-id="9748d-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9748d-275">Is-Single-Valued</span></span>       | <span data-ttu-id="9748d-276">True</span><span class="sxs-lookup"><span data-stu-id="9748d-276">True</span></span>                                         |
| <span data-ttu-id="9748d-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9748d-277">Is Indexed</span></span>             | <span data-ttu-id="9748d-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-278">False</span></span>                                        |
| <span data-ttu-id="9748d-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9748d-279">In Global Catalog</span></span>      | <span data-ttu-id="9748d-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="9748d-280">False</span></span>                                        |
| <span data-ttu-id="9748d-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9748d-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="9748d-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9748d-282">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="9748d-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9748d-283">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="9748d-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9748d-284">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="9748d-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-285">Search-Flags</span></span>           | <span data-ttu-id="9748d-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9748d-286">0x00000000</span></span>                                   |
| <span data-ttu-id="9748d-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9748d-287">System-Flags</span></span>           | <span data-ttu-id="9748d-288">0x00000011</span><span class="sxs-lookup"><span data-stu-id="9748d-288">0x00000011</span></span>                                   |
| <span data-ttu-id="9748d-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9748d-289">Classes used in</span></span>        | [<span data-ttu-id="9748d-290">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="9748d-290">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





