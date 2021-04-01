---
title: атрибут Мснпалловдиалин
description: Указывает, имеет ли учетная запись разрешение на удаленный доступ к серверу удаленного доступа.
ms.assetid: 8e0d98b4-93b1-4a76-a8b7-d6017028b48a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Мснпалловдиалин
topic_type:
- apiref
api_name:
- msNPAllowDialin
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e56f9fe3817053e3e1e49611fb76934acbbcba9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138895"
---
# <a name="msnpallowdialin-attribute"></a><span data-ttu-id="58e0b-104">атрибут Мснпалловдиалин</span><span class="sxs-lookup"><span data-stu-id="58e0b-104">msNPAllowDialin attribute</span></span>

<span data-ttu-id="58e0b-105">Указывает, имеет ли учетная запись разрешение на удаленный доступ к серверу удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="58e0b-105">Indicates whether the account has permission to dial in to the RAS server.</span></span> <span data-ttu-id="58e0b-106">Не изменяйте это значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="58e0b-106">Do not modify this value directly.</span></span> <span data-ttu-id="58e0b-107">Используйте соответствующую [функцию администрирования RAS](/windows/desktop/RRAS/ras-administration-functions) для изменения этого значения.</span><span class="sxs-lookup"><span data-stu-id="58e0b-107">Use the appropriate [RAS administration function](/windows/desktop/RRAS/ras-administration-functions) to modify this value.</span></span>



