---
title: Атрибут Categories
description: Список идентификаторов категорий (GUID) для категорий, применяемых к этому приложению.
ms.assetid: c4a3b166-9424-4cb7-bf71-6e312e9818dc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active Directory
- Схема AD атрибута Active Directory
topic_type:
- apiref
api_name:
- Categories
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e1fc80db2a6ef8633d3edbbad6575d7c0f6652
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138294"
---
# <a name="categories-attribute"></a><span data-ttu-id="5dc9f-105">Атрибут Categories</span><span class="sxs-lookup"><span data-stu-id="5dc9f-105">Categories attribute</span></span>

<span data-ttu-id="5dc9f-106">Список идентификаторов категорий (GUID) для категорий, применяемых к этому приложению.</span><span class="sxs-lookup"><span data-stu-id="5dc9f-106">List of category IDs (GUIDs) for categories that apply to this application.</span></span>



| <span data-ttu-id="5dc9f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="5dc9f-107">Entry</span></span> | <span data-ttu-id="5dc9f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5dc9f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5dc9f-109">CN</span><span class="sxs-lookup"><span data-stu-id="5dc9f-109">CN</span></span>                | <span data-ttu-id="5dc9f-110">Категории</span><span class="sxs-lookup"><span data-stu-id="5dc9f-110">Categories</span></span>                                  |
| <span data-ttu-id="5dc9f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5dc9f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5dc9f-112">Категории</span><span class="sxs-lookup"><span data-stu-id="5dc9f-112">categories</span></span>                                  |
| <span data-ttu-id="5dc9f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="5dc9f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="5dc9f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5dc9f-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5dc9f-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5dc9f-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5dc9f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5dc9f-116">Attribute-Id</span></span>      | <span data-ttu-id="5dc9f-117">1.2.840.113556.1.4.672</span><span class="sxs-lookup"><span data-stu-id="5dc9f-117">1.2.840.113556.1.4.672</span></span>                      |
| <span data-ttu-id="5dc9f-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5dc9f-118">System-Id-Guid</span></span>    | <span data-ttu-id="5dc9f-119">7bfdcb7e-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="5dc9f-119">7bfdcb7e-4807-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="5dc9f-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dc9f-120">Syntax</span></span>            | [<span data-ttu-id="5dc9f-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5dc9f-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5dc9f-122">Implementations</span></span>

-   [<span data-ttu-id="5dc9f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5dc9f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5dc9f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5dc9f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5dc9f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5dc9f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5dc9f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5dc9f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="5dc9f-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="5dc9f-130">Entry</span></span> | <span data-ttu-id="5dc9f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5dc9f-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5dc9f-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5dc9f-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dc9f-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dc9f-134">System-Only</span></span>            | <span data-ttu-id="5dc9f-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-135">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5dc9f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="5dc9f-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-137">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5dc9f-138">Is Indexed</span></span>             | <span data-ttu-id="5dc9f-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-139">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5dc9f-140">In Global Catalog</span></span>      | <span data-ttu-id="5dc9f-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-141">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5dc9f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dc9f-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5dc9f-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5dc9f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dc9f-144">Range-Lower</span></span>            | <span data-ttu-id="5dc9f-145">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-145">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dc9f-146">Range-Upper</span></span>            | <span data-ttu-id="5dc9f-147">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-147">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-148">Search-Flags</span></span>           | <span data-ttu-id="5dc9f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dc9f-149">0x00000000</span></span>                                                       |
| <span data-ttu-id="5dc9f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-150">System-Flags</span></span>           | <span data-ttu-id="5dc9f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dc9f-151">0x00000010</span></span>                                                       |
| <span data-ttu-id="5dc9f-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5dc9f-152">Classes used in</span></span>        | [<span data-ttu-id="5dc9f-153">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5dc9f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5dc9f-154">Windows Server 2003</span></span>



| <span data-ttu-id="5dc9f-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="5dc9f-155">Entry</span></span> | <span data-ttu-id="5dc9f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="5dc9f-156">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5dc9f-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5dc9f-157">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dc9f-158">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dc9f-159">System-Only</span></span>            | <span data-ttu-id="5dc9f-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-160">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5dc9f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5dc9f-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-162">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5dc9f-163">Is Indexed</span></span>             | <span data-ttu-id="5dc9f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-164">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5dc9f-165">In Global Catalog</span></span>      | <span data-ttu-id="5dc9f-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-166">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5dc9f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dc9f-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5dc9f-168">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5dc9f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dc9f-169">Range-Lower</span></span>            | <span data-ttu-id="5dc9f-170">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-170">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dc9f-171">Range-Upper</span></span>            | <span data-ttu-id="5dc9f-172">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-172">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-173">Search-Flags</span></span>           | <span data-ttu-id="5dc9f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dc9f-174">0x00000000</span></span>                                                       |
| <span data-ttu-id="5dc9f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-175">System-Flags</span></span>           | <span data-ttu-id="5dc9f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dc9f-176">0x00000010</span></span>                                                       |
| <span data-ttu-id="5dc9f-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5dc9f-177">Classes used in</span></span>        | [<span data-ttu-id="5dc9f-178">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-178">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5dc9f-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5dc9f-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5dc9f-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="5dc9f-180">Entry</span></span> | <span data-ttu-id="5dc9f-181">Значение</span><span class="sxs-lookup"><span data-stu-id="5dc9f-181">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5dc9f-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5dc9f-182">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dc9f-183">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dc9f-184">System-Only</span></span>            | <span data-ttu-id="5dc9f-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-185">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5dc9f-186">Is-Single-Valued</span></span>       | <span data-ttu-id="5dc9f-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-187">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5dc9f-188">Is Indexed</span></span>             | <span data-ttu-id="5dc9f-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-189">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5dc9f-190">In Global Catalog</span></span>      | <span data-ttu-id="5dc9f-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-191">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5dc9f-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dc9f-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5dc9f-193">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5dc9f-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dc9f-194">Range-Lower</span></span>            | <span data-ttu-id="5dc9f-195">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-195">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dc9f-196">Range-Upper</span></span>            | <span data-ttu-id="5dc9f-197">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-197">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-198">Search-Flags</span></span>           | <span data-ttu-id="5dc9f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dc9f-199">0x00000000</span></span>                                                       |
| <span data-ttu-id="5dc9f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-200">System-Flags</span></span>           | <span data-ttu-id="5dc9f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dc9f-201">0x00000010</span></span>                                                       |
| <span data-ttu-id="5dc9f-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5dc9f-202">Classes used in</span></span>        | [<span data-ttu-id="5dc9f-203">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-203">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5dc9f-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dc9f-204">Windows Server 2008</span></span>



| <span data-ttu-id="5dc9f-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="5dc9f-205">Entry</span></span> | <span data-ttu-id="5dc9f-206">Значение</span><span class="sxs-lookup"><span data-stu-id="5dc9f-206">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5dc9f-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5dc9f-207">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dc9f-208">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dc9f-209">System-Only</span></span>            | <span data-ttu-id="5dc9f-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-210">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5dc9f-211">Is-Single-Valued</span></span>       | <span data-ttu-id="5dc9f-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-212">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5dc9f-213">Is Indexed</span></span>             | <span data-ttu-id="5dc9f-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-214">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5dc9f-215">In Global Catalog</span></span>      | <span data-ttu-id="5dc9f-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-216">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5dc9f-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dc9f-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5dc9f-218">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5dc9f-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dc9f-219">Range-Lower</span></span>            | <span data-ttu-id="5dc9f-220">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-220">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dc9f-221">Range-Upper</span></span>            | <span data-ttu-id="5dc9f-222">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-222">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-223">Search-Flags</span></span>           | <span data-ttu-id="5dc9f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dc9f-224">0x00000000</span></span>                                                       |
| <span data-ttu-id="5dc9f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-225">System-Flags</span></span>           | <span data-ttu-id="5dc9f-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dc9f-226">0x00000010</span></span>                                                       |
| <span data-ttu-id="5dc9f-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5dc9f-227">Classes used in</span></span>        | [<span data-ttu-id="5dc9f-228">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-228">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5dc9f-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5dc9f-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5dc9f-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="5dc9f-230">Entry</span></span> | <span data-ttu-id="5dc9f-231">Значение</span><span class="sxs-lookup"><span data-stu-id="5dc9f-231">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5dc9f-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5dc9f-232">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dc9f-233">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dc9f-234">System-Only</span></span>            | <span data-ttu-id="5dc9f-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-235">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5dc9f-236">Is-Single-Valued</span></span>       | <span data-ttu-id="5dc9f-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-237">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5dc9f-238">Is Indexed</span></span>             | <span data-ttu-id="5dc9f-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-239">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5dc9f-240">In Global Catalog</span></span>      | <span data-ttu-id="5dc9f-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-241">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5dc9f-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dc9f-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5dc9f-243">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5dc9f-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dc9f-244">Range-Lower</span></span>            | <span data-ttu-id="5dc9f-245">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-245">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dc9f-246">Range-Upper</span></span>            | <span data-ttu-id="5dc9f-247">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-247">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-248">Search-Flags</span></span>           | <span data-ttu-id="5dc9f-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dc9f-249">0x00000000</span></span>                                                       |
| <span data-ttu-id="5dc9f-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-250">System-Flags</span></span>           | <span data-ttu-id="5dc9f-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dc9f-251">0x00000010</span></span>                                                       |
| <span data-ttu-id="5dc9f-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5dc9f-252">Classes used in</span></span>        | [<span data-ttu-id="5dc9f-253">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-253">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5dc9f-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5dc9f-254">Windows Server 2012</span></span>



| <span data-ttu-id="5dc9f-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="5dc9f-255">Entry</span></span> | <span data-ttu-id="5dc9f-256">Значение</span><span class="sxs-lookup"><span data-stu-id="5dc9f-256">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5dc9f-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5dc9f-257">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dc9f-258">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="5dc9f-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dc9f-259">System-Only</span></span>            | <span data-ttu-id="5dc9f-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-260">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5dc9f-261">Is-Single-Valued</span></span>       | <span data-ttu-id="5dc9f-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-262">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5dc9f-263">Is Indexed</span></span>             | <span data-ttu-id="5dc9f-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-264">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5dc9f-265">In Global Catalog</span></span>      | <span data-ttu-id="5dc9f-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="5dc9f-266">False</span></span>                                                            |
| <span data-ttu-id="5dc9f-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5dc9f-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dc9f-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5dc9f-268">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="5dc9f-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dc9f-269">Range-Lower</span></span>            | <span data-ttu-id="5dc9f-270">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-270">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dc9f-271">Range-Upper</span></span>            | <span data-ttu-id="5dc9f-272">36</span><span class="sxs-lookup"><span data-stu-id="5dc9f-272">36</span></span>                                                               |
| <span data-ttu-id="5dc9f-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-273">Search-Flags</span></span>           | <span data-ttu-id="5dc9f-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dc9f-274">0x00000000</span></span>                                                       |
| <span data-ttu-id="5dc9f-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dc9f-275">System-Flags</span></span>           | <span data-ttu-id="5dc9f-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dc9f-276">0x00000010</span></span>                                                       |
| <span data-ttu-id="5dc9f-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5dc9f-277">Classes used in</span></span>        | [<span data-ttu-id="5dc9f-278">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="5dc9f-278">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





