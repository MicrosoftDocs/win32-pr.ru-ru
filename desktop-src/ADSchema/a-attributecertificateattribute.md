---
title: атрибут Аттрибутецертификатеаттрибуте
description: Удостоверение и набор атрибутов с цифровой подписью или сертификатом. Используется для привязки данных авторизации к удостоверению.
ms.assetid: 46519f26-01db-4f8e-936d-9255c72cd30c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Аттрибутецертификатеаттрибуте
topic_type:
- apiref
api_name:
- attributeCertificateAttribute
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51005f0c919825a4496437661783857c927b7c6d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893137"
---
# <a name="attributecertificateattribute-attribute"></a><span data-ttu-id="9ab8e-105">атрибут Аттрибутецертификатеаттрибуте</span><span class="sxs-lookup"><span data-stu-id="9ab8e-105">attributeCertificateAttribute attribute</span></span>

<span data-ttu-id="9ab8e-106">Удостоверение и набор атрибутов с цифровой подписью или сертификатом.</span><span class="sxs-lookup"><span data-stu-id="9ab8e-106">A digitally signed or certified identity and set of attributes.</span></span> <span data-ttu-id="9ab8e-107">Используется для привязки данных авторизации к удостоверению.</span><span class="sxs-lookup"><span data-stu-id="9ab8e-107">Used to bind authorization information to an identity.</span></span>



