---
title: Атрибут Product-Code
description: Этот атрибут содержит уникальный идентификатор приложения для конкретного выпуска продукта, представленного в виде строкового идентификатора GUID, например \ 0034; 12345678-1234-1234-1234-123456789012 \ 0034;.
ms.assetid: 1fb50a4c-1a6a-4231-a6b2-92f6bc4a1ead
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Product-Code
- Схема AD атрибута productCode
topic_type:
- apiref
api_name:
- Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dc874552fc819de4f9c58b23809b9f5662ee6e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989507"
---
# <a name="product-code-attribute"></a><span data-ttu-id="6100c-105">Атрибут Product-Code</span><span class="sxs-lookup"><span data-stu-id="6100c-105">Product-Code attribute</span></span>

<span data-ttu-id="6100c-106">Этот атрибут содержит уникальный идентификатор приложения для конкретного выпуска продукта, представленного в виде строкового GUID, например " {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="6100c-106">This attribute contains a unique identifier for an application for a particular product release, represented as a string GUID, for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="6100c-107">Буквы, используемые в этом GUID, должны быть прописными буквами.</span><span class="sxs-lookup"><span data-stu-id="6100c-107">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="6100c-108">Этот идентификатор должен различаться для разных версий и языков.</span><span class="sxs-lookup"><span data-stu-id="6100c-108">This ID must vary for different versions and languages.</span></span>



| <span data-ttu-id="6100c-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="6100c-109">Entry</span></span> | <span data-ttu-id="6100c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6100c-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6100c-111">CN</span><span class="sxs-lookup"><span data-stu-id="6100c-111">CN</span></span>                | <span data-ttu-id="6100c-112">Product-Code</span><span class="sxs-lookup"><span data-stu-id="6100c-112">Product-Code</span></span>                                          |
| <span data-ttu-id="6100c-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6100c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6100c-114">productCode</span><span class="sxs-lookup"><span data-stu-id="6100c-114">productCode</span></span>                                           |
| <span data-ttu-id="6100c-115">Размер</span><span class="sxs-lookup"><span data-stu-id="6100c-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6100c-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6100c-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="6100c-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6100c-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6100c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6100c-118">Attribute-Id</span></span>      | <span data-ttu-id="6100c-119">1.2.840.113556.1.4.818</span><span class="sxs-lookup"><span data-stu-id="6100c-119">1.2.840.113556.1.4.818</span></span>                                |
| <span data-ttu-id="6100c-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6100c-120">System-Id-Guid</span></span>    | <span data-ttu-id="6100c-121">d9e18317-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6100c-121">d9e18317-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="6100c-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6100c-122">Syntax</span></span>            | [<span data-ttu-id="6100c-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="6100c-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6100c-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6100c-124">Implementations</span></span>

