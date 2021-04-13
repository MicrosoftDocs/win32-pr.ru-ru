---
title: атрибут Лабеледури
description: Универсальный идентификатор ресурса, за которым следует метка.
ms.assetid: 214b5b4b-7389-4801-977c-24ffc2e025bd
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Лабеледури
topic_type:
- apiref
api_name:
- labeledURI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bcfae6b1d2029fd916cf2e796e611a6b76318bc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493587"
---
# <a name="labeleduri-attribute"></a><span data-ttu-id="e6675-104">атрибут Лабеледури</span><span class="sxs-lookup"><span data-stu-id="e6675-104">labeledURI attribute</span></span>

<span data-ttu-id="e6675-105">Универсальный идентификатор ресурса, за которым следует метка.</span><span class="sxs-lookup"><span data-stu-id="e6675-105">A Uniform Resource Identifier followed by a label.</span></span> <span data-ttu-id="e6675-106">Метка используется для описания ресурса, на который указывает URI, и служит в качестве отображаемого имени, читаемого человеком.</span><span class="sxs-lookup"><span data-stu-id="e6675-106">The label is used to describe the resource to which the URI points, and is intended as a display name that is human-readable.</span></span>



| <span data-ttu-id="e6675-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6675-107">Entry</span></span> | <span data-ttu-id="e6675-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e6675-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e6675-109">CN</span><span class="sxs-lookup"><span data-stu-id="e6675-109">CN</span></span>                | <span data-ttu-id="e6675-110">лабеледури</span><span class="sxs-lookup"><span data-stu-id="e6675-110">labeledURI</span></span>                                  |
| <span data-ttu-id="e6675-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e6675-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e6675-112">лабеледури</span><span class="sxs-lookup"><span data-stu-id="e6675-112">labeledURI</span></span>                                  |
| <span data-ttu-id="e6675-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e6675-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e6675-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e6675-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e6675-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e6675-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e6675-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e6675-116">Attribute-Id</span></span>      | <span data-ttu-id="e6675-117">1.3.6.1.4.1.250.1.57</span><span class="sxs-lookup"><span data-stu-id="e6675-117">1.3.6.1.4.1.250.1.57</span></span>                        |
| <span data-ttu-id="e6675-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e6675-118">System-Id-Guid</span></span>    | <span data-ttu-id="e6675-119">c569bb46-c680-44bc-a273-e6c227d71b45</span><span class="sxs-lookup"><span data-stu-id="e6675-119">c569bb46-c680-44bc-a273-e6c227d71b45</span></span>        |
| <span data-ttu-id="e6675-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6675-120">Syntax</span></span>            | [<span data-ttu-id="e6675-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e6675-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e6675-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e6675-122">Implementations</span></span>

-   [<span data-ttu-id="e6675-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e6675-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e6675-124">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e6675-124">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e6675-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e6675-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e6675-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e6675-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e6675-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e6675-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e6675-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e6675-128">Windows Server 2003</span></span>



| <span data-ttu-id="e6675-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6675-129">Entry</span></span> | <span data-ttu-id="e6675-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e6675-130">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6675-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6675-131">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6675-132">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6675-133">System-Only</span></span>            | <span data-ttu-id="e6675-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-134">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6675-135">Is-Single-Valued</span></span>       | <span data-ttu-id="e6675-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-136">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6675-137">Is Indexed</span></span>             | <span data-ttu-id="e6675-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-138">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6675-139">In Global Catalog</span></span>      | <span data-ttu-id="e6675-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-140">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6675-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6675-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6675-142">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e6675-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6675-143">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6675-144">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-145">Search-Flags</span></span>           | <span data-ttu-id="e6675-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-146">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-147">System-Flags</span></span>           | <span data-ttu-id="e6675-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-148">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-149">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6675-149">Classes used in</span></span>        | [<span data-ttu-id="e6675-150">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e6675-150">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e6675-151">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="e6675-151">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="e6675-152">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e6675-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e6675-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e6675-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e6675-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6675-154">Entry</span></span> | <span data-ttu-id="e6675-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e6675-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6675-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6675-156">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6675-157">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6675-158">System-Only</span></span>            | <span data-ttu-id="e6675-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-159">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6675-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e6675-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-161">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6675-162">Is Indexed</span></span>             | <span data-ttu-id="e6675-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-163">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6675-164">In Global Catalog</span></span>      | <span data-ttu-id="e6675-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-165">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6675-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6675-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6675-167">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e6675-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6675-168">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6675-169">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-170">Search-Flags</span></span>           | <span data-ttu-id="e6675-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-171">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-172">System-Flags</span></span>           | <span data-ttu-id="e6675-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-173">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6675-174">Classes used in</span></span>        | [<span data-ttu-id="e6675-175">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e6675-175">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e6675-176">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="e6675-176">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="e6675-177">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e6675-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e6675-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6675-178">Windows Server 2008</span></span>



| <span data-ttu-id="e6675-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6675-179">Entry</span></span> | <span data-ttu-id="e6675-180">Значение</span><span class="sxs-lookup"><span data-stu-id="e6675-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6675-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6675-181">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6675-182">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6675-183">System-Only</span></span>            | <span data-ttu-id="e6675-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-184">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6675-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e6675-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-186">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6675-187">Is Indexed</span></span>             | <span data-ttu-id="e6675-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-188">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6675-189">In Global Catalog</span></span>      | <span data-ttu-id="e6675-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-190">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6675-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6675-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6675-192">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e6675-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6675-193">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6675-194">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-195">Search-Flags</span></span>           | <span data-ttu-id="e6675-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-196">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-197">System-Flags</span></span>           | <span data-ttu-id="e6675-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-198">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6675-199">Classes used in</span></span>        | [<span data-ttu-id="e6675-200">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e6675-200">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e6675-201">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="e6675-201">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="e6675-202">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e6675-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e6675-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6675-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e6675-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6675-204">Entry</span></span> | <span data-ttu-id="e6675-205">Значение</span><span class="sxs-lookup"><span data-stu-id="e6675-205">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6675-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6675-206">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6675-207">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6675-208">System-Only</span></span>            | <span data-ttu-id="e6675-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-209">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6675-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e6675-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-211">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6675-212">Is Indexed</span></span>             | <span data-ttu-id="e6675-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-213">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6675-214">In Global Catalog</span></span>      | <span data-ttu-id="e6675-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-215">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6675-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6675-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6675-217">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e6675-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6675-218">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6675-219">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-220">Search-Flags</span></span>           | <span data-ttu-id="e6675-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-221">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-222">System-Flags</span></span>           | <span data-ttu-id="e6675-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-223">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6675-224">Classes used in</span></span>        | [<span data-ttu-id="e6675-225">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e6675-225">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e6675-226">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="e6675-226">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="e6675-227">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e6675-227">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e6675-228">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6675-228">Windows Server 2012</span></span>



| <span data-ttu-id="e6675-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="e6675-229">Entry</span></span> | <span data-ttu-id="e6675-230">Значение</span><span class="sxs-lookup"><span data-stu-id="e6675-230">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6675-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e6675-231">Link-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6675-232">MAPI-Id</span></span>                | \-                                                                                                                                         |
| <span data-ttu-id="e6675-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6675-233">System-Only</span></span>            | <span data-ttu-id="e6675-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-234">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e6675-235">Is-Single-Valued</span></span>       | <span data-ttu-id="e6675-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-236">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e6675-237">Is Indexed</span></span>             | <span data-ttu-id="e6675-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-238">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e6675-239">In Global Catalog</span></span>      | <span data-ttu-id="e6675-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="e6675-240">False</span></span>                                                                                                                                      |
| <span data-ttu-id="e6675-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e6675-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6675-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e6675-242">O:BAG:BAD:S:</span></span>                                                                                                                               |
| <span data-ttu-id="e6675-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6675-243">Range-Lower</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6675-244">Range-Upper</span></span>            | \-                                                                                                                                         |
| <span data-ttu-id="e6675-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-245">Search-Flags</span></span>           | <span data-ttu-id="e6675-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-246">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6675-247">System-Flags</span></span>           | <span data-ttu-id="e6675-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6675-248">0x00000000</span></span>                                                                                                                                 |
| <span data-ttu-id="e6675-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e6675-249">Classes used in</span></span>        | [<span data-ttu-id="e6675-250">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="e6675-250">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="e6675-251">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="e6675-251">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="e6675-252">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="e6675-252">**User**</span></span>](c-user.md)<br/> |



 

 





