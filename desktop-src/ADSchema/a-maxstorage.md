---
title: Атрибут Max-Storage
description: Максимальный объем дискового пространства, который может использовать пользователь. Используйте значение, указанное в параметре USER \_ максстораже \_ ununlimited, чтобы использовать все доступное место на диске.
ms.assetid: 69302641-ecfc-4b0f-81f8-f69b48c6faa7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Max-Storage
- Схема AD атрибута Максстораже
topic_type:
- apiref
api_name:
- Max-Storage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6caff3f85de7073818096324445b63a3c1c9be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893574"
---
# <a name="max-storage-attribute"></a><span data-ttu-id="8f435-106">Атрибут Max-Storage</span><span class="sxs-lookup"><span data-stu-id="8f435-106">Max-Storage attribute</span></span>

<span data-ttu-id="8f435-107">Максимальный объем дискового пространства, который может использовать пользователь.</span><span class="sxs-lookup"><span data-stu-id="8f435-107">The maximum amount of disk space the user can use.</span></span> <span data-ttu-id="8f435-108">Используйте значение, указанное в параметре USER \_ максстораже \_ ununlimited, чтобы использовать все доступное место на диске.</span><span class="sxs-lookup"><span data-stu-id="8f435-108">Use the value specified in USER\_MAXSTORAGE\_UNLIMITED to use all available disk space.</span></span>



| <span data-ttu-id="8f435-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f435-109">Entry</span></span> | <span data-ttu-id="8f435-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8f435-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="8f435-111">CN</span><span class="sxs-lookup"><span data-stu-id="8f435-111">CN</span></span>                | <span data-ttu-id="8f435-112">Max-Storage</span><span class="sxs-lookup"><span data-stu-id="8f435-112">Max-Storage</span></span>                                                |
| <span data-ttu-id="8f435-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8f435-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8f435-114">максстораже</span><span class="sxs-lookup"><span data-stu-id="8f435-114">maxStorage</span></span>                                                 |
| <span data-ttu-id="8f435-115">Размер</span><span class="sxs-lookup"><span data-stu-id="8f435-115">Size</span></span>              | <span data-ttu-id="8f435-116">8 байт: пользователь \_ максстораже \_ без ограничений ((без знака) — 1L)</span><span class="sxs-lookup"><span data-stu-id="8f435-116">8 bytes: USER\_MAXSTORAGE\_UNLIMITED ((unsigned long) -1L)</span></span> |
| <span data-ttu-id="8f435-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8f435-117">Update Privilege</span></span>  | <span data-ttu-id="8f435-118">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="8f435-118">Domain administrator</span></span>                                       |
| <span data-ttu-id="8f435-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8f435-119">Update Frequency</span></span>  | <span data-ttu-id="8f435-120">При необходимости изменения дисковой квоты.</span><span class="sxs-lookup"><span data-stu-id="8f435-120">Whenever the disk quota needs to change.</span></span>                   |
| <span data-ttu-id="8f435-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8f435-121">Attribute-Id</span></span>      | <span data-ttu-id="8f435-122">1.2.840.113556.1.4.76</span><span class="sxs-lookup"><span data-stu-id="8f435-122">1.2.840.113556.1.4.76</span></span>                                      |
| <span data-ttu-id="8f435-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8f435-123">System-Id-Guid</span></span>    | <span data-ttu-id="8f435-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8f435-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span></span>                       |
| <span data-ttu-id="8f435-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f435-125">Syntax</span></span>            | [<span data-ttu-id="8f435-126">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="8f435-126">**Interval**</span></span>](s-interval.md)                             |



## <a name="implementations"></a><span data-ttu-id="8f435-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8f435-127">Implementations</span></span>

