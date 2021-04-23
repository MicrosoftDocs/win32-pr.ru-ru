---
title: Upgrade — атрибут Product-Code
description: Этот атрибут содержит код продукта других пакетов, таких как приложения, которые могут быть обновлены этим пакетом или могут обновлять этот пакет.
ms.assetid: bf0ab06a-88a6-45af-ac9f-ee0ce648e51b
ms.tgt_platform: multiple
keywords:
- Обновление-схема AD атрибута кода продукта
- Схема AD атрибута Упградепродукткоде
topic_type:
- apiref
api_name:
- Upgrade-Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33734ec62665d301568f5f4152b39c5fbf4f94a6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655036"
---
# <a name="upgrade-product-code-attribute"></a><span data-ttu-id="80ca1-105">Upgrade — атрибут Product-Code</span><span class="sxs-lookup"><span data-stu-id="80ca1-105">Upgrade-Product-Code attribute</span></span>

<span data-ttu-id="80ca1-106">Этот атрибут содержит код продукта других пакетов, таких как приложения, которые могут быть обновлены этим пакетом или могут обновлять этот пакет.</span><span class="sxs-lookup"><span data-stu-id="80ca1-106">This attribute contains the product code of other packages, such as applications, that can be upgraded by this package, or that can upgrade this package.</span></span>



| <span data-ttu-id="80ca1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="80ca1-107">Entry</span></span> | <span data-ttu-id="80ca1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="80ca1-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="80ca1-109">CN</span><span class="sxs-lookup"><span data-stu-id="80ca1-109">CN</span></span>                | <span data-ttu-id="80ca1-110">Обновление — код продукта</span><span class="sxs-lookup"><span data-stu-id="80ca1-110">Upgrade-Product-Code</span></span>                                  |
| <span data-ttu-id="80ca1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="80ca1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="80ca1-112">упградепродукткоде</span><span class="sxs-lookup"><span data-stu-id="80ca1-112">upgradeProductCode</span></span>                                    |
| <span data-ttu-id="80ca1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="80ca1-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="80ca1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="80ca1-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="80ca1-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="80ca1-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="80ca1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="80ca1-116">Attribute-Id</span></span>      | <span data-ttu-id="80ca1-117">1.2.840.113556.1.4.813</span><span class="sxs-lookup"><span data-stu-id="80ca1-117">1.2.840.113556.1.4.813</span></span>                                |
| <span data-ttu-id="80ca1-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="80ca1-118">System-Id-Guid</span></span>    | <span data-ttu-id="80ca1-119">d9e18312-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="80ca1-119">d9e18312-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="80ca1-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80ca1-120">Syntax</span></span>            | [<span data-ttu-id="80ca1-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="80ca1-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="80ca1-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="80ca1-122">Implementations</span></span>

