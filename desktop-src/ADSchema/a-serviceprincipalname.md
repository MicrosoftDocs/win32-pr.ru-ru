---
title: Атрибут Service-Principal-Name
description: Список имен участников, используемых для взаимной проверки подлинности с экземпляром службы на этом компьютере.
ms.assetid: 0ad1694f-0d6f-4350-a088-fdf3ef798c46
ms.tgt_platform: multiple
keywords:
- Service-Principal-имя атрибута AD
- Схема AD атрибута пере(или)
topic_type:
- apiref
api_name:
- Service-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 861f160d2c9b71d2c9914c7ff9c2ea0ee43c8528
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655051"
---
# <a name="service-principal-name-attribute"></a><span data-ttu-id="499fa-105">Атрибут Service-Principal-Name</span><span class="sxs-lookup"><span data-stu-id="499fa-105">Service-Principal-Name attribute</span></span>

<span data-ttu-id="499fa-106">Список имен участников, используемых для взаимной проверки подлинности с экземпляром службы на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="499fa-106">List of principal names used for mutual authentication with an instance of a service on this computer.</span></span>



| <span data-ttu-id="499fa-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="499fa-107">Entry</span></span> | <span data-ttu-id="499fa-108">Значение</span><span class="sxs-lookup"><span data-stu-id="499fa-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="499fa-109">CN</span><span class="sxs-lookup"><span data-stu-id="499fa-109">CN</span></span>                | <span data-ttu-id="499fa-110">Имя участника-службы</span><span class="sxs-lookup"><span data-stu-id="499fa-110">Service-Principal-Name</span></span>                      |
| <span data-ttu-id="499fa-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="499fa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="499fa-112">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="499fa-112">servicePrincipalName</span></span>                        |
| <span data-ttu-id="499fa-113">Размер</span><span class="sxs-lookup"><span data-stu-id="499fa-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="499fa-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="499fa-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="499fa-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="499fa-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="499fa-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="499fa-116">Attribute-Id</span></span>      | <span data-ttu-id="499fa-117">1.2.840.113556.1.4.771</span><span class="sxs-lookup"><span data-stu-id="499fa-117">1.2.840.113556.1.4.771</span></span>                      |
| <span data-ttu-id="499fa-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="499fa-118">System-Id-Guid</span></span>    | <span data-ttu-id="499fa-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="499fa-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span></span>        |
| <span data-ttu-id="499fa-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="499fa-120">Syntax</span></span>            | [<span data-ttu-id="499fa-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="499fa-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="499fa-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="499fa-122">Implementations</span></span>

