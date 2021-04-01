---
title: Атрибут MS-DS-Creator-SID
description: Идентификатор безопасности создателя объекта, содержащего этот атрибут.
ms.assetid: 5e643c56-bfe9-4489-89a9-5ce56f90f288
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DS-Creator-SID
- Схема AD атрибута mS-DS-Креаторсид
topic_type:
- apiref
api_name:
- MS-DS-Creator-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b5b5635773271c4864ac2c8ec1898edcc9a9f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989557"
---
# <a name="ms-ds-creator-sid-attribute"></a><span data-ttu-id="9f9d9-105">Атрибут MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="9f9d9-105">MS-DS-Creator-SID attribute</span></span>

<span data-ttu-id="9f9d9-106">Идентификатор безопасности создателя объекта, содержащего этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="9f9d9-106">The security ID of the creator of the object that contains this attribute.</span></span>



| <span data-ttu-id="9f9d9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="9f9d9-107">Entry</span></span> | <span data-ttu-id="9f9d9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9f9d9-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9f9d9-109">CN</span><span class="sxs-lookup"><span data-stu-id="9f9d9-109">CN</span></span>                | <span data-ttu-id="9f9d9-110">MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="9f9d9-110">MS-DS-Creator-SID</span></span>                    |
| <span data-ttu-id="9f9d9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9f9d9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9f9d9-112">mS-DS-Креаторсид</span><span class="sxs-lookup"><span data-stu-id="9f9d9-112">mS-DS-CreatorSID</span></span>                     |
| <span data-ttu-id="9f9d9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="9f9d9-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9f9d9-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9f9d9-114">Update Privilege</span></span>  | <span data-ttu-id="9f9d9-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="9f9d9-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="9f9d9-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9f9d9-116">Update Frequency</span></span>  | <span data-ttu-id="9f9d9-117">При создании нового объекта.</span><span class="sxs-lookup"><span data-stu-id="9f9d9-117">Whenever a new object is created.</span></span>    |
| <span data-ttu-id="9f9d9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9f9d9-118">Attribute-Id</span></span>      | <span data-ttu-id="9f9d9-119">1.2.840.113556.1.4.1410</span><span class="sxs-lookup"><span data-stu-id="9f9d9-119">1.2.840.113556.1.4.1410</span></span>              |
| <span data-ttu-id="9f9d9-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9f9d9-120">System-Id-Guid</span></span>    | <span data-ttu-id="9f9d9-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="9f9d9-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span></span> |
| <span data-ttu-id="9f9d9-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f9d9-122">Syntax</span></span>            | [<span data-ttu-id="9f9d9-123">**Строка (SID)**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-123">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="9f9d9-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9f9d9-124">Implementations</span></span>

-   [<span data-ttu-id="9f9d9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9f9d9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9f9d9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9f9d9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9f9d9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9f9d9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9f9d9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f9d9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9f9d9-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="9f9d9-132">Entry</span></span> | <span data-ttu-id="9f9d9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9f9d9-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9f9d9-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9f9d9-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9d9-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9d9-136">System-Only</span></span>            | <span data-ttu-id="9f9d9-137">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-137">True</span></span>                              |
| <span data-ttu-id="9f9d9-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9f9d9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9d9-139">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-139">True</span></span>                              |
| <span data-ttu-id="9f9d9-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9f9d9-140">Is Indexed</span></span>             | <span data-ttu-id="9f9d9-141">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-141">True</span></span>                              |
| <span data-ttu-id="9f9d9-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9f9d9-142">In Global Catalog</span></span>      | <span data-ttu-id="9f9d9-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="9f9d9-143">False</span></span>                             |
| <span data-ttu-id="9f9d9-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9f9d9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9d9-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9f9d9-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9f9d9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9d9-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9d9-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-148">Search-Flags</span></span>           | <span data-ttu-id="9f9d9-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9f9d9-149">0x00000001</span></span>                        |
| <span data-ttu-id="9f9d9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-150">System-Flags</span></span>           | <span data-ttu-id="9f9d9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f9d9-151">0x00000010</span></span>                        |
| <span data-ttu-id="9f9d9-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9f9d9-152">Classes used in</span></span>        | [<span data-ttu-id="9f9d9-153">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9f9d9-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f9d9-154">Windows Server 2003</span></span>



| <span data-ttu-id="9f9d9-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="9f9d9-155">Entry</span></span> | <span data-ttu-id="9f9d9-156">Значение</span><span class="sxs-lookup"><span data-stu-id="9f9d9-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9f9d9-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9f9d9-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9d9-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9d9-159">System-Only</span></span>            | <span data-ttu-id="9f9d9-160">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-160">True</span></span>                              |
| <span data-ttu-id="9f9d9-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9f9d9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9d9-162">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-162">True</span></span>                              |
| <span data-ttu-id="9f9d9-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9f9d9-163">Is Indexed</span></span>             | <span data-ttu-id="9f9d9-164">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-164">True</span></span>                              |
| <span data-ttu-id="9f9d9-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9f9d9-165">In Global Catalog</span></span>      | <span data-ttu-id="9f9d9-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="9f9d9-166">False</span></span>                             |
| <span data-ttu-id="9f9d9-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9f9d9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9d9-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9f9d9-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9f9d9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9d9-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9d9-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-171">Search-Flags</span></span>           | <span data-ttu-id="9f9d9-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9f9d9-172">0x00000001</span></span>                        |
| <span data-ttu-id="9f9d9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-173">System-Flags</span></span>           | <span data-ttu-id="9f9d9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f9d9-174">0x00000010</span></span>                        |
| <span data-ttu-id="9f9d9-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9f9d9-175">Classes used in</span></span>        | [<span data-ttu-id="9f9d9-176">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9f9d9-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9f9d9-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9f9d9-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="9f9d9-178">Entry</span></span> | <span data-ttu-id="9f9d9-179">Значение</span><span class="sxs-lookup"><span data-stu-id="9f9d9-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9f9d9-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9f9d9-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9d9-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9d9-182">System-Only</span></span>            | <span data-ttu-id="9f9d9-183">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-183">True</span></span>                              |
| <span data-ttu-id="9f9d9-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9f9d9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9d9-185">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-185">True</span></span>                              |
| <span data-ttu-id="9f9d9-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9f9d9-186">Is Indexed</span></span>             | <span data-ttu-id="9f9d9-187">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-187">True</span></span>                              |
| <span data-ttu-id="9f9d9-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9f9d9-188">In Global Catalog</span></span>      | <span data-ttu-id="9f9d9-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="9f9d9-189">False</span></span>                             |
| <span data-ttu-id="9f9d9-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9f9d9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9d9-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9f9d9-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9f9d9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9d9-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9d9-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-194">Search-Flags</span></span>           | <span data-ttu-id="9f9d9-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9f9d9-195">0x00000001</span></span>                        |
| <span data-ttu-id="9f9d9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-196">System-Flags</span></span>           | <span data-ttu-id="9f9d9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f9d9-197">0x00000010</span></span>                        |
| <span data-ttu-id="9f9d9-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9f9d9-198">Classes used in</span></span>        | [<span data-ttu-id="9f9d9-199">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9f9d9-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f9d9-200">Windows Server 2008</span></span>



| <span data-ttu-id="9f9d9-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="9f9d9-201">Entry</span></span> | <span data-ttu-id="9f9d9-202">Значение</span><span class="sxs-lookup"><span data-stu-id="9f9d9-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9f9d9-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9f9d9-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9d9-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9d9-205">System-Only</span></span>            | <span data-ttu-id="9f9d9-206">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-206">True</span></span>                              |
| <span data-ttu-id="9f9d9-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9f9d9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9d9-208">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-208">True</span></span>                              |
| <span data-ttu-id="9f9d9-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9f9d9-209">Is Indexed</span></span>             | <span data-ttu-id="9f9d9-210">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-210">True</span></span>                              |
| <span data-ttu-id="9f9d9-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9f9d9-211">In Global Catalog</span></span>      | <span data-ttu-id="9f9d9-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="9f9d9-212">False</span></span>                             |
| <span data-ttu-id="9f9d9-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9f9d9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9d9-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9f9d9-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9f9d9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9d9-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9d9-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-217">Search-Flags</span></span>           | <span data-ttu-id="9f9d9-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9f9d9-218">0x00000001</span></span>                        |
| <span data-ttu-id="9f9d9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-219">System-Flags</span></span>           | <span data-ttu-id="9f9d9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f9d9-220">0x00000010</span></span>                        |
| <span data-ttu-id="9f9d9-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9f9d9-221">Classes used in</span></span>        | [<span data-ttu-id="9f9d9-222">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9f9d9-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f9d9-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9f9d9-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="9f9d9-224">Entry</span></span> | <span data-ttu-id="9f9d9-225">Значение</span><span class="sxs-lookup"><span data-stu-id="9f9d9-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9f9d9-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9f9d9-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9d9-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9d9-228">System-Only</span></span>            | <span data-ttu-id="9f9d9-229">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-229">True</span></span>                              |
| <span data-ttu-id="9f9d9-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9f9d9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9d9-231">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-231">True</span></span>                              |
| <span data-ttu-id="9f9d9-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9f9d9-232">Is Indexed</span></span>             | <span data-ttu-id="9f9d9-233">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-233">True</span></span>                              |
| <span data-ttu-id="9f9d9-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9f9d9-234">In Global Catalog</span></span>      | <span data-ttu-id="9f9d9-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="9f9d9-235">False</span></span>                             |
| <span data-ttu-id="9f9d9-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9f9d9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9d9-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9f9d9-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9f9d9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9d9-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9d9-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-240">Search-Flags</span></span>           | <span data-ttu-id="9f9d9-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9f9d9-241">0x00000001</span></span>                        |
| <span data-ttu-id="9f9d9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-242">System-Flags</span></span>           | <span data-ttu-id="9f9d9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f9d9-243">0x00000010</span></span>                        |
| <span data-ttu-id="9f9d9-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9f9d9-244">Classes used in</span></span>        | [<span data-ttu-id="9f9d9-245">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9f9d9-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f9d9-246">Windows Server 2012</span></span>



| <span data-ttu-id="9f9d9-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="9f9d9-247">Entry</span></span> | <span data-ttu-id="9f9d9-248">Значение</span><span class="sxs-lookup"><span data-stu-id="9f9d9-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9f9d9-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9f9d9-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9f9d9-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9f9d9-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9f9d9-251">System-Only</span></span>            | <span data-ttu-id="9f9d9-252">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-252">True</span></span>                              |
| <span data-ttu-id="9f9d9-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9f9d9-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9f9d9-254">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-254">True</span></span>                              |
| <span data-ttu-id="9f9d9-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9f9d9-255">Is Indexed</span></span>             | <span data-ttu-id="9f9d9-256">True</span><span class="sxs-lookup"><span data-stu-id="9f9d9-256">True</span></span>                              |
| <span data-ttu-id="9f9d9-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9f9d9-257">In Global Catalog</span></span>      | <span data-ttu-id="9f9d9-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="9f9d9-258">False</span></span>                             |
| <span data-ttu-id="9f9d9-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9f9d9-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9f9d9-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9f9d9-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9f9d9-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9f9d9-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9f9d9-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9f9d9-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-263">Search-Flags</span></span>           | <span data-ttu-id="9f9d9-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9f9d9-264">0x00000001</span></span>                        |
| <span data-ttu-id="9f9d9-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9f9d9-265">System-Flags</span></span>           | <span data-ttu-id="9f9d9-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9f9d9-266">0x00000010</span></span>                        |
| <span data-ttu-id="9f9d9-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9f9d9-267">Classes used in</span></span>        | [<span data-ttu-id="9f9d9-268">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="9f9d9-268">**User**</span></span>](c-user.md)<br/> |



 

 