-   [<span data-ttu-id="6100c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6100c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6100c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6100c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6100c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6100c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6100c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6100c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6100c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6100c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6100c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6100c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6100c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6100c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6100c-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="6100c-132">Entry</span></span> | <span data-ttu-id="6100c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6100c-133">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6100c-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6100c-134">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6100c-135">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6100c-136">System-Only</span></span>            | <span data-ttu-id="6100c-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-137">False</span></span>                                                            |
| <span data-ttu-id="6100c-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6100c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6100c-139">True</span><span class="sxs-lookup"><span data-stu-id="6100c-139">True</span></span>                                                             |
| <span data-ttu-id="6100c-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6100c-140">Is Indexed</span></span>             | <span data-ttu-id="6100c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-141">False</span></span>                                                            |
| <span data-ttu-id="6100c-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6100c-142">In Global Catalog</span></span>      | <span data-ttu-id="6100c-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-143">False</span></span>                                                            |
| <span data-ttu-id="6100c-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6100c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6100c-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6100c-145">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6100c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6100c-146">Range-Lower</span></span>            | <span data-ttu-id="6100c-147">0</span><span class="sxs-lookup"><span data-stu-id="6100c-147">0</span></span>                                                                |
| <span data-ttu-id="6100c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6100c-148">Range-Upper</span></span>            | <span data-ttu-id="6100c-149">16</span><span class="sxs-lookup"><span data-stu-id="6100c-149">16</span></span>                                                               |
| <span data-ttu-id="6100c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-150">Search-Flags</span></span>           | <span data-ttu-id="6100c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6100c-151">0x00000000</span></span>                                                       |
| <span data-ttu-id="6100c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-152">System-Flags</span></span>           | <span data-ttu-id="6100c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6100c-153">0x00000010</span></span>                                                       |
| <span data-ttu-id="6100c-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6100c-154">Classes used in</span></span>        | [<span data-ttu-id="6100c-155">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="6100c-155">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6100c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6100c-156">Windows Server 2003</span></span>



| <span data-ttu-id="6100c-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="6100c-157">Entry</span></span> | <span data-ttu-id="6100c-158">Значение</span><span class="sxs-lookup"><span data-stu-id="6100c-158">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6100c-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6100c-159">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6100c-160">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6100c-161">System-Only</span></span>            | <span data-ttu-id="6100c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-162">False</span></span>                                                            |
| <span data-ttu-id="6100c-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6100c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6100c-164">True</span><span class="sxs-lookup"><span data-stu-id="6100c-164">True</span></span>                                                             |
| <span data-ttu-id="6100c-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6100c-165">Is Indexed</span></span>             | <span data-ttu-id="6100c-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-166">False</span></span>                                                            |
| <span data-ttu-id="6100c-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6100c-167">In Global Catalog</span></span>      | <span data-ttu-id="6100c-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-168">False</span></span>                                                            |
| <span data-ttu-id="6100c-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6100c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6100c-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6100c-170">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6100c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6100c-171">Range-Lower</span></span>            | <span data-ttu-id="6100c-172">0</span><span class="sxs-lookup"><span data-stu-id="6100c-172">0</span></span>                                                                |
| <span data-ttu-id="6100c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6100c-173">Range-Upper</span></span>            | <span data-ttu-id="6100c-174">16</span><span class="sxs-lookup"><span data-stu-id="6100c-174">16</span></span>                                                               |
| <span data-ttu-id="6100c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-175">Search-Flags</span></span>           | <span data-ttu-id="6100c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6100c-176">0x00000000</span></span>                                                       |
| <span data-ttu-id="6100c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-177">System-Flags</span></span>           | <span data-ttu-id="6100c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6100c-178">0x00000010</span></span>                                                       |
| <span data-ttu-id="6100c-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6100c-179">Classes used in</span></span>        | [<span data-ttu-id="6100c-180">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="6100c-180">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6100c-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6100c-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6100c-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="6100c-182">Entry</span></span> | <span data-ttu-id="6100c-183">Значение</span><span class="sxs-lookup"><span data-stu-id="6100c-183">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6100c-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6100c-184">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6100c-185">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6100c-186">System-Only</span></span>            | <span data-ttu-id="6100c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-187">False</span></span>                                                            |
| <span data-ttu-id="6100c-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6100c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6100c-189">True</span><span class="sxs-lookup"><span data-stu-id="6100c-189">True</span></span>                                                             |
| <span data-ttu-id="6100c-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6100c-190">Is Indexed</span></span>             | <span data-ttu-id="6100c-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-191">False</span></span>                                                            |
| <span data-ttu-id="6100c-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6100c-192">In Global Catalog</span></span>      | <span data-ttu-id="6100c-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-193">False</span></span>                                                            |
| <span data-ttu-id="6100c-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6100c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6100c-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6100c-195">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6100c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6100c-196">Range-Lower</span></span>            | <span data-ttu-id="6100c-197">0</span><span class="sxs-lookup"><span data-stu-id="6100c-197">0</span></span>                                                                |
| <span data-ttu-id="6100c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6100c-198">Range-Upper</span></span>            | <span data-ttu-id="6100c-199">16</span><span class="sxs-lookup"><span data-stu-id="6100c-199">16</span></span>                                                               |
| <span data-ttu-id="6100c-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-200">Search-Flags</span></span>           | <span data-ttu-id="6100c-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6100c-201">0x00000000</span></span>                                                       |
| <span data-ttu-id="6100c-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-202">System-Flags</span></span>           | <span data-ttu-id="6100c-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6100c-203">0x00000010</span></span>                                                       |
| <span data-ttu-id="6100c-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6100c-204">Classes used in</span></span>        | [<span data-ttu-id="6100c-205">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="6100c-205">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6100c-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6100c-206">Windows Server 2008</span></span>



| <span data-ttu-id="6100c-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="6100c-207">Entry</span></span> | <span data-ttu-id="6100c-208">Значение</span><span class="sxs-lookup"><span data-stu-id="6100c-208">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6100c-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6100c-209">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6100c-210">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6100c-211">System-Only</span></span>            | <span data-ttu-id="6100c-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-212">False</span></span>                                                            |
| <span data-ttu-id="6100c-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6100c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6100c-214">True</span><span class="sxs-lookup"><span data-stu-id="6100c-214">True</span></span>                                                             |
| <span data-ttu-id="6100c-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6100c-215">Is Indexed</span></span>             | <span data-ttu-id="6100c-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-216">False</span></span>                                                            |
| <span data-ttu-id="6100c-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6100c-217">In Global Catalog</span></span>      | <span data-ttu-id="6100c-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-218">False</span></span>                                                            |
| <span data-ttu-id="6100c-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6100c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6100c-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6100c-220">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6100c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6100c-221">Range-Lower</span></span>            | <span data-ttu-id="6100c-222">0</span><span class="sxs-lookup"><span data-stu-id="6100c-222">0</span></span>                                                                |
| <span data-ttu-id="6100c-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6100c-223">Range-Upper</span></span>            | <span data-ttu-id="6100c-224">16</span><span class="sxs-lookup"><span data-stu-id="6100c-224">16</span></span>                                                               |
| <span data-ttu-id="6100c-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-225">Search-Flags</span></span>           | <span data-ttu-id="6100c-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6100c-226">0x00000000</span></span>                                                       |
| <span data-ttu-id="6100c-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-227">System-Flags</span></span>           | <span data-ttu-id="6100c-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6100c-228">0x00000010</span></span>                                                       |
| <span data-ttu-id="6100c-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6100c-229">Classes used in</span></span>        | [<span data-ttu-id="6100c-230">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="6100c-230">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6100c-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6100c-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6100c-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="6100c-232">Entry</span></span> | <span data-ttu-id="6100c-233">Значение</span><span class="sxs-lookup"><span data-stu-id="6100c-233">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6100c-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6100c-234">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6100c-235">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="6100c-236">System-Only</span></span>            | <span data-ttu-id="6100c-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-237">False</span></span>                                                            |
| <span data-ttu-id="6100c-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6100c-238">Is-Single-Valued</span></span>       | <span data-ttu-id="6100c-239">True</span><span class="sxs-lookup"><span data-stu-id="6100c-239">True</span></span>                                                             |
| <span data-ttu-id="6100c-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6100c-240">Is Indexed</span></span>             | <span data-ttu-id="6100c-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-241">False</span></span>                                                            |
| <span data-ttu-id="6100c-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6100c-242">In Global Catalog</span></span>      | <span data-ttu-id="6100c-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-243">False</span></span>                                                            |
| <span data-ttu-id="6100c-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6100c-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="6100c-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6100c-245">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6100c-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6100c-246">Range-Lower</span></span>            | <span data-ttu-id="6100c-247">0</span><span class="sxs-lookup"><span data-stu-id="6100c-247">0</span></span>                                                                |
| <span data-ttu-id="6100c-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6100c-248">Range-Upper</span></span>            | <span data-ttu-id="6100c-249">16</span><span class="sxs-lookup"><span data-stu-id="6100c-249">16</span></span>                                                               |
| <span data-ttu-id="6100c-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-250">Search-Flags</span></span>           | <span data-ttu-id="6100c-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6100c-251">0x00000000</span></span>                                                       |
| <span data-ttu-id="6100c-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-252">System-Flags</span></span>           | <span data-ttu-id="6100c-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6100c-253">0x00000010</span></span>                                                       |
| <span data-ttu-id="6100c-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6100c-254">Classes used in</span></span>        | [<span data-ttu-id="6100c-255">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="6100c-255">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6100c-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6100c-256">Windows Server 2012</span></span>



| <span data-ttu-id="6100c-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="6100c-257">Entry</span></span> | <span data-ttu-id="6100c-258">Значение</span><span class="sxs-lookup"><span data-stu-id="6100c-258">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6100c-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6100c-259">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6100c-260">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6100c-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="6100c-261">System-Only</span></span>            | <span data-ttu-id="6100c-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-262">False</span></span>                                                            |
| <span data-ttu-id="6100c-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6100c-263">Is-Single-Valued</span></span>       | <span data-ttu-id="6100c-264">True</span><span class="sxs-lookup"><span data-stu-id="6100c-264">True</span></span>                                                             |
| <span data-ttu-id="6100c-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6100c-265">Is Indexed</span></span>             | <span data-ttu-id="6100c-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-266">False</span></span>                                                            |
| <span data-ttu-id="6100c-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6100c-267">In Global Catalog</span></span>      | <span data-ttu-id="6100c-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="6100c-268">False</span></span>                                                            |
| <span data-ttu-id="6100c-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6100c-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="6100c-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6100c-270">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6100c-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6100c-271">Range-Lower</span></span>            | <span data-ttu-id="6100c-272">0</span><span class="sxs-lookup"><span data-stu-id="6100c-272">0</span></span>                                                                |
| <span data-ttu-id="6100c-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6100c-273">Range-Upper</span></span>            | <span data-ttu-id="6100c-274">16</span><span class="sxs-lookup"><span data-stu-id="6100c-274">16</span></span>                                                               |
| <span data-ttu-id="6100c-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-275">Search-Flags</span></span>           | <span data-ttu-id="6100c-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6100c-276">0x00000000</span></span>                                                       |
| <span data-ttu-id="6100c-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6100c-277">System-Flags</span></span>           | <span data-ttu-id="6100c-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6100c-278">0x00000010</span></span>                                                       |
| <span data-ttu-id="6100c-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6100c-279">Classes used in</span></span>        | [<span data-ttu-id="6100c-280">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="6100c-280">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





