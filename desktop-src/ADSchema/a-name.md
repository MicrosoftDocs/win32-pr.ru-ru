---
title: Атрибут RDN
description: Относительное различающееся имя (RDN) объекта.
ms.assetid: 07fe0e81-1b18-4dbb-abca-a059a8bf993e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута RDN
- имя атрибута схемы AD
topic_type:
- apiref
api_name:
- RDN
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe49bd525d0fa3f4ed95874f2020d9d2a5eb9554
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655344"
---
# <a name="rdn-attribute"></a><span data-ttu-id="f1935-105">Атрибут RDN</span><span class="sxs-lookup"><span data-stu-id="f1935-105">RDN attribute</span></span>

<span data-ttu-id="f1935-106">Относительное различающееся имя (RDN) объекта.</span><span class="sxs-lookup"><span data-stu-id="f1935-106">The Relative Distinguished Name (RDN) of an object.</span></span> <span data-ttu-id="f1935-107">RDN — это относительная часть различающегося имени (DN), однозначно определяющая объект LDAP.</span><span class="sxs-lookup"><span data-stu-id="f1935-107">An RDN is the relative portion of a distinguished name (DN), which uniquely identifies an LDAP object.</span></span>



| <span data-ttu-id="f1935-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="f1935-108">Entry</span></span> | <span data-ttu-id="f1935-109">Значение</span><span class="sxs-lookup"><span data-stu-id="f1935-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="f1935-110">CN</span><span class="sxs-lookup"><span data-stu-id="f1935-110">CN</span></span>                | <span data-ttu-id="f1935-111">RDN</span><span class="sxs-lookup"><span data-stu-id="f1935-111">RDN</span></span>                                            |
| <span data-ttu-id="f1935-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f1935-112">Ldap-Display-Name</span></span> | <span data-ttu-id="f1935-113">name</span><span class="sxs-lookup"><span data-stu-id="f1935-113">name</span></span>                                           |
| <span data-ttu-id="f1935-114">Размер</span><span class="sxs-lookup"><span data-stu-id="f1935-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="f1935-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f1935-115">Update Privilege</span></span>  | <span data-ttu-id="f1935-116">Это значение задается администратором схемы.</span><span class="sxs-lookup"><span data-stu-id="f1935-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="f1935-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f1935-117">Update Frequency</span></span>  | \-                                             |
| <span data-ttu-id="f1935-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f1935-118">Attribute-Id</span></span>      | <span data-ttu-id="f1935-119">1.2.840.113556.1.4.1</span><span class="sxs-lookup"><span data-stu-id="f1935-119">1.2.840.113556.1.4.1</span></span>                           |
| <span data-ttu-id="f1935-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f1935-120">System-Id-Guid</span></span>    | <span data-ttu-id="f1935-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f1935-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="f1935-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1935-122">Syntax</span></span>            | [<span data-ttu-id="f1935-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="f1935-123">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="f1935-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f1935-124">Implementations</span></span>