| <span data-ttu-id="9ab8e-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ab8e-108">Entry</span></span> | <span data-ttu-id="9ab8e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab8e-109">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="9ab8e-110">CN</span><span class="sxs-lookup"><span data-stu-id="9ab8e-110">CN</span></span>                | <span data-ttu-id="9ab8e-111">аттрибутецертификатеаттрибуте</span><span class="sxs-lookup"><span data-stu-id="9ab8e-111">attributeCertificateAttribute</span></span>                         |
| <span data-ttu-id="9ab8e-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9ab8e-112">Ldap-Display-Name</span></span> | <span data-ttu-id="9ab8e-113">аттрибутецертификатеаттрибуте</span><span class="sxs-lookup"><span data-stu-id="9ab8e-113">attributeCertificateAttribute</span></span>                         |
| <span data-ttu-id="9ab8e-114">Размер</span><span class="sxs-lookup"><span data-stu-id="9ab8e-114">Size</span></span>              | \-                                                    |
| <span data-ttu-id="9ab8e-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9ab8e-115">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="9ab8e-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9ab8e-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="9ab8e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9ab8e-117">Attribute-Id</span></span>      | <span data-ttu-id="9ab8e-118">2.5.4.58</span><span class="sxs-lookup"><span data-stu-id="9ab8e-118">2.5.4.58</span></span>                                              |
| <span data-ttu-id="9ab8e-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9ab8e-119">System-Id-Guid</span></span>    | <span data-ttu-id="9ab8e-120">fa4693bb-7bc2-4cb9-81a8-c99c43b7905e</span><span class="sxs-lookup"><span data-stu-id="9ab8e-120">fa4693bb-7bc2-4cb9-81a8-c99c43b7905e</span></span>                  |
| <span data-ttu-id="9ab8e-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ab8e-121">Syntax</span></span>            | [<span data-ttu-id="9ab8e-122">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="9ab8e-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9ab8e-123">Implementations</span></span>

-   [<span data-ttu-id="9ab8e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9ab8e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9ab8e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9ab8e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9ab8e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9ab8e-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ab8e-129">Windows Server 2003</span></span>



| <span data-ttu-id="9ab8e-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ab8e-130">Entry</span></span> | <span data-ttu-id="9ab8e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab8e-131">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9ab8e-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ab8e-132">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab8e-133">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab8e-134">System-Only</span></span>            | <span data-ttu-id="9ab8e-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-135">False</span></span>                                 |
| <span data-ttu-id="9ab8e-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ab8e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab8e-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-137">False</span></span>                                 |
| <span data-ttu-id="9ab8e-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ab8e-138">Is Indexed</span></span>             | <span data-ttu-id="9ab8e-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-139">False</span></span>                                 |
| <span data-ttu-id="9ab8e-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ab8e-140">In Global Catalog</span></span>      | <span data-ttu-id="9ab8e-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-141">False</span></span>                                 |
| <span data-ttu-id="9ab8e-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ab8e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab8e-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ab8e-143">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9ab8e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab8e-144">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab8e-145">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-146">Search-Flags</span></span>           | <span data-ttu-id="9ab8e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-147">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-148">System-Flags</span></span>           | <span data-ttu-id="9ab8e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-149">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ab8e-150">Classes used in</span></span>        | [<span data-ttu-id="9ab8e-151">**Человек**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-151">**Person**</span></span>](c-person.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9ab8e-152">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9ab8e-152">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9ab8e-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ab8e-153">Entry</span></span> | <span data-ttu-id="9ab8e-154">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab8e-154">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9ab8e-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ab8e-155">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab8e-156">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab8e-157">System-Only</span></span>            | <span data-ttu-id="9ab8e-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-158">False</span></span>                                 |
| <span data-ttu-id="9ab8e-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ab8e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab8e-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-160">False</span></span>                                 |
| <span data-ttu-id="9ab8e-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ab8e-161">Is Indexed</span></span>             | <span data-ttu-id="9ab8e-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-162">False</span></span>                                 |
| <span data-ttu-id="9ab8e-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ab8e-163">In Global Catalog</span></span>      | <span data-ttu-id="9ab8e-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-164">False</span></span>                                 |
| <span data-ttu-id="9ab8e-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ab8e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab8e-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ab8e-166">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9ab8e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab8e-167">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab8e-168">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-169">Search-Flags</span></span>           | <span data-ttu-id="9ab8e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-170">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-171">System-Flags</span></span>           | <span data-ttu-id="9ab8e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-172">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ab8e-173">Classes used in</span></span>        | [<span data-ttu-id="9ab8e-174">**Человек**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-174">**Person**</span></span>](c-person.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9ab8e-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ab8e-175">Windows Server 2008</span></span>



| <span data-ttu-id="9ab8e-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ab8e-176">Entry</span></span> | <span data-ttu-id="9ab8e-177">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab8e-177">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9ab8e-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ab8e-178">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab8e-179">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab8e-180">System-Only</span></span>            | <span data-ttu-id="9ab8e-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-181">False</span></span>                                 |
| <span data-ttu-id="9ab8e-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ab8e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab8e-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-183">False</span></span>                                 |
| <span data-ttu-id="9ab8e-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ab8e-184">Is Indexed</span></span>             | <span data-ttu-id="9ab8e-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-185">False</span></span>                                 |
| <span data-ttu-id="9ab8e-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ab8e-186">In Global Catalog</span></span>      | <span data-ttu-id="9ab8e-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-187">False</span></span>                                 |
| <span data-ttu-id="9ab8e-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ab8e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab8e-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ab8e-189">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9ab8e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab8e-190">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab8e-191">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-192">Search-Flags</span></span>           | <span data-ttu-id="9ab8e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-193">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-194">System-Flags</span></span>           | <span data-ttu-id="9ab8e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-195">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ab8e-196">Classes used in</span></span>        | [<span data-ttu-id="9ab8e-197">**Человек**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-197">**Person**</span></span>](c-person.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9ab8e-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ab8e-198">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9ab8e-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ab8e-199">Entry</span></span> | <span data-ttu-id="9ab8e-200">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab8e-200">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9ab8e-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ab8e-201">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab8e-202">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab8e-203">System-Only</span></span>            | <span data-ttu-id="9ab8e-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-204">False</span></span>                                 |
| <span data-ttu-id="9ab8e-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ab8e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab8e-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-206">False</span></span>                                 |
| <span data-ttu-id="9ab8e-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ab8e-207">Is Indexed</span></span>             | <span data-ttu-id="9ab8e-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-208">False</span></span>                                 |
| <span data-ttu-id="9ab8e-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ab8e-209">In Global Catalog</span></span>      | <span data-ttu-id="9ab8e-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-210">False</span></span>                                 |
| <span data-ttu-id="9ab8e-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ab8e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab8e-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ab8e-212">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9ab8e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab8e-213">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab8e-214">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-215">Search-Flags</span></span>           | <span data-ttu-id="9ab8e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-216">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-217">System-Flags</span></span>           | <span data-ttu-id="9ab8e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-218">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ab8e-219">Classes used in</span></span>        | [<span data-ttu-id="9ab8e-220">**Человек**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-220">**Person**</span></span>](c-person.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9ab8e-221">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ab8e-221">Windows Server 2012</span></span>



| <span data-ttu-id="9ab8e-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ab8e-222">Entry</span></span> | <span data-ttu-id="9ab8e-223">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab8e-223">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="9ab8e-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ab8e-224">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab8e-225">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="9ab8e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab8e-226">System-Only</span></span>            | <span data-ttu-id="9ab8e-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-227">False</span></span>                                 |
| <span data-ttu-id="9ab8e-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ab8e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab8e-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-229">False</span></span>                                 |
| <span data-ttu-id="9ab8e-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ab8e-230">Is Indexed</span></span>             | <span data-ttu-id="9ab8e-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-231">False</span></span>                                 |
| <span data-ttu-id="9ab8e-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ab8e-232">In Global Catalog</span></span>      | <span data-ttu-id="9ab8e-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab8e-233">False</span></span>                                 |
| <span data-ttu-id="9ab8e-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ab8e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab8e-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ab8e-235">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="9ab8e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab8e-236">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab8e-237">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="9ab8e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-238">Search-Flags</span></span>           | <span data-ttu-id="9ab8e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-239">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab8e-240">System-Flags</span></span>           | <span data-ttu-id="9ab8e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab8e-241">0x00000000</span></span>                            |
| <span data-ttu-id="9ab8e-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ab8e-242">Classes used in</span></span>        | [<span data-ttu-id="9ab8e-243">**Человек**</span><span class="sxs-lookup"><span data-stu-id="9ab8e-243">**Person**</span></span>](c-person.md)<br/> |



 

 





