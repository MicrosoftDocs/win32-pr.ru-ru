---
title: атрибут x500uniqueIdentifier
description: Используется для различения объектов при повторном использовании различающегося имени. Это другой тип атрибута из типов UID и uniqueIdentifier.
ms.assetid: 72975f85-2e0a-4b4e-8fc2-8eeb2d744563
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута x500uniqueIdentifier
topic_type:
- apiref
api_name:
- x500uniqueIdentifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b6be2dd1beca51dbc3ad2de2caa8ef6afb11a5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138730"
---
# <a name="x500uniqueidentifier-attribute"></a><span data-ttu-id="299af-105">атрибут x500uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="299af-105">x500uniqueIdentifier attribute</span></span>

<span data-ttu-id="299af-106">Используется для различения объектов при повторном использовании различающегося имени.</span><span class="sxs-lookup"><span data-stu-id="299af-106">Used to distinguish between objects when a distinguished name has been reused.</span></span> <span data-ttu-id="299af-107">Это другой тип атрибута из типов UID и uniqueIdentifier.</span><span class="sxs-lookup"><span data-stu-id="299af-107">This is a different attribute type from both the uid and uniqueIdentifier types.</span></span>



| <span data-ttu-id="299af-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="299af-108">Entry</span></span> | <span data-ttu-id="299af-109">Значение</span><span class="sxs-lookup"><span data-stu-id="299af-109">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="299af-110">CN</span><span class="sxs-lookup"><span data-stu-id="299af-110">CN</span></span>                | <span data-ttu-id="299af-111">x500uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="299af-111">x500uniqueIdentifier</span></span>                                  |
| <span data-ttu-id="299af-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="299af-112">Ldap-Display-Name</span></span> | <span data-ttu-id="299af-113">x500uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="299af-113">x500uniqueIdentifier</span></span>                                  |
| <span data-ttu-id="299af-114">Размер</span><span class="sxs-lookup"><span data-stu-id="299af-114">Size</span></span>              | \-                                                    |
| <span data-ttu-id="299af-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="299af-115">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="299af-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="299af-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="299af-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="299af-117">Attribute-Id</span></span>      | <span data-ttu-id="299af-118">2.5.4.45</span><span class="sxs-lookup"><span data-stu-id="299af-118">2.5.4.45</span></span>                                              |
| <span data-ttu-id="299af-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="299af-119">System-Id-Guid</span></span>    | <span data-ttu-id="299af-120">d07da11f-8a3d-42b6-b0aa-76c962be719a</span><span class="sxs-lookup"><span data-stu-id="299af-120">d07da11f-8a3d-42b6-b0aa-76c962be719a</span></span>                  |
| <span data-ttu-id="299af-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="299af-121">Syntax</span></span>            | [<span data-ttu-id="299af-122">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="299af-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="299af-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="299af-123">Implementations</span></span>