-   [<span data-ttu-id="f1935-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f1935-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f1935-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f1935-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f1935-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f1935-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f1935-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f1935-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f1935-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f1935-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f1935-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f1935-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f1935-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f1935-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f1935-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1935-132">Windows 2000 Server</span></span>



| <span data-ttu-id="f1935-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="f1935-133">Entry</span></span> | <span data-ttu-id="f1935-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f1935-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1935-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f1935-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1935-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1935-136">MAPI-Id</span></span>                | <span data-ttu-id="f1935-137">0x8202</span><span class="sxs-lookup"><span data-stu-id="f1935-137">0x8202</span></span>                          |
| <span data-ttu-id="f1935-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1935-138">System-Only</span></span>            | <span data-ttu-id="f1935-139">True</span><span class="sxs-lookup"><span data-stu-id="f1935-139">True</span></span>                            |
| <span data-ttu-id="f1935-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f1935-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f1935-141">True</span><span class="sxs-lookup"><span data-stu-id="f1935-141">True</span></span>                            |
| <span data-ttu-id="f1935-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f1935-142">Is Indexed</span></span>             | <span data-ttu-id="f1935-143">True</span><span class="sxs-lookup"><span data-stu-id="f1935-143">True</span></span>                            |
| <span data-ttu-id="f1935-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f1935-144">In Global Catalog</span></span>      | <span data-ttu-id="f1935-145">True</span><span class="sxs-lookup"><span data-stu-id="f1935-145">True</span></span>                            |
| <span data-ttu-id="f1935-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f1935-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1935-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f1935-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1935-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1935-148">Range-Lower</span></span>            | <span data-ttu-id="f1935-149">1</span><span class="sxs-lookup"><span data-stu-id="f1935-149">1</span></span>                               |
| <span data-ttu-id="f1935-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1935-150">Range-Upper</span></span>            | <span data-ttu-id="f1935-151">255</span><span class="sxs-lookup"><span data-stu-id="f1935-151">255</span></span>                             |
| <span data-ttu-id="f1935-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-152">Search-Flags</span></span>           | <span data-ttu-id="f1935-153">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f1935-153">0x0000000D</span></span>                      |
| <span data-ttu-id="f1935-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-154">System-Flags</span></span>           | <span data-ttu-id="f1935-155">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f1935-155">0x00000012</span></span>                      |
| <span data-ttu-id="f1935-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f1935-156">Classes used in</span></span>        | [<span data-ttu-id="f1935-157">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f1935-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f1935-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1935-158">Windows Server 2003</span></span>



| <span data-ttu-id="f1935-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="f1935-159">Entry</span></span> | <span data-ttu-id="f1935-160">Значение</span><span class="sxs-lookup"><span data-stu-id="f1935-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1935-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f1935-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1935-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1935-162">MAPI-Id</span></span>                | <span data-ttu-id="f1935-163">0x8202</span><span class="sxs-lookup"><span data-stu-id="f1935-163">0x8202</span></span>                          |
| <span data-ttu-id="f1935-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1935-164">System-Only</span></span>            | <span data-ttu-id="f1935-165">True</span><span class="sxs-lookup"><span data-stu-id="f1935-165">True</span></span>                            |
| <span data-ttu-id="f1935-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f1935-166">Is-Single-Valued</span></span>       | <span data-ttu-id="f1935-167">True</span><span class="sxs-lookup"><span data-stu-id="f1935-167">True</span></span>                            |
| <span data-ttu-id="f1935-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f1935-168">Is Indexed</span></span>             | <span data-ttu-id="f1935-169">True</span><span class="sxs-lookup"><span data-stu-id="f1935-169">True</span></span>                            |
| <span data-ttu-id="f1935-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f1935-170">In Global Catalog</span></span>      | <span data-ttu-id="f1935-171">True</span><span class="sxs-lookup"><span data-stu-id="f1935-171">True</span></span>                            |
| <span data-ttu-id="f1935-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f1935-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1935-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f1935-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1935-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1935-174">Range-Lower</span></span>            | <span data-ttu-id="f1935-175">1</span><span class="sxs-lookup"><span data-stu-id="f1935-175">1</span></span>                               |
| <span data-ttu-id="f1935-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1935-176">Range-Upper</span></span>            | <span data-ttu-id="f1935-177">255</span><span class="sxs-lookup"><span data-stu-id="f1935-177">255</span></span>                             |
| <span data-ttu-id="f1935-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-178">Search-Flags</span></span>           | <span data-ttu-id="f1935-179">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f1935-179">0x0000000D</span></span>                      |
| <span data-ttu-id="f1935-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-180">System-Flags</span></span>           | <span data-ttu-id="f1935-181">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f1935-181">0x00000012</span></span>                      |
| <span data-ttu-id="f1935-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f1935-182">Classes used in</span></span>        | [<span data-ttu-id="f1935-183">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f1935-183">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f1935-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="f1935-184">ADAM</span></span>



| <span data-ttu-id="f1935-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="f1935-185">Entry</span></span> | <span data-ttu-id="f1935-186">Значение</span><span class="sxs-lookup"><span data-stu-id="f1935-186">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1935-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f1935-187">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1935-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1935-188">MAPI-Id</span></span>                | <span data-ttu-id="f1935-189">0x8202</span><span class="sxs-lookup"><span data-stu-id="f1935-189">0x8202</span></span>                          |
| <span data-ttu-id="f1935-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1935-190">System-Only</span></span>            | <span data-ttu-id="f1935-191">True</span><span class="sxs-lookup"><span data-stu-id="f1935-191">True</span></span>                            |
| <span data-ttu-id="f1935-192">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f1935-192">Is-Single-Valued</span></span>       | <span data-ttu-id="f1935-193">True</span><span class="sxs-lookup"><span data-stu-id="f1935-193">True</span></span>                            |
| <span data-ttu-id="f1935-194">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f1935-194">Is Indexed</span></span>             | <span data-ttu-id="f1935-195">True</span><span class="sxs-lookup"><span data-stu-id="f1935-195">True</span></span>                            |
| <span data-ttu-id="f1935-196">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f1935-196">In Global Catalog</span></span>      | <span data-ttu-id="f1935-197">True</span><span class="sxs-lookup"><span data-stu-id="f1935-197">True</span></span>                            |
| <span data-ttu-id="f1935-198">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f1935-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1935-199">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f1935-199">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1935-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1935-200">Range-Lower</span></span>            | <span data-ttu-id="f1935-201">1</span><span class="sxs-lookup"><span data-stu-id="f1935-201">1</span></span>                               |
| <span data-ttu-id="f1935-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1935-202">Range-Upper</span></span>            | <span data-ttu-id="f1935-203">255</span><span class="sxs-lookup"><span data-stu-id="f1935-203">255</span></span>                             |
| <span data-ttu-id="f1935-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-204">Search-Flags</span></span>           | <span data-ttu-id="f1935-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f1935-205">0x0000000D</span></span>                      |
| <span data-ttu-id="f1935-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-206">System-Flags</span></span>           | <span data-ttu-id="f1935-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f1935-207">0x00000012</span></span>                      |
| <span data-ttu-id="f1935-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f1935-208">Classes used in</span></span>        | [<span data-ttu-id="f1935-209">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f1935-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f1935-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f1935-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f1935-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="f1935-211">Entry</span></span> | <span data-ttu-id="f1935-212">Значение</span><span class="sxs-lookup"><span data-stu-id="f1935-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1935-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f1935-213">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1935-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1935-214">MAPI-Id</span></span>                | <span data-ttu-id="f1935-215">0x8202</span><span class="sxs-lookup"><span data-stu-id="f1935-215">0x8202</span></span>                          |
| <span data-ttu-id="f1935-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1935-216">System-Only</span></span>            | <span data-ttu-id="f1935-217">True</span><span class="sxs-lookup"><span data-stu-id="f1935-217">True</span></span>                            |
| <span data-ttu-id="f1935-218">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f1935-218">Is-Single-Valued</span></span>       | <span data-ttu-id="f1935-219">True</span><span class="sxs-lookup"><span data-stu-id="f1935-219">True</span></span>                            |
| <span data-ttu-id="f1935-220">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f1935-220">Is Indexed</span></span>             | <span data-ttu-id="f1935-221">True</span><span class="sxs-lookup"><span data-stu-id="f1935-221">True</span></span>                            |
| <span data-ttu-id="f1935-222">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f1935-222">In Global Catalog</span></span>      | <span data-ttu-id="f1935-223">True</span><span class="sxs-lookup"><span data-stu-id="f1935-223">True</span></span>                            |
| <span data-ttu-id="f1935-224">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f1935-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1935-225">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f1935-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1935-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1935-226">Range-Lower</span></span>            | <span data-ttu-id="f1935-227">1</span><span class="sxs-lookup"><span data-stu-id="f1935-227">1</span></span>                               |
| <span data-ttu-id="f1935-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1935-228">Range-Upper</span></span>            | <span data-ttu-id="f1935-229">255</span><span class="sxs-lookup"><span data-stu-id="f1935-229">255</span></span>                             |
| <span data-ttu-id="f1935-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-230">Search-Flags</span></span>           | <span data-ttu-id="f1935-231">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f1935-231">0x0000000D</span></span>                      |
| <span data-ttu-id="f1935-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-232">System-Flags</span></span>           | <span data-ttu-id="f1935-233">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f1935-233">0x00000012</span></span>                      |
| <span data-ttu-id="f1935-234">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f1935-234">Classes used in</span></span>        | [<span data-ttu-id="f1935-235">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f1935-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f1935-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1935-236">Windows Server 2008</span></span>



| <span data-ttu-id="f1935-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="f1935-237">Entry</span></span> | <span data-ttu-id="f1935-238">Значение</span><span class="sxs-lookup"><span data-stu-id="f1935-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1935-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f1935-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1935-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1935-240">MAPI-Id</span></span>                | <span data-ttu-id="f1935-241">0x8202</span><span class="sxs-lookup"><span data-stu-id="f1935-241">0x8202</span></span>                          |
| <span data-ttu-id="f1935-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1935-242">System-Only</span></span>            | <span data-ttu-id="f1935-243">True</span><span class="sxs-lookup"><span data-stu-id="f1935-243">True</span></span>                            |
| <span data-ttu-id="f1935-244">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f1935-244">Is-Single-Valued</span></span>       | <span data-ttu-id="f1935-245">True</span><span class="sxs-lookup"><span data-stu-id="f1935-245">True</span></span>                            |
| <span data-ttu-id="f1935-246">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f1935-246">Is Indexed</span></span>             | <span data-ttu-id="f1935-247">True</span><span class="sxs-lookup"><span data-stu-id="f1935-247">True</span></span>                            |
| <span data-ttu-id="f1935-248">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f1935-248">In Global Catalog</span></span>      | <span data-ttu-id="f1935-249">True</span><span class="sxs-lookup"><span data-stu-id="f1935-249">True</span></span>                            |
| <span data-ttu-id="f1935-250">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f1935-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1935-251">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f1935-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1935-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1935-252">Range-Lower</span></span>            | <span data-ttu-id="f1935-253">1</span><span class="sxs-lookup"><span data-stu-id="f1935-253">1</span></span>                               |
| <span data-ttu-id="f1935-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1935-254">Range-Upper</span></span>            | <span data-ttu-id="f1935-255">255</span><span class="sxs-lookup"><span data-stu-id="f1935-255">255</span></span>                             |
| <span data-ttu-id="f1935-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-256">Search-Flags</span></span>           | <span data-ttu-id="f1935-257">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f1935-257">0x0000000D</span></span>                      |
| <span data-ttu-id="f1935-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-258">System-Flags</span></span>           | <span data-ttu-id="f1935-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f1935-259">0x00000012</span></span>                      |
| <span data-ttu-id="f1935-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f1935-260">Classes used in</span></span>        | [<span data-ttu-id="f1935-261">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f1935-261">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f1935-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1935-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f1935-263">Ввод</span><span class="sxs-lookup"><span data-stu-id="f1935-263">Entry</span></span> | <span data-ttu-id="f1935-264">Значение</span><span class="sxs-lookup"><span data-stu-id="f1935-264">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1935-265">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f1935-265">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1935-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1935-266">MAPI-Id</span></span>                | <span data-ttu-id="f1935-267">0x8202</span><span class="sxs-lookup"><span data-stu-id="f1935-267">0x8202</span></span>                          |
| <span data-ttu-id="f1935-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1935-268">System-Only</span></span>            | <span data-ttu-id="f1935-269">True</span><span class="sxs-lookup"><span data-stu-id="f1935-269">True</span></span>                            |
| <span data-ttu-id="f1935-270">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f1935-270">Is-Single-Valued</span></span>       | <span data-ttu-id="f1935-271">True</span><span class="sxs-lookup"><span data-stu-id="f1935-271">True</span></span>                            |
| <span data-ttu-id="f1935-272">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f1935-272">Is Indexed</span></span>             | <span data-ttu-id="f1935-273">True</span><span class="sxs-lookup"><span data-stu-id="f1935-273">True</span></span>                            |
| <span data-ttu-id="f1935-274">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f1935-274">In Global Catalog</span></span>      | <span data-ttu-id="f1935-275">True</span><span class="sxs-lookup"><span data-stu-id="f1935-275">True</span></span>                            |
| <span data-ttu-id="f1935-276">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f1935-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1935-277">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f1935-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1935-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1935-278">Range-Lower</span></span>            | <span data-ttu-id="f1935-279">1</span><span class="sxs-lookup"><span data-stu-id="f1935-279">1</span></span>                               |
| <span data-ttu-id="f1935-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1935-280">Range-Upper</span></span>            | <span data-ttu-id="f1935-281">255</span><span class="sxs-lookup"><span data-stu-id="f1935-281">255</span></span>                             |
| <span data-ttu-id="f1935-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-282">Search-Flags</span></span>           | <span data-ttu-id="f1935-283">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f1935-283">0x0000000D</span></span>                      |
| <span data-ttu-id="f1935-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-284">System-Flags</span></span>           | <span data-ttu-id="f1935-285">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f1935-285">0x00000012</span></span>                      |
| <span data-ttu-id="f1935-286">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f1935-286">Classes used in</span></span>        | [<span data-ttu-id="f1935-287">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f1935-287">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f1935-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1935-288">Windows Server 2012</span></span>



| <span data-ttu-id="f1935-289">Ввод</span><span class="sxs-lookup"><span data-stu-id="f1935-289">Entry</span></span> | <span data-ttu-id="f1935-290">Значение</span><span class="sxs-lookup"><span data-stu-id="f1935-290">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f1935-291">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f1935-291">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="f1935-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f1935-292">MAPI-Id</span></span>                | <span data-ttu-id="f1935-293">0x8202</span><span class="sxs-lookup"><span data-stu-id="f1935-293">0x8202</span></span>                          |
| <span data-ttu-id="f1935-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="f1935-294">System-Only</span></span>            | <span data-ttu-id="f1935-295">True</span><span class="sxs-lookup"><span data-stu-id="f1935-295">True</span></span>                            |
| <span data-ttu-id="f1935-296">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f1935-296">Is-Single-Valued</span></span>       | <span data-ttu-id="f1935-297">True</span><span class="sxs-lookup"><span data-stu-id="f1935-297">True</span></span>                            |
| <span data-ttu-id="f1935-298">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f1935-298">Is Indexed</span></span>             | <span data-ttu-id="f1935-299">True</span><span class="sxs-lookup"><span data-stu-id="f1935-299">True</span></span>                            |
| <span data-ttu-id="f1935-300">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f1935-300">In Global Catalog</span></span>      | <span data-ttu-id="f1935-301">True</span><span class="sxs-lookup"><span data-stu-id="f1935-301">True</span></span>                            |
| <span data-ttu-id="f1935-302">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f1935-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="f1935-303">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f1935-303">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f1935-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f1935-304">Range-Lower</span></span>            | <span data-ttu-id="f1935-305">1</span><span class="sxs-lookup"><span data-stu-id="f1935-305">1</span></span>                               |
| <span data-ttu-id="f1935-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f1935-306">Range-Upper</span></span>            | <span data-ttu-id="f1935-307">255</span><span class="sxs-lookup"><span data-stu-id="f1935-307">255</span></span>                             |
| <span data-ttu-id="f1935-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-308">Search-Flags</span></span>           | <span data-ttu-id="f1935-309">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="f1935-309">0x0000000D</span></span>                      |
| <span data-ttu-id="f1935-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f1935-310">System-Flags</span></span>           | <span data-ttu-id="f1935-311">0x00000012</span><span class="sxs-lookup"><span data-stu-id="f1935-311">0x00000012</span></span>                      |
| <span data-ttu-id="f1935-312">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f1935-312">Classes used in</span></span>        | [<span data-ttu-id="f1935-313">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="f1935-313">**Top**</span></span>](c-top.md)<br/> |



 

 





