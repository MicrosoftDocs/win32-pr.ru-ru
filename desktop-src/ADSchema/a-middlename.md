---
title: Атрибут Other-Name
description: Дополнительные имена для пользователя. Например, отчество, патронимик, матронимик или другие.
ms.assetid: 539de593-e879-4b4a-bf75-c022f53e80de
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Other-Name
- Схема AD атрибута middleName
topic_type:
- apiref
api_name:
- Other-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e62a9555d77d95d5e30ebacaec5950a19c318b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138695"
---
# <a name="other-name-attribute"></a><span data-ttu-id="ec41c-106">Атрибут Other-Name</span><span class="sxs-lookup"><span data-stu-id="ec41c-106">Other-Name attribute</span></span>

<span data-ttu-id="ec41c-107">Дополнительные имена для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ec41c-107">Additional names for a user.</span></span> <span data-ttu-id="ec41c-108">Например, отчество, патронимик, матронимик или другие.</span><span class="sxs-lookup"><span data-stu-id="ec41c-108">For example, middle name, patronymic, matronymic, or others.</span></span>



| <span data-ttu-id="ec41c-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec41c-109">Entry</span></span> | <span data-ttu-id="ec41c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ec41c-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ec41c-111">CN</span><span class="sxs-lookup"><span data-stu-id="ec41c-111">CN</span></span>                | <span data-ttu-id="ec41c-112">Other-Name</span><span class="sxs-lookup"><span data-stu-id="ec41c-112">Other-Name</span></span>                                  |
| <span data-ttu-id="ec41c-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ec41c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ec41c-114">middleName</span><span class="sxs-lookup"><span data-stu-id="ec41c-114">middleName</span></span>                                  |
| <span data-ttu-id="ec41c-115">Размер</span><span class="sxs-lookup"><span data-stu-id="ec41c-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="ec41c-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ec41c-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="ec41c-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ec41c-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ec41c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec41c-118">Attribute-Id</span></span>      | <span data-ttu-id="ec41c-119">2.16.840.1.113730.3.1.34</span><span class="sxs-lookup"><span data-stu-id="ec41c-119">2.16.840.1.113730.3.1.34</span></span>                    |
| <span data-ttu-id="ec41c-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ec41c-120">System-Id-Guid</span></span>    | <span data-ttu-id="ec41c-121">bf9679f2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ec41c-121">bf9679f2-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="ec41c-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec41c-122">Syntax</span></span>            | [<span data-ttu-id="ec41c-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="ec41c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ec41c-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ec41c-124">Implementations</span></span>

