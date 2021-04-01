---
title: Атрибут-маркер первичной группы
description: Вычисленный атрибут, используемый для получения списка членства в группе, например для пользователей домена. Полное членство таких групп не сохраняется явно для целей масштабирования.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута-маркера PRIMARY-Group
- Схема AD атрибута Примариграуптокен
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138518"
---
# <a name="primary-group-token-attribute"></a><span data-ttu-id="d482a-106">Атрибут-маркер первичной группы</span><span class="sxs-lookup"><span data-stu-id="d482a-106">Primary-Group-Token attribute</span></span>

<span data-ttu-id="d482a-107">Вычисленный атрибут, используемый для получения списка членства в группе, например для пользователей домена.</span><span class="sxs-lookup"><span data-stu-id="d482a-107">A computed attribute that is used in retrieving the membership list of a group, such as Domain Users.</span></span> <span data-ttu-id="d482a-108">Полное членство таких групп не сохраняется явно для целей масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d482a-108">The complete membership of such groups is not stored explicitly for scaling reasons.</span></span>



| <span data-ttu-id="d482a-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="d482a-109">Entry</span></span> | <span data-ttu-id="d482a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d482a-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="d482a-111">CN</span><span class="sxs-lookup"><span data-stu-id="d482a-111">CN</span></span>                | <span data-ttu-id="d482a-112">Маркер первичной группы</span><span class="sxs-lookup"><span data-stu-id="d482a-112">Primary-Group-Token</span></span>                        |
| <span data-ttu-id="d482a-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d482a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d482a-114">примариграуптокен</span><span class="sxs-lookup"><span data-stu-id="d482a-114">primaryGroupToken</span></span>                          |
| <span data-ttu-id="d482a-115">Размер</span><span class="sxs-lookup"><span data-stu-id="d482a-115">Size</span></span>              | <span data-ttu-id="d482a-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="d482a-116">4 bytes</span></span>                                    |
| <span data-ttu-id="d482a-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d482a-117">Update Privilege</span></span>  | <span data-ttu-id="d482a-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="d482a-118">This value is set by the system.</span></span>           |
| <span data-ttu-id="d482a-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d482a-119">Update Frequency</span></span>  | <span data-ttu-id="d482a-120">Каждый раз при изменении основной группы объектов.</span><span class="sxs-lookup"><span data-stu-id="d482a-120">Whenever an objects primary group changes.</span></span> |
| <span data-ttu-id="d482a-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d482a-121">Attribute-Id</span></span>      | <span data-ttu-id="d482a-122">1.2.840.113556.1.4.1412</span><span class="sxs-lookup"><span data-stu-id="d482a-122">1.2.840.113556.1.4.1412</span></span>                    |
| <span data-ttu-id="d482a-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d482a-123">System-Id-Guid</span></span>    | <span data-ttu-id="d482a-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span><span class="sxs-lookup"><span data-stu-id="d482a-124">c0ed8738-7efd-4481-84d9-66d2db8be369</span></span>       |
| <span data-ttu-id="d482a-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d482a-125">Syntax</span></span>            | [<span data-ttu-id="d482a-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="d482a-126">**Enumeration**</span></span>](s-enumeration.md)       |



## <a name="implementations"></a><span data-ttu-id="d482a-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d482a-127">Implementations</span></span>

-   [<span data-ttu-id="d482a-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d482a-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d482a-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d482a-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d482a-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d482a-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d482a-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d482a-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d482a-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d482a-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d482a-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d482a-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d482a-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d482a-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d482a-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d482a-135">Windows 2000 Server</span></span>



| <span data-ttu-id="d482a-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="d482a-136">Entry</span></span> | <span data-ttu-id="d482a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d482a-137">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d482a-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d482a-138">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d482a-139">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="d482a-140">System-Only</span></span>            | <span data-ttu-id="d482a-141">True</span><span class="sxs-lookup"><span data-stu-id="d482a-141">True</span></span>                                |
| <span data-ttu-id="d482a-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d482a-142">Is-Single-Valued</span></span>       | <span data-ttu-id="d482a-143">True</span><span class="sxs-lookup"><span data-stu-id="d482a-143">True</span></span>                                |
| <span data-ttu-id="d482a-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d482a-144">Is Indexed</span></span>             | <span data-ttu-id="d482a-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-145">False</span></span>                               |
| <span data-ttu-id="d482a-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d482a-146">In Global Catalog</span></span>      | <span data-ttu-id="d482a-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-147">False</span></span>                               |
| <span data-ttu-id="d482a-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d482a-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="d482a-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d482a-149">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d482a-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d482a-150">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d482a-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d482a-151">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d482a-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-152">Search-Flags</span></span>           | <span data-ttu-id="d482a-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d482a-153">0x00000000</span></span>                          |
| <span data-ttu-id="d482a-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-154">System-Flags</span></span>           | <span data-ttu-id="d482a-155">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d482a-155">0x00000014</span></span>                          |
| <span data-ttu-id="d482a-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d482a-156">Classes used in</span></span>        | [<span data-ttu-id="d482a-157">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d482a-157">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d482a-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d482a-158">Windows Server 2003</span></span>



| <span data-ttu-id="d482a-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="d482a-159">Entry</span></span> | <span data-ttu-id="d482a-160">Значение</span><span class="sxs-lookup"><span data-stu-id="d482a-160">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d482a-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d482a-161">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d482a-162">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="d482a-163">System-Only</span></span>            | <span data-ttu-id="d482a-164">True</span><span class="sxs-lookup"><span data-stu-id="d482a-164">True</span></span>                                |
| <span data-ttu-id="d482a-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d482a-165">Is-Single-Valued</span></span>       | <span data-ttu-id="d482a-166">True</span><span class="sxs-lookup"><span data-stu-id="d482a-166">True</span></span>                                |
| <span data-ttu-id="d482a-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d482a-167">Is Indexed</span></span>             | <span data-ttu-id="d482a-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-168">False</span></span>                               |
| <span data-ttu-id="d482a-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d482a-169">In Global Catalog</span></span>      | <span data-ttu-id="d482a-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-170">False</span></span>                               |
| <span data-ttu-id="d482a-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d482a-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="d482a-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d482a-172">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d482a-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d482a-173">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d482a-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d482a-174">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d482a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-175">Search-Flags</span></span>           | <span data-ttu-id="d482a-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d482a-176">0x00000000</span></span>                          |
| <span data-ttu-id="d482a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-177">System-Flags</span></span>           | <span data-ttu-id="d482a-178">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d482a-178">0x00000014</span></span>                          |
| <span data-ttu-id="d482a-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d482a-179">Classes used in</span></span>        | [<span data-ttu-id="d482a-180">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d482a-180">**Group**</span></span>](c-group.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d482a-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="d482a-181">ADAM</span></span>



| <span data-ttu-id="d482a-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="d482a-182">Entry</span></span> | <span data-ttu-id="d482a-183">Значение</span><span class="sxs-lookup"><span data-stu-id="d482a-183">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d482a-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d482a-184">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d482a-185">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="d482a-186">System-Only</span></span>            | <span data-ttu-id="d482a-187">True</span><span class="sxs-lookup"><span data-stu-id="d482a-187">True</span></span>                                |
| <span data-ttu-id="d482a-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d482a-188">Is-Single-Valued</span></span>       | <span data-ttu-id="d482a-189">True</span><span class="sxs-lookup"><span data-stu-id="d482a-189">True</span></span>                                |
| <span data-ttu-id="d482a-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d482a-190">Is Indexed</span></span>             | <span data-ttu-id="d482a-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-191">False</span></span>                               |
| <span data-ttu-id="d482a-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d482a-192">In Global Catalog</span></span>      | <span data-ttu-id="d482a-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-193">False</span></span>                               |
| <span data-ttu-id="d482a-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d482a-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="d482a-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d482a-195">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d482a-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d482a-196">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d482a-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d482a-197">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d482a-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-198">Search-Flags</span></span>           | <span data-ttu-id="d482a-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d482a-199">0x00000000</span></span>                          |
| <span data-ttu-id="d482a-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-200">System-Flags</span></span>           | <span data-ttu-id="d482a-201">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d482a-201">0x00000014</span></span>                          |
| <span data-ttu-id="d482a-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d482a-202">Classes used in</span></span>        | [<span data-ttu-id="d482a-203">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d482a-203">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d482a-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d482a-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d482a-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="d482a-205">Entry</span></span> | <span data-ttu-id="d482a-206">Значение</span><span class="sxs-lookup"><span data-stu-id="d482a-206">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d482a-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d482a-207">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d482a-208">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="d482a-209">System-Only</span></span>            | <span data-ttu-id="d482a-210">True</span><span class="sxs-lookup"><span data-stu-id="d482a-210">True</span></span>                                |
| <span data-ttu-id="d482a-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d482a-211">Is-Single-Valued</span></span>       | <span data-ttu-id="d482a-212">True</span><span class="sxs-lookup"><span data-stu-id="d482a-212">True</span></span>                                |
| <span data-ttu-id="d482a-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d482a-213">Is Indexed</span></span>             | <span data-ttu-id="d482a-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-214">False</span></span>                               |
| <span data-ttu-id="d482a-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d482a-215">In Global Catalog</span></span>      | <span data-ttu-id="d482a-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-216">False</span></span>                               |
| <span data-ttu-id="d482a-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d482a-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="d482a-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d482a-218">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d482a-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d482a-219">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d482a-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d482a-220">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d482a-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-221">Search-Flags</span></span>           | <span data-ttu-id="d482a-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d482a-222">0x00000000</span></span>                          |
| <span data-ttu-id="d482a-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-223">System-Flags</span></span>           | <span data-ttu-id="d482a-224">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d482a-224">0x00000014</span></span>                          |
| <span data-ttu-id="d482a-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d482a-225">Classes used in</span></span>        | [<span data-ttu-id="d482a-226">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d482a-226">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d482a-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d482a-227">Windows Server 2008</span></span>



| <span data-ttu-id="d482a-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="d482a-228">Entry</span></span> | <span data-ttu-id="d482a-229">Значение</span><span class="sxs-lookup"><span data-stu-id="d482a-229">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d482a-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d482a-230">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d482a-231">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="d482a-232">System-Only</span></span>            | <span data-ttu-id="d482a-233">True</span><span class="sxs-lookup"><span data-stu-id="d482a-233">True</span></span>                                |
| <span data-ttu-id="d482a-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d482a-234">Is-Single-Valued</span></span>       | <span data-ttu-id="d482a-235">True</span><span class="sxs-lookup"><span data-stu-id="d482a-235">True</span></span>                                |
| <span data-ttu-id="d482a-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d482a-236">Is Indexed</span></span>             | <span data-ttu-id="d482a-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-237">False</span></span>                               |
| <span data-ttu-id="d482a-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d482a-238">In Global Catalog</span></span>      | <span data-ttu-id="d482a-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-239">False</span></span>                               |
| <span data-ttu-id="d482a-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d482a-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="d482a-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d482a-241">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d482a-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d482a-242">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d482a-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d482a-243">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d482a-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-244">Search-Flags</span></span>           | <span data-ttu-id="d482a-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d482a-245">0x00000000</span></span>                          |
| <span data-ttu-id="d482a-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-246">System-Flags</span></span>           | <span data-ttu-id="d482a-247">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d482a-247">0x00000014</span></span>                          |
| <span data-ttu-id="d482a-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d482a-248">Classes used in</span></span>        | [<span data-ttu-id="d482a-249">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d482a-249">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d482a-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d482a-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d482a-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="d482a-251">Entry</span></span> | <span data-ttu-id="d482a-252">Значение</span><span class="sxs-lookup"><span data-stu-id="d482a-252">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d482a-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d482a-253">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d482a-254">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="d482a-255">System-Only</span></span>            | <span data-ttu-id="d482a-256">True</span><span class="sxs-lookup"><span data-stu-id="d482a-256">True</span></span>                                |
| <span data-ttu-id="d482a-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d482a-257">Is-Single-Valued</span></span>       | <span data-ttu-id="d482a-258">True</span><span class="sxs-lookup"><span data-stu-id="d482a-258">True</span></span>                                |
| <span data-ttu-id="d482a-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d482a-259">Is Indexed</span></span>             | <span data-ttu-id="d482a-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-260">False</span></span>                               |
| <span data-ttu-id="d482a-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d482a-261">In Global Catalog</span></span>      | <span data-ttu-id="d482a-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-262">False</span></span>                               |
| <span data-ttu-id="d482a-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d482a-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="d482a-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d482a-264">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d482a-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d482a-265">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d482a-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d482a-266">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d482a-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-267">Search-Flags</span></span>           | <span data-ttu-id="d482a-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d482a-268">0x00000000</span></span>                          |
| <span data-ttu-id="d482a-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-269">System-Flags</span></span>           | <span data-ttu-id="d482a-270">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d482a-270">0x00000014</span></span>                          |
| <span data-ttu-id="d482a-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d482a-271">Classes used in</span></span>        | [<span data-ttu-id="d482a-272">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d482a-272">**Group**</span></span>](c-group.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d482a-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d482a-273">Windows Server 2012</span></span>



| <span data-ttu-id="d482a-274">Ввод</span><span class="sxs-lookup"><span data-stu-id="d482a-274">Entry</span></span> | <span data-ttu-id="d482a-275">Значение</span><span class="sxs-lookup"><span data-stu-id="d482a-275">Value</span></span> |
|------------------------|-------------------------------------|
| <span data-ttu-id="d482a-276">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d482a-276">Link-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d482a-277">MAPI-Id</span></span>                | \-                                  |
| <span data-ttu-id="d482a-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="d482a-278">System-Only</span></span>            | <span data-ttu-id="d482a-279">True</span><span class="sxs-lookup"><span data-stu-id="d482a-279">True</span></span>                                |
| <span data-ttu-id="d482a-280">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d482a-280">Is-Single-Valued</span></span>       | <span data-ttu-id="d482a-281">True</span><span class="sxs-lookup"><span data-stu-id="d482a-281">True</span></span>                                |
| <span data-ttu-id="d482a-282">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d482a-282">Is Indexed</span></span>             | <span data-ttu-id="d482a-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-283">False</span></span>                               |
| <span data-ttu-id="d482a-284">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d482a-284">In Global Catalog</span></span>      | <span data-ttu-id="d482a-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="d482a-285">False</span></span>                               |
| <span data-ttu-id="d482a-286">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d482a-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="d482a-287">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d482a-287">O:BAG:BAD:S:</span></span>                        |
| <span data-ttu-id="d482a-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d482a-288">Range-Lower</span></span>            | \-                                  |
| <span data-ttu-id="d482a-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d482a-289">Range-Upper</span></span>            | \-                                  |
| <span data-ttu-id="d482a-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-290">Search-Flags</span></span>           | <span data-ttu-id="d482a-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d482a-291">0x00000000</span></span>                          |
| <span data-ttu-id="d482a-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d482a-292">System-Flags</span></span>           | <span data-ttu-id="d482a-293">0x00000014</span><span class="sxs-lookup"><span data-stu-id="d482a-293">0x00000014</span></span>                          |
| <span data-ttu-id="d482a-294">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d482a-294">Classes used in</span></span>        | [<span data-ttu-id="d482a-295">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d482a-295">**Group**</span></span>](c-group.md)<br/> |



 

 