-   [<span data-ttu-id="8f435-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8f435-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8f435-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8f435-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8f435-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8f435-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8f435-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8f435-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8f435-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8f435-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8f435-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8f435-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8f435-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f435-134">Windows 2000 Server</span></span>



| <span data-ttu-id="8f435-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f435-135">Entry</span></span> | <span data-ttu-id="8f435-136">Значение</span><span class="sxs-lookup"><span data-stu-id="8f435-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f435-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f435-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f435-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f435-139">System-Only</span></span>            | <span data-ttu-id="8f435-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-140">False</span></span>                             |
| <span data-ttu-id="8f435-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f435-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8f435-142">True</span><span class="sxs-lookup"><span data-stu-id="8f435-142">True</span></span>                              |
| <span data-ttu-id="8f435-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f435-143">Is Indexed</span></span>             | <span data-ttu-id="8f435-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-144">False</span></span>                             |
| <span data-ttu-id="8f435-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f435-145">In Global Catalog</span></span>      | <span data-ttu-id="8f435-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-146">False</span></span>                             |
| <span data-ttu-id="8f435-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f435-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f435-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f435-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f435-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f435-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f435-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f435-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f435-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-151">Search-Flags</span></span>           | <span data-ttu-id="8f435-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-152">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-153">System-Flags</span></span>           | <span data-ttu-id="8f435-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-154">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f435-155">Classes used in</span></span>        | [<span data-ttu-id="8f435-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f435-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8f435-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f435-157">Windows Server 2003</span></span>



| <span data-ttu-id="8f435-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f435-158">Entry</span></span> | <span data-ttu-id="8f435-159">Значение</span><span class="sxs-lookup"><span data-stu-id="8f435-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f435-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f435-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f435-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f435-162">System-Only</span></span>            | <span data-ttu-id="8f435-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-163">False</span></span>                             |
| <span data-ttu-id="8f435-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f435-164">Is-Single-Valued</span></span>       | <span data-ttu-id="8f435-165">True</span><span class="sxs-lookup"><span data-stu-id="8f435-165">True</span></span>                              |
| <span data-ttu-id="8f435-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f435-166">Is Indexed</span></span>             | <span data-ttu-id="8f435-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-167">False</span></span>                             |
| <span data-ttu-id="8f435-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f435-168">In Global Catalog</span></span>      | <span data-ttu-id="8f435-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-169">False</span></span>                             |
| <span data-ttu-id="8f435-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f435-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f435-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f435-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f435-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f435-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f435-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f435-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f435-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-174">Search-Flags</span></span>           | <span data-ttu-id="8f435-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-175">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-176">System-Flags</span></span>           | <span data-ttu-id="8f435-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-177">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f435-178">Classes used in</span></span>        | [<span data-ttu-id="8f435-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f435-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8f435-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8f435-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8f435-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f435-181">Entry</span></span> | <span data-ttu-id="8f435-182">Значение</span><span class="sxs-lookup"><span data-stu-id="8f435-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f435-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f435-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f435-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f435-185">System-Only</span></span>            | <span data-ttu-id="8f435-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-186">False</span></span>                             |
| <span data-ttu-id="8f435-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f435-187">Is-Single-Valued</span></span>       | <span data-ttu-id="8f435-188">True</span><span class="sxs-lookup"><span data-stu-id="8f435-188">True</span></span>                              |
| <span data-ttu-id="8f435-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f435-189">Is Indexed</span></span>             | <span data-ttu-id="8f435-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-190">False</span></span>                             |
| <span data-ttu-id="8f435-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f435-191">In Global Catalog</span></span>      | <span data-ttu-id="8f435-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-192">False</span></span>                             |
| <span data-ttu-id="8f435-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f435-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f435-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f435-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f435-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f435-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f435-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f435-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f435-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-197">Search-Flags</span></span>           | <span data-ttu-id="8f435-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-198">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-199">System-Flags</span></span>           | <span data-ttu-id="8f435-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-200">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f435-201">Classes used in</span></span>        | [<span data-ttu-id="8f435-202">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f435-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8f435-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f435-203">Windows Server 2008</span></span>



| <span data-ttu-id="8f435-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f435-204">Entry</span></span> | <span data-ttu-id="8f435-205">Значение</span><span class="sxs-lookup"><span data-stu-id="8f435-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f435-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f435-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f435-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f435-208">System-Only</span></span>            | <span data-ttu-id="8f435-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-209">False</span></span>                             |
| <span data-ttu-id="8f435-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f435-210">Is-Single-Valued</span></span>       | <span data-ttu-id="8f435-211">True</span><span class="sxs-lookup"><span data-stu-id="8f435-211">True</span></span>                              |
| <span data-ttu-id="8f435-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f435-212">Is Indexed</span></span>             | <span data-ttu-id="8f435-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-213">False</span></span>                             |
| <span data-ttu-id="8f435-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f435-214">In Global Catalog</span></span>      | <span data-ttu-id="8f435-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-215">False</span></span>                             |
| <span data-ttu-id="8f435-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f435-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f435-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f435-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f435-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f435-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f435-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f435-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f435-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-220">Search-Flags</span></span>           | <span data-ttu-id="8f435-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-221">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-222">System-Flags</span></span>           | <span data-ttu-id="8f435-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-223">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f435-224">Classes used in</span></span>        | [<span data-ttu-id="8f435-225">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f435-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8f435-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8f435-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8f435-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f435-227">Entry</span></span> | <span data-ttu-id="8f435-228">Значение</span><span class="sxs-lookup"><span data-stu-id="8f435-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f435-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f435-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f435-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f435-231">System-Only</span></span>            | <span data-ttu-id="8f435-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-232">False</span></span>                             |
| <span data-ttu-id="8f435-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f435-233">Is-Single-Valued</span></span>       | <span data-ttu-id="8f435-234">True</span><span class="sxs-lookup"><span data-stu-id="8f435-234">True</span></span>                              |
| <span data-ttu-id="8f435-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f435-235">Is Indexed</span></span>             | <span data-ttu-id="8f435-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-236">False</span></span>                             |
| <span data-ttu-id="8f435-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f435-237">In Global Catalog</span></span>      | <span data-ttu-id="8f435-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-238">False</span></span>                             |
| <span data-ttu-id="8f435-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f435-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f435-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f435-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f435-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f435-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f435-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f435-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f435-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-243">Search-Flags</span></span>           | <span data-ttu-id="8f435-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-244">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-245">System-Flags</span></span>           | <span data-ttu-id="8f435-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-246">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f435-247">Classes used in</span></span>        | [<span data-ttu-id="8f435-248">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8f435-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8f435-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f435-249">Windows Server 2012</span></span>



| <span data-ttu-id="8f435-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f435-250">Entry</span></span> | <span data-ttu-id="8f435-251">Значение</span><span class="sxs-lookup"><span data-stu-id="8f435-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="8f435-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8f435-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f435-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="8f435-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f435-254">System-Only</span></span>            | <span data-ttu-id="8f435-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-255">False</span></span>                             |
| <span data-ttu-id="8f435-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8f435-256">Is-Single-Valued</span></span>       | <span data-ttu-id="8f435-257">True</span><span class="sxs-lookup"><span data-stu-id="8f435-257">True</span></span>                              |
| <span data-ttu-id="8f435-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8f435-258">Is Indexed</span></span>             | <span data-ttu-id="8f435-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-259">False</span></span>                             |
| <span data-ttu-id="8f435-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8f435-260">In Global Catalog</span></span>      | <span data-ttu-id="8f435-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f435-261">False</span></span>                             |
| <span data-ttu-id="8f435-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8f435-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f435-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8f435-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="8f435-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f435-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="8f435-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f435-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="8f435-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-266">Search-Flags</span></span>           | <span data-ttu-id="8f435-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-267">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f435-268">System-Flags</span></span>           | <span data-ttu-id="8f435-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f435-269">0x00000010</span></span>                        |
| <span data-ttu-id="8f435-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8f435-270">Classes used in</span></span>        | [<span data-ttu-id="8f435-271">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="8f435-271">**User**</span></span>](c-user.md)<br/> |



 

 