| <span data-ttu-id="58e0b-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="58e0b-108">Entry</span></span> | <span data-ttu-id="58e0b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="58e0b-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="58e0b-110">CN</span><span class="sxs-lookup"><span data-stu-id="58e0b-110">CN</span></span>                | <span data-ttu-id="58e0b-111">мснпалловдиалин</span><span class="sxs-lookup"><span data-stu-id="58e0b-111">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="58e0b-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="58e0b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="58e0b-113">мснпалловдиалин</span><span class="sxs-lookup"><span data-stu-id="58e0b-113">msNPAllowDialin</span></span>                      |
| <span data-ttu-id="58e0b-114">Размер</span><span class="sxs-lookup"><span data-stu-id="58e0b-114">Size</span></span>              | <span data-ttu-id="58e0b-115">4 байта</span><span class="sxs-lookup"><span data-stu-id="58e0b-115">4 bytes</span></span>                              |
| <span data-ttu-id="58e0b-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="58e0b-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="58e0b-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="58e0b-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="58e0b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="58e0b-118">Attribute-Id</span></span>      | <span data-ttu-id="58e0b-119">1.2.840.113556.1.4.1119</span><span class="sxs-lookup"><span data-stu-id="58e0b-119">1.2.840.113556.1.4.1119</span></span>              |
| <span data-ttu-id="58e0b-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="58e0b-120">System-Id-Guid</span></span>    | <span data-ttu-id="58e0b-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="58e0b-121">db0c9085-c1f2-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="58e0b-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58e0b-122">Syntax</span></span>            | [<span data-ttu-id="58e0b-123">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="58e0b-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="58e0b-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="58e0b-124">Implementations</span></span>

-   [<span data-ttu-id="58e0b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="58e0b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="58e0b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="58e0b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="58e0b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="58e0b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="58e0b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="58e0b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="58e0b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="58e0b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="58e0b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="58e0b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="58e0b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="58e0b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="58e0b-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="58e0b-132">Entry</span></span> | <span data-ttu-id="58e0b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="58e0b-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58e0b-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58e0b-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e0b-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e0b-136">System-Only</span></span>            | <span data-ttu-id="58e0b-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-137">False</span></span>                             |
| <span data-ttu-id="58e0b-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58e0b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="58e0b-139">True</span><span class="sxs-lookup"><span data-stu-id="58e0b-139">True</span></span>                              |
| <span data-ttu-id="58e0b-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58e0b-140">Is Indexed</span></span>             | <span data-ttu-id="58e0b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-141">False</span></span>                             |
| <span data-ttu-id="58e0b-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58e0b-142">In Global Catalog</span></span>      | <span data-ttu-id="58e0b-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-143">False</span></span>                             |
| <span data-ttu-id="58e0b-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58e0b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e0b-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58e0b-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58e0b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e0b-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="58e0b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e0b-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="58e0b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-148">Search-Flags</span></span>           | <span data-ttu-id="58e0b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58e0b-149">0x00000000</span></span>                        |
| <span data-ttu-id="58e0b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-150">System-Flags</span></span>           | <span data-ttu-id="58e0b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e0b-151">0x00000010</span></span>                        |
| <span data-ttu-id="58e0b-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58e0b-152">Classes used in</span></span>        | [<span data-ttu-id="58e0b-153">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="58e0b-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="58e0b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58e0b-154">Windows Server 2003</span></span>



| <span data-ttu-id="58e0b-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="58e0b-155">Entry</span></span> | <span data-ttu-id="58e0b-156">Значение</span><span class="sxs-lookup"><span data-stu-id="58e0b-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58e0b-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58e0b-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e0b-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e0b-159">System-Only</span></span>            | <span data-ttu-id="58e0b-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-160">False</span></span>                             |
| <span data-ttu-id="58e0b-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58e0b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="58e0b-162">True</span><span class="sxs-lookup"><span data-stu-id="58e0b-162">True</span></span>                              |
| <span data-ttu-id="58e0b-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58e0b-163">Is Indexed</span></span>             | <span data-ttu-id="58e0b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-164">False</span></span>                             |
| <span data-ttu-id="58e0b-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58e0b-165">In Global Catalog</span></span>      | <span data-ttu-id="58e0b-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-166">False</span></span>                             |
| <span data-ttu-id="58e0b-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58e0b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e0b-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58e0b-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58e0b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e0b-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="58e0b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e0b-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="58e0b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-171">Search-Flags</span></span>           | <span data-ttu-id="58e0b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58e0b-172">0x00000000</span></span>                        |
| <span data-ttu-id="58e0b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-173">System-Flags</span></span>           | <span data-ttu-id="58e0b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e0b-174">0x00000010</span></span>                        |
| <span data-ttu-id="58e0b-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58e0b-175">Classes used in</span></span>        | [<span data-ttu-id="58e0b-176">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="58e0b-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="58e0b-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="58e0b-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="58e0b-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="58e0b-178">Entry</span></span> | <span data-ttu-id="58e0b-179">Значение</span><span class="sxs-lookup"><span data-stu-id="58e0b-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58e0b-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58e0b-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e0b-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e0b-182">System-Only</span></span>            | <span data-ttu-id="58e0b-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-183">False</span></span>                             |
| <span data-ttu-id="58e0b-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58e0b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="58e0b-185">True</span><span class="sxs-lookup"><span data-stu-id="58e0b-185">True</span></span>                              |
| <span data-ttu-id="58e0b-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58e0b-186">Is Indexed</span></span>             | <span data-ttu-id="58e0b-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-187">False</span></span>                             |
| <span data-ttu-id="58e0b-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58e0b-188">In Global Catalog</span></span>      | <span data-ttu-id="58e0b-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-189">False</span></span>                             |
| <span data-ttu-id="58e0b-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58e0b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e0b-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58e0b-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58e0b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e0b-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="58e0b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e0b-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="58e0b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-194">Search-Flags</span></span>           | <span data-ttu-id="58e0b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58e0b-195">0x00000000</span></span>                        |
| <span data-ttu-id="58e0b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-196">System-Flags</span></span>           | <span data-ttu-id="58e0b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e0b-197">0x00000010</span></span>                        |
| <span data-ttu-id="58e0b-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58e0b-198">Classes used in</span></span>        | [<span data-ttu-id="58e0b-199">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="58e0b-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="58e0b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58e0b-200">Windows Server 2008</span></span>



| <span data-ttu-id="58e0b-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="58e0b-201">Entry</span></span> | <span data-ttu-id="58e0b-202">Значение</span><span class="sxs-lookup"><span data-stu-id="58e0b-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58e0b-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58e0b-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e0b-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e0b-205">System-Only</span></span>            | <span data-ttu-id="58e0b-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-206">False</span></span>                             |
| <span data-ttu-id="58e0b-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58e0b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="58e0b-208">True</span><span class="sxs-lookup"><span data-stu-id="58e0b-208">True</span></span>                              |
| <span data-ttu-id="58e0b-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58e0b-209">Is Indexed</span></span>             | <span data-ttu-id="58e0b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-210">False</span></span>                             |
| <span data-ttu-id="58e0b-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58e0b-211">In Global Catalog</span></span>      | <span data-ttu-id="58e0b-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-212">False</span></span>                             |
| <span data-ttu-id="58e0b-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58e0b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e0b-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58e0b-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58e0b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e0b-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="58e0b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e0b-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="58e0b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-217">Search-Flags</span></span>           | <span data-ttu-id="58e0b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e0b-218">0x00000010</span></span>                        |
| <span data-ttu-id="58e0b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-219">System-Flags</span></span>           | <span data-ttu-id="58e0b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e0b-220">0x00000010</span></span>                        |
| <span data-ttu-id="58e0b-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58e0b-221">Classes used in</span></span>        | [<span data-ttu-id="58e0b-222">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="58e0b-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="58e0b-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="58e0b-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="58e0b-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="58e0b-224">Entry</span></span> | <span data-ttu-id="58e0b-225">Значение</span><span class="sxs-lookup"><span data-stu-id="58e0b-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58e0b-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58e0b-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e0b-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e0b-228">System-Only</span></span>            | <span data-ttu-id="58e0b-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-229">False</span></span>                             |
| <span data-ttu-id="58e0b-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58e0b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="58e0b-231">True</span><span class="sxs-lookup"><span data-stu-id="58e0b-231">True</span></span>                              |
| <span data-ttu-id="58e0b-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58e0b-232">Is Indexed</span></span>             | <span data-ttu-id="58e0b-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-233">False</span></span>                             |
| <span data-ttu-id="58e0b-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58e0b-234">In Global Catalog</span></span>      | <span data-ttu-id="58e0b-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-235">False</span></span>                             |
| <span data-ttu-id="58e0b-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58e0b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e0b-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58e0b-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58e0b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e0b-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="58e0b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e0b-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="58e0b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-240">Search-Flags</span></span>           | <span data-ttu-id="58e0b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e0b-241">0x00000010</span></span>                        |
| <span data-ttu-id="58e0b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-242">System-Flags</span></span>           | <span data-ttu-id="58e0b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e0b-243">0x00000010</span></span>                        |
| <span data-ttu-id="58e0b-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58e0b-244">Classes used in</span></span>        | [<span data-ttu-id="58e0b-245">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="58e0b-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="58e0b-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58e0b-246">Windows Server 2012</span></span>



| <span data-ttu-id="58e0b-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="58e0b-247">Entry</span></span> | <span data-ttu-id="58e0b-248">Значение</span><span class="sxs-lookup"><span data-stu-id="58e0b-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="58e0b-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="58e0b-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58e0b-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="58e0b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="58e0b-251">System-Only</span></span>            | <span data-ttu-id="58e0b-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-252">False</span></span>                             |
| <span data-ttu-id="58e0b-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="58e0b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="58e0b-254">True</span><span class="sxs-lookup"><span data-stu-id="58e0b-254">True</span></span>                              |
| <span data-ttu-id="58e0b-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="58e0b-255">Is Indexed</span></span>             | <span data-ttu-id="58e0b-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-256">False</span></span>                             |
| <span data-ttu-id="58e0b-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="58e0b-257">In Global Catalog</span></span>      | <span data-ttu-id="58e0b-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="58e0b-258">False</span></span>                             |
| <span data-ttu-id="58e0b-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="58e0b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="58e0b-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="58e0b-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="58e0b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58e0b-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="58e0b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58e0b-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="58e0b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-263">Search-Flags</span></span>           | <span data-ttu-id="58e0b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e0b-264">0x00000010</span></span>                        |
| <span data-ttu-id="58e0b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58e0b-265">System-Flags</span></span>           | <span data-ttu-id="58e0b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58e0b-266">0x00000010</span></span>                        |
| <span data-ttu-id="58e0b-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="58e0b-267">Classes used in</span></span>        | [<span data-ttu-id="58e0b-268">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="58e0b-268">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="58e0b-269">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58e0b-269">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e0b-270">Функции администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="58e0b-270">RAS Administration Functions</span></span>](/windows/desktop/RRAS/ras-administration-functions)
</dt> </dl>

 