-   [<span data-ttu-id="ec41c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec41c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec41c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec41c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec41c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec41c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec41c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec41c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec41c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec41c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec41c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec41c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec41c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec41c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ec41c-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec41c-132">Entry</span></span> | <span data-ttu-id="ec41c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ec41c-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ec41c-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec41c-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec41c-135">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec41c-136">System-Only</span></span>            | <span data-ttu-id="ec41c-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-137">False</span></span>                                                              |
| <span data-ttu-id="ec41c-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec41c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ec41c-139">True</span><span class="sxs-lookup"><span data-stu-id="ec41c-139">True</span></span>                                                               |
| <span data-ttu-id="ec41c-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec41c-140">Is Indexed</span></span>             | <span data-ttu-id="ec41c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-141">False</span></span>                                                              |
| <span data-ttu-id="ec41c-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec41c-142">In Global Catalog</span></span>      | <span data-ttu-id="ec41c-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-143">False</span></span>                                                              |
| <span data-ttu-id="ec41c-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec41c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec41c-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec41c-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ec41c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec41c-146">Range-Lower</span></span>            | <span data-ttu-id="ec41c-147">0</span><span class="sxs-lookup"><span data-stu-id="ec41c-147">0</span></span>                                                                  |
| <span data-ttu-id="ec41c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec41c-148">Range-Upper</span></span>            | <span data-ttu-id="ec41c-149">64</span><span class="sxs-lookup"><span data-stu-id="ec41c-149">64</span></span>                                                                 |
| <span data-ttu-id="ec41c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-150">Search-Flags</span></span>           | <span data-ttu-id="ec41c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec41c-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="ec41c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-152">System-Flags</span></span>           | <span data-ttu-id="ec41c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec41c-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="ec41c-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec41c-154">Classes used in</span></span>        | [<span data-ttu-id="ec41c-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ec41c-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec41c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec41c-156">Windows Server 2003</span></span>



| <span data-ttu-id="ec41c-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec41c-157">Entry</span></span> | <span data-ttu-id="ec41c-158">Значение</span><span class="sxs-lookup"><span data-stu-id="ec41c-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ec41c-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec41c-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec41c-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec41c-161">System-Only</span></span>            | <span data-ttu-id="ec41c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-162">False</span></span>                                                              |
| <span data-ttu-id="ec41c-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec41c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ec41c-164">True</span><span class="sxs-lookup"><span data-stu-id="ec41c-164">True</span></span>                                                               |
| <span data-ttu-id="ec41c-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec41c-165">Is Indexed</span></span>             | <span data-ttu-id="ec41c-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-166">False</span></span>                                                              |
| <span data-ttu-id="ec41c-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec41c-167">In Global Catalog</span></span>      | <span data-ttu-id="ec41c-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-168">False</span></span>                                                              |
| <span data-ttu-id="ec41c-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec41c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec41c-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec41c-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ec41c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec41c-171">Range-Lower</span></span>            | <span data-ttu-id="ec41c-172">0</span><span class="sxs-lookup"><span data-stu-id="ec41c-172">0</span></span>                                                                  |
| <span data-ttu-id="ec41c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec41c-173">Range-Upper</span></span>            | <span data-ttu-id="ec41c-174">64</span><span class="sxs-lookup"><span data-stu-id="ec41c-174">64</span></span>                                                                 |
| <span data-ttu-id="ec41c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-175">Search-Flags</span></span>           | <span data-ttu-id="ec41c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec41c-176">0x00000000</span></span>                                                         |
| <span data-ttu-id="ec41c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-177">System-Flags</span></span>           | <span data-ttu-id="ec41c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec41c-178">0x00000010</span></span>                                                         |
| <span data-ttu-id="ec41c-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec41c-179">Classes used in</span></span>        | [<span data-ttu-id="ec41c-180">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ec41c-180">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec41c-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec41c-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec41c-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec41c-182">Entry</span></span> | <span data-ttu-id="ec41c-183">Значение</span><span class="sxs-lookup"><span data-stu-id="ec41c-183">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ec41c-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec41c-184">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec41c-185">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec41c-186">System-Only</span></span>            | <span data-ttu-id="ec41c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-187">False</span></span>                                                              |
| <span data-ttu-id="ec41c-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec41c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ec41c-189">True</span><span class="sxs-lookup"><span data-stu-id="ec41c-189">True</span></span>                                                               |
| <span data-ttu-id="ec41c-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec41c-190">Is Indexed</span></span>             | <span data-ttu-id="ec41c-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-191">False</span></span>                                                              |
| <span data-ttu-id="ec41c-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec41c-192">In Global Catalog</span></span>      | <span data-ttu-id="ec41c-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-193">False</span></span>                                                              |
| <span data-ttu-id="ec41c-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec41c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec41c-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec41c-195">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ec41c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec41c-196">Range-Lower</span></span>            | <span data-ttu-id="ec41c-197">0</span><span class="sxs-lookup"><span data-stu-id="ec41c-197">0</span></span>                                                                  |
| <span data-ttu-id="ec41c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec41c-198">Range-Upper</span></span>            | <span data-ttu-id="ec41c-199">64</span><span class="sxs-lookup"><span data-stu-id="ec41c-199">64</span></span>                                                                 |
| <span data-ttu-id="ec41c-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-200">Search-Flags</span></span>           | <span data-ttu-id="ec41c-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec41c-201">0x00000000</span></span>                                                         |
| <span data-ttu-id="ec41c-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-202">System-Flags</span></span>           | <span data-ttu-id="ec41c-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec41c-203">0x00000010</span></span>                                                         |
| <span data-ttu-id="ec41c-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec41c-204">Classes used in</span></span>        | [<span data-ttu-id="ec41c-205">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ec41c-205">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec41c-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec41c-206">Windows Server 2008</span></span>



| <span data-ttu-id="ec41c-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec41c-207">Entry</span></span> | <span data-ttu-id="ec41c-208">Значение</span><span class="sxs-lookup"><span data-stu-id="ec41c-208">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ec41c-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec41c-209">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec41c-210">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec41c-211">System-Only</span></span>            | <span data-ttu-id="ec41c-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-212">False</span></span>                                                              |
| <span data-ttu-id="ec41c-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec41c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="ec41c-214">True</span><span class="sxs-lookup"><span data-stu-id="ec41c-214">True</span></span>                                                               |
| <span data-ttu-id="ec41c-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec41c-215">Is Indexed</span></span>             | <span data-ttu-id="ec41c-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-216">False</span></span>                                                              |
| <span data-ttu-id="ec41c-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec41c-217">In Global Catalog</span></span>      | <span data-ttu-id="ec41c-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-218">False</span></span>                                                              |
| <span data-ttu-id="ec41c-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec41c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec41c-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec41c-220">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ec41c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec41c-221">Range-Lower</span></span>            | <span data-ttu-id="ec41c-222">0</span><span class="sxs-lookup"><span data-stu-id="ec41c-222">0</span></span>                                                                  |
| <span data-ttu-id="ec41c-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec41c-223">Range-Upper</span></span>            | <span data-ttu-id="ec41c-224">64</span><span class="sxs-lookup"><span data-stu-id="ec41c-224">64</span></span>                                                                 |
| <span data-ttu-id="ec41c-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-225">Search-Flags</span></span>           | <span data-ttu-id="ec41c-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec41c-226">0x00000000</span></span>                                                         |
| <span data-ttu-id="ec41c-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-227">System-Flags</span></span>           | <span data-ttu-id="ec41c-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec41c-228">0x00000010</span></span>                                                         |
| <span data-ttu-id="ec41c-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec41c-229">Classes used in</span></span>        | [<span data-ttu-id="ec41c-230">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ec41c-230">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec41c-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec41c-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec41c-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec41c-232">Entry</span></span> | <span data-ttu-id="ec41c-233">Значение</span><span class="sxs-lookup"><span data-stu-id="ec41c-233">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ec41c-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec41c-234">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec41c-235">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec41c-236">System-Only</span></span>            | <span data-ttu-id="ec41c-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-237">False</span></span>                                                              |
| <span data-ttu-id="ec41c-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec41c-238">Is-Single-Valued</span></span>       | <span data-ttu-id="ec41c-239">True</span><span class="sxs-lookup"><span data-stu-id="ec41c-239">True</span></span>                                                               |
| <span data-ttu-id="ec41c-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec41c-240">Is Indexed</span></span>             | <span data-ttu-id="ec41c-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-241">False</span></span>                                                              |
| <span data-ttu-id="ec41c-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec41c-242">In Global Catalog</span></span>      | <span data-ttu-id="ec41c-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-243">False</span></span>                                                              |
| <span data-ttu-id="ec41c-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec41c-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec41c-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec41c-245">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ec41c-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec41c-246">Range-Lower</span></span>            | <span data-ttu-id="ec41c-247">0</span><span class="sxs-lookup"><span data-stu-id="ec41c-247">0</span></span>                                                                  |
| <span data-ttu-id="ec41c-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec41c-248">Range-Upper</span></span>            | <span data-ttu-id="ec41c-249">64</span><span class="sxs-lookup"><span data-stu-id="ec41c-249">64</span></span>                                                                 |
| <span data-ttu-id="ec41c-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-250">Search-Flags</span></span>           | <span data-ttu-id="ec41c-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec41c-251">0x00000000</span></span>                                                         |
| <span data-ttu-id="ec41c-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-252">System-Flags</span></span>           | <span data-ttu-id="ec41c-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec41c-253">0x00000010</span></span>                                                         |
| <span data-ttu-id="ec41c-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec41c-254">Classes used in</span></span>        | [<span data-ttu-id="ec41c-255">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ec41c-255">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec41c-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec41c-256">Windows Server 2012</span></span>



| <span data-ttu-id="ec41c-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec41c-257">Entry</span></span> | <span data-ttu-id="ec41c-258">Значение</span><span class="sxs-lookup"><span data-stu-id="ec41c-258">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ec41c-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec41c-259">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec41c-260">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ec41c-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec41c-261">System-Only</span></span>            | <span data-ttu-id="ec41c-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-262">False</span></span>                                                              |
| <span data-ttu-id="ec41c-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec41c-263">Is-Single-Valued</span></span>       | <span data-ttu-id="ec41c-264">True</span><span class="sxs-lookup"><span data-stu-id="ec41c-264">True</span></span>                                                               |
| <span data-ttu-id="ec41c-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec41c-265">Is Indexed</span></span>             | <span data-ttu-id="ec41c-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-266">False</span></span>                                                              |
| <span data-ttu-id="ec41c-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec41c-267">In Global Catalog</span></span>      | <span data-ttu-id="ec41c-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec41c-268">False</span></span>                                                              |
| <span data-ttu-id="ec41c-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec41c-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec41c-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec41c-270">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ec41c-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec41c-271">Range-Lower</span></span>            | <span data-ttu-id="ec41c-272">0</span><span class="sxs-lookup"><span data-stu-id="ec41c-272">0</span></span>                                                                  |
| <span data-ttu-id="ec41c-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec41c-273">Range-Upper</span></span>            | <span data-ttu-id="ec41c-274">64</span><span class="sxs-lookup"><span data-stu-id="ec41c-274">64</span></span>                                                                 |
| <span data-ttu-id="ec41c-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-275">Search-Flags</span></span>           | <span data-ttu-id="ec41c-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec41c-276">0x00000000</span></span>                                                         |
| <span data-ttu-id="ec41c-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec41c-277">System-Flags</span></span>           | <span data-ttu-id="ec41c-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec41c-278">0x00000010</span></span>                                                         |
| <span data-ttu-id="ec41c-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec41c-279">Classes used in</span></span>        | [<span data-ttu-id="ec41c-280">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ec41c-280">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