-   [<span data-ttu-id="299af-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="299af-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="299af-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="299af-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="299af-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="299af-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="299af-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="299af-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="299af-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="299af-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="299af-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="299af-129">Windows Server 2003</span></span>



| <span data-ttu-id="299af-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="299af-130">Entry</span></span> | <span data-ttu-id="299af-131">Значение</span><span class="sxs-lookup"><span data-stu-id="299af-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="299af-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="299af-132">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="299af-133">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="299af-134">System-Only</span></span>            | <span data-ttu-id="299af-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-135">False</span></span>                                                                                 |
| <span data-ttu-id="299af-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="299af-136">Is-Single-Valued</span></span>       | <span data-ttu-id="299af-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-137">False</span></span>                                                                                 |
| <span data-ttu-id="299af-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="299af-138">Is Indexed</span></span>             | <span data-ttu-id="299af-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-139">False</span></span>                                                                                 |
| <span data-ttu-id="299af-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="299af-140">In Global Catalog</span></span>      | <span data-ttu-id="299af-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-141">False</span></span>                                                                                 |
| <span data-ttu-id="299af-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="299af-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="299af-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="299af-143">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="299af-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="299af-144">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="299af-145">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-146">Search-Flags</span></span>           | <span data-ttu-id="299af-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-147">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-148">System-Flags</span></span>           | <span data-ttu-id="299af-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-149">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="299af-150">Classes used in</span></span>        | [<span data-ttu-id="299af-151">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="299af-151">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="299af-152">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="299af-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="299af-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="299af-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="299af-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="299af-154">Entry</span></span> | <span data-ttu-id="299af-155">Значение</span><span class="sxs-lookup"><span data-stu-id="299af-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="299af-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="299af-156">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="299af-157">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="299af-158">System-Only</span></span>            | <span data-ttu-id="299af-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-159">False</span></span>                                                                                 |
| <span data-ttu-id="299af-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="299af-160">Is-Single-Valued</span></span>       | <span data-ttu-id="299af-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-161">False</span></span>                                                                                 |
| <span data-ttu-id="299af-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="299af-162">Is Indexed</span></span>             | <span data-ttu-id="299af-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-163">False</span></span>                                                                                 |
| <span data-ttu-id="299af-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="299af-164">In Global Catalog</span></span>      | <span data-ttu-id="299af-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-165">False</span></span>                                                                                 |
| <span data-ttu-id="299af-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="299af-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="299af-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="299af-167">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="299af-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="299af-168">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="299af-169">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-170">Search-Flags</span></span>           | <span data-ttu-id="299af-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-171">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-172">System-Flags</span></span>           | <span data-ttu-id="299af-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-173">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="299af-174">Classes used in</span></span>        | [<span data-ttu-id="299af-175">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="299af-175">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="299af-176">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="299af-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="299af-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="299af-177">Windows Server 2008</span></span>



| <span data-ttu-id="299af-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="299af-178">Entry</span></span> | <span data-ttu-id="299af-179">Значение</span><span class="sxs-lookup"><span data-stu-id="299af-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="299af-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="299af-180">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="299af-181">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="299af-182">System-Only</span></span>            | <span data-ttu-id="299af-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-183">False</span></span>                                                                                 |
| <span data-ttu-id="299af-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="299af-184">Is-Single-Valued</span></span>       | <span data-ttu-id="299af-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-185">False</span></span>                                                                                 |
| <span data-ttu-id="299af-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="299af-186">Is Indexed</span></span>             | <span data-ttu-id="299af-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-187">False</span></span>                                                                                 |
| <span data-ttu-id="299af-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="299af-188">In Global Catalog</span></span>      | <span data-ttu-id="299af-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-189">False</span></span>                                                                                 |
| <span data-ttu-id="299af-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="299af-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="299af-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="299af-191">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="299af-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="299af-192">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="299af-193">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-194">Search-Flags</span></span>           | <span data-ttu-id="299af-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-195">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-196">System-Flags</span></span>           | <span data-ttu-id="299af-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-197">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="299af-198">Classes used in</span></span>        | [<span data-ttu-id="299af-199">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="299af-199">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="299af-200">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="299af-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="299af-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="299af-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="299af-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="299af-202">Entry</span></span> | <span data-ttu-id="299af-203">Значение</span><span class="sxs-lookup"><span data-stu-id="299af-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="299af-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="299af-204">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="299af-205">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="299af-206">System-Only</span></span>            | <span data-ttu-id="299af-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-207">False</span></span>                                                                                 |
| <span data-ttu-id="299af-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="299af-208">Is-Single-Valued</span></span>       | <span data-ttu-id="299af-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-209">False</span></span>                                                                                 |
| <span data-ttu-id="299af-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="299af-210">Is Indexed</span></span>             | <span data-ttu-id="299af-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-211">False</span></span>                                                                                 |
| <span data-ttu-id="299af-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="299af-212">In Global Catalog</span></span>      | <span data-ttu-id="299af-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-213">False</span></span>                                                                                 |
| <span data-ttu-id="299af-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="299af-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="299af-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="299af-215">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="299af-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="299af-216">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="299af-217">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-218">Search-Flags</span></span>           | <span data-ttu-id="299af-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-219">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-220">System-Flags</span></span>           | <span data-ttu-id="299af-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-221">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="299af-222">Classes used in</span></span>        | [<span data-ttu-id="299af-223">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="299af-223">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="299af-224">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="299af-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="299af-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="299af-225">Windows Server 2012</span></span>



| <span data-ttu-id="299af-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="299af-226">Entry</span></span> | <span data-ttu-id="299af-227">Значение</span><span class="sxs-lookup"><span data-stu-id="299af-227">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="299af-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="299af-228">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="299af-229">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="299af-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="299af-230">System-Only</span></span>            | <span data-ttu-id="299af-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-231">False</span></span>                                                                                 |
| <span data-ttu-id="299af-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="299af-232">Is-Single-Valued</span></span>       | <span data-ttu-id="299af-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-233">False</span></span>                                                                                 |
| <span data-ttu-id="299af-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="299af-234">Is Indexed</span></span>             | <span data-ttu-id="299af-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-235">False</span></span>                                                                                 |
| <span data-ttu-id="299af-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="299af-236">In Global Catalog</span></span>      | <span data-ttu-id="299af-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="299af-237">False</span></span>                                                                                 |
| <span data-ttu-id="299af-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="299af-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="299af-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="299af-239">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="299af-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="299af-240">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="299af-241">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="299af-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-242">Search-Flags</span></span>           | <span data-ttu-id="299af-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-243">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="299af-244">System-Flags</span></span>           | <span data-ttu-id="299af-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="299af-245">0x00000000</span></span>                                                                            |
| <span data-ttu-id="299af-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="299af-246">Classes used in</span></span>        | [<span data-ttu-id="299af-247">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="299af-247">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="299af-248">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="299af-248">**User**</span></span>](c-user.md)<br/> |



 

 





