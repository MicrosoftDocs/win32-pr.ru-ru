---
title: Атрибут FSMO-Role-Owner
description: Гибкое Single-Master операция — различающееся имя контроллера домена, в котором можно изменить схему.
ms.assetid: 8eb28524-4bbf-453c-89ab-864ef94b0781
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута FSMO для владельца роли
- Схема AD атрибута Фсморолеовнер
topic_type:
- apiref
api_name:
- FSMO-Role-Owner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4439e5ee10fba11db831024d6b1958b75cd81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893609"
---
# <a name="fsmo-role-owner-attribute"></a><span data-ttu-id="d339e-105">Атрибут FSMO-Role-Owner</span><span class="sxs-lookup"><span data-stu-id="d339e-105">FSMO-Role-Owner attribute</span></span>

<span data-ttu-id="d339e-106">Гибкая операция Single-Master: различающееся имя контроллера домена, в котором можно изменить схему.</span><span class="sxs-lookup"><span data-stu-id="d339e-106">Flexible Single-Master Operation: The distinguished name of the DC where the schema can be modified.</span></span>



| <span data-ttu-id="d339e-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d339e-107">Entry</span></span> | <span data-ttu-id="d339e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d339e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d339e-109">CN</span><span class="sxs-lookup"><span data-stu-id="d339e-109">CN</span></span>                | <span data-ttu-id="d339e-110">FSMO-Role-Owner</span><span class="sxs-lookup"><span data-stu-id="d339e-110">FSMO-Role-Owner</span></span>                         |
| <span data-ttu-id="d339e-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d339e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d339e-112">фсморолеовнер</span><span class="sxs-lookup"><span data-stu-id="d339e-112">fSMORoleOwner</span></span>                           |
| <span data-ttu-id="d339e-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d339e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="d339e-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d339e-114">Update Privilege</span></span>  | <span data-ttu-id="d339e-115">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="d339e-115">Schema administrator</span></span>                    |
| <span data-ttu-id="d339e-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d339e-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="d339e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d339e-117">Attribute-Id</span></span>      | <span data-ttu-id="d339e-118">1.2.840.113556.1.4.369</span><span class="sxs-lookup"><span data-stu-id="d339e-118">1.2.840.113556.1.4.369</span></span>                  |
| <span data-ttu-id="d339e-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d339e-119">System-Id-Guid</span></span>    | <span data-ttu-id="d339e-120">66171887-8f3c-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="d339e-120">66171887-8f3c-11d0-afda-00c04fd930c9</span></span>    |
| <span data-ttu-id="d339e-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d339e-121">Syntax</span></span>            | [<span data-ttu-id="d339e-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d339e-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d339e-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d339e-123">Implementations</span></span>

-   [<span data-ttu-id="d339e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d339e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d339e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d339e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d339e-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d339e-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d339e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d339e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d339e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d339e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d339e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d339e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d339e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d339e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d339e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d339e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d339e-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="d339e-132">Entry</span></span> | <span data-ttu-id="d339e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d339e-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d339e-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d339e-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d339e-135">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d339e-136">System-Only</span></span>            | <span data-ttu-id="d339e-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-137">False</span></span>                           |
| <span data-ttu-id="d339e-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d339e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d339e-139">True</span><span class="sxs-lookup"><span data-stu-id="d339e-139">True</span></span>                            |
| <span data-ttu-id="d339e-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d339e-140">Is Indexed</span></span>             | <span data-ttu-id="d339e-141">True</span><span class="sxs-lookup"><span data-stu-id="d339e-141">True</span></span>                            |
| <span data-ttu-id="d339e-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d339e-142">In Global Catalog</span></span>      | <span data-ttu-id="d339e-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-143">False</span></span>                           |
| <span data-ttu-id="d339e-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d339e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d339e-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d339e-145">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d339e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d339e-146">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d339e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d339e-147">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d339e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-148">Search-Flags</span></span>           | <span data-ttu-id="d339e-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d339e-149">0x00000001</span></span>                      |
| <span data-ttu-id="d339e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-150">System-Flags</span></span>           | <span data-ttu-id="d339e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d339e-151">0x00000010</span></span>                      |
| <span data-ttu-id="d339e-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d339e-152">Classes used in</span></span>        | [<span data-ttu-id="d339e-153">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d339e-153">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d339e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d339e-154">Windows Server 2003</span></span>



| <span data-ttu-id="d339e-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="d339e-155">Entry</span></span> | <span data-ttu-id="d339e-156">Значение</span><span class="sxs-lookup"><span data-stu-id="d339e-156">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d339e-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d339e-157">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d339e-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d339e-159">System-Only</span></span>            | <span data-ttu-id="d339e-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-160">False</span></span>                           |
| <span data-ttu-id="d339e-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d339e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d339e-162">True</span><span class="sxs-lookup"><span data-stu-id="d339e-162">True</span></span>                            |
| <span data-ttu-id="d339e-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d339e-163">Is Indexed</span></span>             | <span data-ttu-id="d339e-164">True</span><span class="sxs-lookup"><span data-stu-id="d339e-164">True</span></span>                            |
| <span data-ttu-id="d339e-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d339e-165">In Global Catalog</span></span>      | <span data-ttu-id="d339e-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-166">False</span></span>                           |
| <span data-ttu-id="d339e-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d339e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d339e-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d339e-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d339e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d339e-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d339e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d339e-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d339e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-171">Search-Flags</span></span>           | <span data-ttu-id="d339e-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d339e-172">0x00000001</span></span>                      |
| <span data-ttu-id="d339e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-173">System-Flags</span></span>           | <span data-ttu-id="d339e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d339e-174">0x00000010</span></span>                      |
| <span data-ttu-id="d339e-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d339e-175">Classes used in</span></span>        | [<span data-ttu-id="d339e-176">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d339e-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d339e-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="d339e-177">ADAM</span></span>



| <span data-ttu-id="d339e-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="d339e-178">Entry</span></span> | <span data-ttu-id="d339e-179">Значение</span><span class="sxs-lookup"><span data-stu-id="d339e-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d339e-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d339e-180">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d339e-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d339e-182">System-Only</span></span>            | <span data-ttu-id="d339e-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-183">False</span></span>                           |
| <span data-ttu-id="d339e-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d339e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d339e-185">True</span><span class="sxs-lookup"><span data-stu-id="d339e-185">True</span></span>                            |
| <span data-ttu-id="d339e-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d339e-186">Is Indexed</span></span>             | <span data-ttu-id="d339e-187">True</span><span class="sxs-lookup"><span data-stu-id="d339e-187">True</span></span>                            |
| <span data-ttu-id="d339e-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d339e-188">In Global Catalog</span></span>      | <span data-ttu-id="d339e-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-189">False</span></span>                           |
| <span data-ttu-id="d339e-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d339e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d339e-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d339e-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d339e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d339e-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d339e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d339e-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d339e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-194">Search-Flags</span></span>           | <span data-ttu-id="d339e-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d339e-195">0x00000001</span></span>                      |
| <span data-ttu-id="d339e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-196">System-Flags</span></span>           | <span data-ttu-id="d339e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d339e-197">0x00000010</span></span>                      |
| <span data-ttu-id="d339e-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d339e-198">Classes used in</span></span>        | [<span data-ttu-id="d339e-199">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d339e-199">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d339e-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d339e-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d339e-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="d339e-201">Entry</span></span> | <span data-ttu-id="d339e-202">Значение</span><span class="sxs-lookup"><span data-stu-id="d339e-202">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d339e-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d339e-203">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d339e-204">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d339e-205">System-Only</span></span>            | <span data-ttu-id="d339e-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-206">False</span></span>                           |
| <span data-ttu-id="d339e-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d339e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d339e-208">True</span><span class="sxs-lookup"><span data-stu-id="d339e-208">True</span></span>                            |
| <span data-ttu-id="d339e-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d339e-209">Is Indexed</span></span>             | <span data-ttu-id="d339e-210">True</span><span class="sxs-lookup"><span data-stu-id="d339e-210">True</span></span>                            |
| <span data-ttu-id="d339e-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d339e-211">In Global Catalog</span></span>      | <span data-ttu-id="d339e-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-212">False</span></span>                           |
| <span data-ttu-id="d339e-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d339e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d339e-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d339e-214">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d339e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d339e-215">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d339e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d339e-216">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d339e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-217">Search-Flags</span></span>           | <span data-ttu-id="d339e-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d339e-218">0x00000001</span></span>                      |
| <span data-ttu-id="d339e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-219">System-Flags</span></span>           | <span data-ttu-id="d339e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d339e-220">0x00000010</span></span>                      |
| <span data-ttu-id="d339e-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d339e-221">Classes used in</span></span>        | [<span data-ttu-id="d339e-222">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d339e-222">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d339e-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d339e-223">Windows Server 2008</span></span>



| <span data-ttu-id="d339e-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="d339e-224">Entry</span></span> | <span data-ttu-id="d339e-225">Значение</span><span class="sxs-lookup"><span data-stu-id="d339e-225">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d339e-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d339e-226">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d339e-227">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d339e-228">System-Only</span></span>            | <span data-ttu-id="d339e-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-229">False</span></span>                           |
| <span data-ttu-id="d339e-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d339e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d339e-231">True</span><span class="sxs-lookup"><span data-stu-id="d339e-231">True</span></span>                            |
| <span data-ttu-id="d339e-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d339e-232">Is Indexed</span></span>             | <span data-ttu-id="d339e-233">True</span><span class="sxs-lookup"><span data-stu-id="d339e-233">True</span></span>                            |
| <span data-ttu-id="d339e-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d339e-234">In Global Catalog</span></span>      | <span data-ttu-id="d339e-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-235">False</span></span>                           |
| <span data-ttu-id="d339e-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d339e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d339e-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d339e-237">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d339e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d339e-238">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d339e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d339e-239">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d339e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-240">Search-Flags</span></span>           | <span data-ttu-id="d339e-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d339e-241">0x00000001</span></span>                      |
| <span data-ttu-id="d339e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-242">System-Flags</span></span>           | <span data-ttu-id="d339e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d339e-243">0x00000010</span></span>                      |
| <span data-ttu-id="d339e-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d339e-244">Classes used in</span></span>        | [<span data-ttu-id="d339e-245">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d339e-245">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d339e-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d339e-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d339e-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="d339e-247">Entry</span></span> | <span data-ttu-id="d339e-248">Значение</span><span class="sxs-lookup"><span data-stu-id="d339e-248">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d339e-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d339e-249">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d339e-250">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d339e-251">System-Only</span></span>            | <span data-ttu-id="d339e-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-252">False</span></span>                           |
| <span data-ttu-id="d339e-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d339e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d339e-254">True</span><span class="sxs-lookup"><span data-stu-id="d339e-254">True</span></span>                            |
| <span data-ttu-id="d339e-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d339e-255">Is Indexed</span></span>             | <span data-ttu-id="d339e-256">True</span><span class="sxs-lookup"><span data-stu-id="d339e-256">True</span></span>                            |
| <span data-ttu-id="d339e-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d339e-257">In Global Catalog</span></span>      | <span data-ttu-id="d339e-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-258">False</span></span>                           |
| <span data-ttu-id="d339e-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d339e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d339e-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d339e-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d339e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d339e-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d339e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d339e-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d339e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-263">Search-Flags</span></span>           | <span data-ttu-id="d339e-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d339e-264">0x00000001</span></span>                      |
| <span data-ttu-id="d339e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-265">System-Flags</span></span>           | <span data-ttu-id="d339e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d339e-266">0x00000010</span></span>                      |
| <span data-ttu-id="d339e-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d339e-267">Classes used in</span></span>        | [<span data-ttu-id="d339e-268">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d339e-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d339e-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d339e-269">Windows Server 2012</span></span>



| <span data-ttu-id="d339e-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="d339e-270">Entry</span></span> | <span data-ttu-id="d339e-271">Значение</span><span class="sxs-lookup"><span data-stu-id="d339e-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d339e-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d339e-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d339e-273">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d339e-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="d339e-274">System-Only</span></span>            | <span data-ttu-id="d339e-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-275">False</span></span>                           |
| <span data-ttu-id="d339e-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d339e-276">Is-Single-Valued</span></span>       | <span data-ttu-id="d339e-277">True</span><span class="sxs-lookup"><span data-stu-id="d339e-277">True</span></span>                            |
| <span data-ttu-id="d339e-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d339e-278">Is Indexed</span></span>             | <span data-ttu-id="d339e-279">True</span><span class="sxs-lookup"><span data-stu-id="d339e-279">True</span></span>                            |
| <span data-ttu-id="d339e-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d339e-280">In Global Catalog</span></span>      | <span data-ttu-id="d339e-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="d339e-281">False</span></span>                           |
| <span data-ttu-id="d339e-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d339e-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="d339e-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d339e-283">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d339e-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d339e-284">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d339e-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d339e-285">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d339e-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-286">Search-Flags</span></span>           | <span data-ttu-id="d339e-287">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d339e-287">0x00000001</span></span>                      |
| <span data-ttu-id="d339e-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d339e-288">System-Flags</span></span>           | <span data-ttu-id="d339e-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d339e-289">0x00000010</span></span>                      |
| <span data-ttu-id="d339e-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d339e-290">Classes used in</span></span>        | [<span data-ttu-id="d339e-291">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="d339e-291">**Top**</span></span>](c-top.md)<br/> |



 

 