-   [<span data-ttu-id="80ca1-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="80ca1-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="80ca1-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="80ca1-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="80ca1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="80ca1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="80ca1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="80ca1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="80ca1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="80ca1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="80ca1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="80ca1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="80ca1-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80ca1-129">Windows 2000 Server</span></span>



| <span data-ttu-id="80ca1-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="80ca1-130">Entry</span></span> | <span data-ttu-id="80ca1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="80ca1-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="80ca1-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80ca1-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80ca1-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="80ca1-134">System-Only</span></span>            | <span data-ttu-id="80ca1-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-135">False</span></span>                                                            |
| <span data-ttu-id="80ca1-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80ca1-136">Is-Single-Valued</span></span>       | <span data-ttu-id="80ca1-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-137">False</span></span>                                                            |
| <span data-ttu-id="80ca1-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80ca1-138">Is Indexed</span></span>             | <span data-ttu-id="80ca1-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-139">False</span></span>                                                            |
| <span data-ttu-id="80ca1-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80ca1-140">In Global Catalog</span></span>      | <span data-ttu-id="80ca1-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-141">False</span></span>                                                            |
| <span data-ttu-id="80ca1-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80ca1-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="80ca1-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80ca1-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="80ca1-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80ca1-144">Range-Lower</span></span>            | <span data-ttu-id="80ca1-145">0</span><span class="sxs-lookup"><span data-stu-id="80ca1-145">0</span></span>                                                                |
| <span data-ttu-id="80ca1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80ca1-146">Range-Upper</span></span>            | <span data-ttu-id="80ca1-147">16</span><span class="sxs-lookup"><span data-stu-id="80ca1-147">16</span></span>                                                               |
| <span data-ttu-id="80ca1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-148">Search-Flags</span></span>           | <span data-ttu-id="80ca1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80ca1-149">0x00000000</span></span>                                                       |
| <span data-ttu-id="80ca1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-150">System-Flags</span></span>           | <span data-ttu-id="80ca1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80ca1-151">0x00000010</span></span>                                                       |
| <span data-ttu-id="80ca1-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80ca1-152">Classes used in</span></span>        | [<span data-ttu-id="80ca1-153">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="80ca1-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="80ca1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80ca1-154">Windows Server 2003</span></span>



| <span data-ttu-id="80ca1-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="80ca1-155">Entry</span></span> | <span data-ttu-id="80ca1-156">Значение</span><span class="sxs-lookup"><span data-stu-id="80ca1-156">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="80ca1-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80ca1-157">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80ca1-158">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="80ca1-159">System-Only</span></span>            | <span data-ttu-id="80ca1-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-160">False</span></span>                                                            |
| <span data-ttu-id="80ca1-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80ca1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="80ca1-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-162">False</span></span>                                                            |
| <span data-ttu-id="80ca1-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80ca1-163">Is Indexed</span></span>             | <span data-ttu-id="80ca1-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-164">False</span></span>                                                            |
| <span data-ttu-id="80ca1-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80ca1-165">In Global Catalog</span></span>      | <span data-ttu-id="80ca1-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-166">False</span></span>                                                            |
| <span data-ttu-id="80ca1-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80ca1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="80ca1-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80ca1-168">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="80ca1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80ca1-169">Range-Lower</span></span>            | <span data-ttu-id="80ca1-170">0</span><span class="sxs-lookup"><span data-stu-id="80ca1-170">0</span></span>                                                                |
| <span data-ttu-id="80ca1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80ca1-171">Range-Upper</span></span>            | <span data-ttu-id="80ca1-172">16</span><span class="sxs-lookup"><span data-stu-id="80ca1-172">16</span></span>                                                               |
| <span data-ttu-id="80ca1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-173">Search-Flags</span></span>           | <span data-ttu-id="80ca1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80ca1-174">0x00000000</span></span>                                                       |
| <span data-ttu-id="80ca1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-175">System-Flags</span></span>           | <span data-ttu-id="80ca1-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80ca1-176">0x00000010</span></span>                                                       |
| <span data-ttu-id="80ca1-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80ca1-177">Classes used in</span></span>        | [<span data-ttu-id="80ca1-178">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="80ca1-178">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="80ca1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="80ca1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="80ca1-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="80ca1-180">Entry</span></span> | <span data-ttu-id="80ca1-181">Значение</span><span class="sxs-lookup"><span data-stu-id="80ca1-181">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="80ca1-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80ca1-182">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80ca1-183">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="80ca1-184">System-Only</span></span>            | <span data-ttu-id="80ca1-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-185">False</span></span>                                                            |
| <span data-ttu-id="80ca1-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80ca1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="80ca1-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-187">False</span></span>                                                            |
| <span data-ttu-id="80ca1-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80ca1-188">Is Indexed</span></span>             | <span data-ttu-id="80ca1-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-189">False</span></span>                                                            |
| <span data-ttu-id="80ca1-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80ca1-190">In Global Catalog</span></span>      | <span data-ttu-id="80ca1-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-191">False</span></span>                                                            |
| <span data-ttu-id="80ca1-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80ca1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="80ca1-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80ca1-193">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="80ca1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80ca1-194">Range-Lower</span></span>            | <span data-ttu-id="80ca1-195">0</span><span class="sxs-lookup"><span data-stu-id="80ca1-195">0</span></span>                                                                |
| <span data-ttu-id="80ca1-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80ca1-196">Range-Upper</span></span>            | <span data-ttu-id="80ca1-197">16</span><span class="sxs-lookup"><span data-stu-id="80ca1-197">16</span></span>                                                               |
| <span data-ttu-id="80ca1-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-198">Search-Flags</span></span>           | <span data-ttu-id="80ca1-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80ca1-199">0x00000000</span></span>                                                       |
| <span data-ttu-id="80ca1-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-200">System-Flags</span></span>           | <span data-ttu-id="80ca1-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80ca1-201">0x00000010</span></span>                                                       |
| <span data-ttu-id="80ca1-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80ca1-202">Classes used in</span></span>        | [<span data-ttu-id="80ca1-203">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="80ca1-203">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="80ca1-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80ca1-204">Windows Server 2008</span></span>



| <span data-ttu-id="80ca1-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="80ca1-205">Entry</span></span> | <span data-ttu-id="80ca1-206">Значение</span><span class="sxs-lookup"><span data-stu-id="80ca1-206">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="80ca1-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80ca1-207">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80ca1-208">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="80ca1-209">System-Only</span></span>            | <span data-ttu-id="80ca1-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-210">False</span></span>                                                            |
| <span data-ttu-id="80ca1-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80ca1-211">Is-Single-Valued</span></span>       | <span data-ttu-id="80ca1-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-212">False</span></span>                                                            |
| <span data-ttu-id="80ca1-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80ca1-213">Is Indexed</span></span>             | <span data-ttu-id="80ca1-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-214">False</span></span>                                                            |
| <span data-ttu-id="80ca1-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80ca1-215">In Global Catalog</span></span>      | <span data-ttu-id="80ca1-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-216">False</span></span>                                                            |
| <span data-ttu-id="80ca1-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80ca1-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="80ca1-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80ca1-218">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="80ca1-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80ca1-219">Range-Lower</span></span>            | <span data-ttu-id="80ca1-220">0</span><span class="sxs-lookup"><span data-stu-id="80ca1-220">0</span></span>                                                                |
| <span data-ttu-id="80ca1-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80ca1-221">Range-Upper</span></span>            | <span data-ttu-id="80ca1-222">16</span><span class="sxs-lookup"><span data-stu-id="80ca1-222">16</span></span>                                                               |
| <span data-ttu-id="80ca1-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-223">Search-Flags</span></span>           | <span data-ttu-id="80ca1-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80ca1-224">0x00000000</span></span>                                                       |
| <span data-ttu-id="80ca1-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-225">System-Flags</span></span>           | <span data-ttu-id="80ca1-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80ca1-226">0x00000010</span></span>                                                       |
| <span data-ttu-id="80ca1-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80ca1-227">Classes used in</span></span>        | [<span data-ttu-id="80ca1-228">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="80ca1-228">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="80ca1-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80ca1-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="80ca1-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="80ca1-230">Entry</span></span> | <span data-ttu-id="80ca1-231">Значение</span><span class="sxs-lookup"><span data-stu-id="80ca1-231">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="80ca1-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80ca1-232">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80ca1-233">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="80ca1-234">System-Only</span></span>            | <span data-ttu-id="80ca1-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-235">False</span></span>                                                            |
| <span data-ttu-id="80ca1-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80ca1-236">Is-Single-Valued</span></span>       | <span data-ttu-id="80ca1-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-237">False</span></span>                                                            |
| <span data-ttu-id="80ca1-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80ca1-238">Is Indexed</span></span>             | <span data-ttu-id="80ca1-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-239">False</span></span>                                                            |
| <span data-ttu-id="80ca1-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80ca1-240">In Global Catalog</span></span>      | <span data-ttu-id="80ca1-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-241">False</span></span>                                                            |
| <span data-ttu-id="80ca1-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80ca1-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="80ca1-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80ca1-243">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="80ca1-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80ca1-244">Range-Lower</span></span>            | <span data-ttu-id="80ca1-245">0</span><span class="sxs-lookup"><span data-stu-id="80ca1-245">0</span></span>                                                                |
| <span data-ttu-id="80ca1-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80ca1-246">Range-Upper</span></span>            | <span data-ttu-id="80ca1-247">16</span><span class="sxs-lookup"><span data-stu-id="80ca1-247">16</span></span>                                                               |
| <span data-ttu-id="80ca1-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-248">Search-Flags</span></span>           | <span data-ttu-id="80ca1-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80ca1-249">0x00000000</span></span>                                                       |
| <span data-ttu-id="80ca1-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-250">System-Flags</span></span>           | <span data-ttu-id="80ca1-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80ca1-251">0x00000010</span></span>                                                       |
| <span data-ttu-id="80ca1-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80ca1-252">Classes used in</span></span>        | [<span data-ttu-id="80ca1-253">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="80ca1-253">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="80ca1-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80ca1-254">Windows Server 2012</span></span>



| <span data-ttu-id="80ca1-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="80ca1-255">Entry</span></span> | <span data-ttu-id="80ca1-256">Значение</span><span class="sxs-lookup"><span data-stu-id="80ca1-256">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="80ca1-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80ca1-257">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80ca1-258">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="80ca1-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="80ca1-259">System-Only</span></span>            | <span data-ttu-id="80ca1-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-260">False</span></span>                                                            |
| <span data-ttu-id="80ca1-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80ca1-261">Is-Single-Valued</span></span>       | <span data-ttu-id="80ca1-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-262">False</span></span>                                                            |
| <span data-ttu-id="80ca1-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80ca1-263">Is Indexed</span></span>             | <span data-ttu-id="80ca1-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-264">False</span></span>                                                            |
| <span data-ttu-id="80ca1-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80ca1-265">In Global Catalog</span></span>      | <span data-ttu-id="80ca1-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="80ca1-266">False</span></span>                                                            |
| <span data-ttu-id="80ca1-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80ca1-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="80ca1-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80ca1-268">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="80ca1-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80ca1-269">Range-Lower</span></span>            | <span data-ttu-id="80ca1-270">0</span><span class="sxs-lookup"><span data-stu-id="80ca1-270">0</span></span>                                                                |
| <span data-ttu-id="80ca1-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80ca1-271">Range-Upper</span></span>            | <span data-ttu-id="80ca1-272">16</span><span class="sxs-lookup"><span data-stu-id="80ca1-272">16</span></span>                                                               |
| <span data-ttu-id="80ca1-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-273">Search-Flags</span></span>           | <span data-ttu-id="80ca1-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80ca1-274">0x00000000</span></span>                                                       |
| <span data-ttu-id="80ca1-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80ca1-275">System-Flags</span></span>           | <span data-ttu-id="80ca1-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80ca1-276">0x00000010</span></span>                                                       |
| <span data-ttu-id="80ca1-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80ca1-277">Classes used in</span></span>        | [<span data-ttu-id="80ca1-278">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="80ca1-278">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