-   [<span data-ttu-id="499fa-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="499fa-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="499fa-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="499fa-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="499fa-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="499fa-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="499fa-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="499fa-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="499fa-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="499fa-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="499fa-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="499fa-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="499fa-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="499fa-129">Windows 2000 Server</span></span>



| <span data-ttu-id="499fa-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="499fa-130">Entry</span></span> | <span data-ttu-id="499fa-131">Значение</span><span class="sxs-lookup"><span data-stu-id="499fa-131">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="499fa-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="499fa-132">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="499fa-133">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="499fa-134">System-Only</span></span>            | <span data-ttu-id="499fa-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-135">False</span></span>                             |
| <span data-ttu-id="499fa-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="499fa-136">Is-Single-Valued</span></span>       | <span data-ttu-id="499fa-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-137">False</span></span>                             |
| <span data-ttu-id="499fa-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="499fa-138">Is Indexed</span></span>             | <span data-ttu-id="499fa-139">True</span><span class="sxs-lookup"><span data-stu-id="499fa-139">True</span></span>                              |
| <span data-ttu-id="499fa-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="499fa-140">In Global Catalog</span></span>      | <span data-ttu-id="499fa-141">True</span><span class="sxs-lookup"><span data-stu-id="499fa-141">True</span></span>                              |
| <span data-ttu-id="499fa-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="499fa-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="499fa-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="499fa-143">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="499fa-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="499fa-144">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="499fa-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="499fa-145">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="499fa-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-146">Search-Flags</span></span>           | <span data-ttu-id="499fa-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="499fa-147">0x00000001</span></span>                        |
| <span data-ttu-id="499fa-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-148">System-Flags</span></span>           | <span data-ttu-id="499fa-149">0x00000012</span><span class="sxs-lookup"><span data-stu-id="499fa-149">0x00000012</span></span>                        |
| <span data-ttu-id="499fa-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="499fa-150">Classes used in</span></span>        | [<span data-ttu-id="499fa-151">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="499fa-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="499fa-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="499fa-152">Windows Server 2003</span></span>



| <span data-ttu-id="499fa-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="499fa-153">Entry</span></span> | <span data-ttu-id="499fa-154">Значение</span><span class="sxs-lookup"><span data-stu-id="499fa-154">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="499fa-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="499fa-155">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="499fa-156">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="499fa-157">System-Only</span></span>            | <span data-ttu-id="499fa-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-158">False</span></span>                             |
| <span data-ttu-id="499fa-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="499fa-159">Is-Single-Valued</span></span>       | <span data-ttu-id="499fa-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-160">False</span></span>                             |
| <span data-ttu-id="499fa-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="499fa-161">Is Indexed</span></span>             | <span data-ttu-id="499fa-162">True</span><span class="sxs-lookup"><span data-stu-id="499fa-162">True</span></span>                              |
| <span data-ttu-id="499fa-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="499fa-163">In Global Catalog</span></span>      | <span data-ttu-id="499fa-164">True</span><span class="sxs-lookup"><span data-stu-id="499fa-164">True</span></span>                              |
| <span data-ttu-id="499fa-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="499fa-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="499fa-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="499fa-166">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="499fa-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="499fa-167">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="499fa-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="499fa-168">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="499fa-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-169">Search-Flags</span></span>           | <span data-ttu-id="499fa-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="499fa-170">0x00000001</span></span>                        |
| <span data-ttu-id="499fa-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-171">System-Flags</span></span>           | <span data-ttu-id="499fa-172">0x00000012</span><span class="sxs-lookup"><span data-stu-id="499fa-172">0x00000012</span></span>                        |
| <span data-ttu-id="499fa-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="499fa-173">Classes used in</span></span>        | [<span data-ttu-id="499fa-174">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="499fa-174">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="499fa-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="499fa-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="499fa-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="499fa-176">Entry</span></span> | <span data-ttu-id="499fa-177">Значение</span><span class="sxs-lookup"><span data-stu-id="499fa-177">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="499fa-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="499fa-178">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="499fa-179">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="499fa-180">System-Only</span></span>            | <span data-ttu-id="499fa-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-181">False</span></span>                             |
| <span data-ttu-id="499fa-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="499fa-182">Is-Single-Valued</span></span>       | <span data-ttu-id="499fa-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-183">False</span></span>                             |
| <span data-ttu-id="499fa-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="499fa-184">Is Indexed</span></span>             | <span data-ttu-id="499fa-185">True</span><span class="sxs-lookup"><span data-stu-id="499fa-185">True</span></span>                              |
| <span data-ttu-id="499fa-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="499fa-186">In Global Catalog</span></span>      | <span data-ttu-id="499fa-187">True</span><span class="sxs-lookup"><span data-stu-id="499fa-187">True</span></span>                              |
| <span data-ttu-id="499fa-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="499fa-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="499fa-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="499fa-189">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="499fa-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="499fa-190">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="499fa-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="499fa-191">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="499fa-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-192">Search-Flags</span></span>           | <span data-ttu-id="499fa-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="499fa-193">0x00000001</span></span>                        |
| <span data-ttu-id="499fa-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-194">System-Flags</span></span>           | <span data-ttu-id="499fa-195">0x00000012</span><span class="sxs-lookup"><span data-stu-id="499fa-195">0x00000012</span></span>                        |
| <span data-ttu-id="499fa-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="499fa-196">Classes used in</span></span>        | [<span data-ttu-id="499fa-197">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="499fa-197">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="499fa-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="499fa-198">Windows Server 2008</span></span>



| <span data-ttu-id="499fa-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="499fa-199">Entry</span></span> | <span data-ttu-id="499fa-200">Значение</span><span class="sxs-lookup"><span data-stu-id="499fa-200">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="499fa-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="499fa-201">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="499fa-202">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="499fa-203">System-Only</span></span>            | <span data-ttu-id="499fa-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-204">False</span></span>                             |
| <span data-ttu-id="499fa-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="499fa-205">Is-Single-Valued</span></span>       | <span data-ttu-id="499fa-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-206">False</span></span>                             |
| <span data-ttu-id="499fa-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="499fa-207">Is Indexed</span></span>             | <span data-ttu-id="499fa-208">True</span><span class="sxs-lookup"><span data-stu-id="499fa-208">True</span></span>                              |
| <span data-ttu-id="499fa-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="499fa-209">In Global Catalog</span></span>      | <span data-ttu-id="499fa-210">True</span><span class="sxs-lookup"><span data-stu-id="499fa-210">True</span></span>                              |
| <span data-ttu-id="499fa-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="499fa-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="499fa-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="499fa-212">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="499fa-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="499fa-213">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="499fa-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="499fa-214">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="499fa-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-215">Search-Flags</span></span>           | <span data-ttu-id="499fa-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="499fa-216">0x00000001</span></span>                        |
| <span data-ttu-id="499fa-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-217">System-Flags</span></span>           | <span data-ttu-id="499fa-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="499fa-218">0x00000012</span></span>                        |
| <span data-ttu-id="499fa-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="499fa-219">Classes used in</span></span>        | [<span data-ttu-id="499fa-220">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="499fa-220">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="499fa-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="499fa-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="499fa-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="499fa-222">Entry</span></span> | <span data-ttu-id="499fa-223">Значение</span><span class="sxs-lookup"><span data-stu-id="499fa-223">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="499fa-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="499fa-224">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="499fa-225">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="499fa-226">System-Only</span></span>            | <span data-ttu-id="499fa-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-227">False</span></span>                             |
| <span data-ttu-id="499fa-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="499fa-228">Is-Single-Valued</span></span>       | <span data-ttu-id="499fa-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-229">False</span></span>                             |
| <span data-ttu-id="499fa-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="499fa-230">Is Indexed</span></span>             | <span data-ttu-id="499fa-231">True</span><span class="sxs-lookup"><span data-stu-id="499fa-231">True</span></span>                              |
| <span data-ttu-id="499fa-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="499fa-232">In Global Catalog</span></span>      | <span data-ttu-id="499fa-233">True</span><span class="sxs-lookup"><span data-stu-id="499fa-233">True</span></span>                              |
| <span data-ttu-id="499fa-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="499fa-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="499fa-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="499fa-235">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="499fa-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="499fa-236">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="499fa-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="499fa-237">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="499fa-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-238">Search-Flags</span></span>           | <span data-ttu-id="499fa-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="499fa-239">0x00000001</span></span>                        |
| <span data-ttu-id="499fa-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-240">System-Flags</span></span>           | <span data-ttu-id="499fa-241">0x00000012</span><span class="sxs-lookup"><span data-stu-id="499fa-241">0x00000012</span></span>                        |
| <span data-ttu-id="499fa-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="499fa-242">Classes used in</span></span>        | [<span data-ttu-id="499fa-243">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="499fa-243">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="499fa-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="499fa-244">Windows Server 2012</span></span>



| <span data-ttu-id="499fa-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="499fa-245">Entry</span></span> | <span data-ttu-id="499fa-246">Значение</span><span class="sxs-lookup"><span data-stu-id="499fa-246">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="499fa-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="499fa-247">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="499fa-248">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="499fa-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="499fa-249">System-Only</span></span>            | <span data-ttu-id="499fa-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-250">False</span></span>                             |
| <span data-ttu-id="499fa-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="499fa-251">Is-Single-Valued</span></span>       | <span data-ttu-id="499fa-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="499fa-252">False</span></span>                             |
| <span data-ttu-id="499fa-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="499fa-253">Is Indexed</span></span>             | <span data-ttu-id="499fa-254">True</span><span class="sxs-lookup"><span data-stu-id="499fa-254">True</span></span>                              |
| <span data-ttu-id="499fa-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="499fa-255">In Global Catalog</span></span>      | <span data-ttu-id="499fa-256">True</span><span class="sxs-lookup"><span data-stu-id="499fa-256">True</span></span>                              |
| <span data-ttu-id="499fa-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="499fa-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="499fa-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="499fa-258">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="499fa-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="499fa-259">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="499fa-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="499fa-260">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="499fa-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-261">Search-Flags</span></span>           | <span data-ttu-id="499fa-262">0x00000001</span><span class="sxs-lookup"><span data-stu-id="499fa-262">0x00000001</span></span>                        |
| <span data-ttu-id="499fa-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="499fa-263">System-Flags</span></span>           | <span data-ttu-id="499fa-264">0x00000012</span><span class="sxs-lookup"><span data-stu-id="499fa-264">0x00000012</span></span>                        |
| <span data-ttu-id="499fa-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="499fa-265">Classes used in</span></span>        | [<span data-ttu-id="499fa-266">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="499fa-266">**User**</span></span>](c-user.md)<br/> |



 

 





