---
title: Атрибут NC-Name
description: Различающееся имя контекста именования для объекта.
ms.assetid: c60294b6-b803-49b4-9c94-6c0b82a45a9c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута NC-Name
- Схема AD атрибута nCName
topic_type:
- apiref
api_name:
- NC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152083e53950be81f2942ac217691989d5eb07b7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655340"
---
# <a name="nc-name-attribute"></a><span data-ttu-id="02bd1-105">Атрибут NC-Name</span><span class="sxs-lookup"><span data-stu-id="02bd1-105">NC-Name attribute</span></span>

<span data-ttu-id="02bd1-106">Различающееся имя контекста именования для объекта.</span><span class="sxs-lookup"><span data-stu-id="02bd1-106">The distinguished name of the Naming Context for the object.</span></span>



| <span data-ttu-id="02bd1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="02bd1-107">Entry</span></span> | <span data-ttu-id="02bd1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="02bd1-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="02bd1-109">CN</span><span class="sxs-lookup"><span data-stu-id="02bd1-109">CN</span></span>                | <span data-ttu-id="02bd1-110">NC-Name</span><span class="sxs-lookup"><span data-stu-id="02bd1-110">NC-Name</span></span>                                 |
| <span data-ttu-id="02bd1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="02bd1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="02bd1-112">Параметрами</span><span class="sxs-lookup"><span data-stu-id="02bd1-112">nCName</span></span>                                  |
| <span data-ttu-id="02bd1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="02bd1-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="02bd1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="02bd1-114">Update Privilege</span></span>  | <span data-ttu-id="02bd1-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="02bd1-115">Domain administrator</span></span>                    |
| <span data-ttu-id="02bd1-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="02bd1-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="02bd1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="02bd1-117">Attribute-Id</span></span>      | <span data-ttu-id="02bd1-118">1.2.840.113556.1.2.16</span><span class="sxs-lookup"><span data-stu-id="02bd1-118">1.2.840.113556.1.2.16</span></span>                   |
| <span data-ttu-id="02bd1-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="02bd1-119">System-Id-Guid</span></span>    | <span data-ttu-id="02bd1-120">bf9679d6-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="02bd1-120">bf9679d6-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="02bd1-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02bd1-121">Syntax</span></span>            | [<span data-ttu-id="02bd1-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="02bd1-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="02bd1-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="02bd1-123">Implementations</span></span>

-   [<span data-ttu-id="02bd1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="02bd1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="02bd1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="02bd1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="02bd1-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="02bd1-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="02bd1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="02bd1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="02bd1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="02bd1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="02bd1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="02bd1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="02bd1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="02bd1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="02bd1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="02bd1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="02bd1-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="02bd1-132">Entry</span></span> | <span data-ttu-id="02bd1-133">Значение</span><span class="sxs-lookup"><span data-stu-id="02bd1-133">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="02bd1-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="02bd1-134">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02bd1-135">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="02bd1-136">System-Only</span></span>            | <span data-ttu-id="02bd1-137">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-137">True</span></span>                                       |
| <span data-ttu-id="02bd1-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="02bd1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="02bd1-139">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-139">True</span></span>                                       |
| <span data-ttu-id="02bd1-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="02bd1-140">Is Indexed</span></span>             | <span data-ttu-id="02bd1-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-141">False</span></span>                                      |
| <span data-ttu-id="02bd1-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="02bd1-142">In Global Catalog</span></span>      | <span data-ttu-id="02bd1-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-143">False</span></span>                                      |
| <span data-ttu-id="02bd1-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="02bd1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="02bd1-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="02bd1-145">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="02bd1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02bd1-146">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02bd1-147">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-148">Search-Flags</span></span>           | <span data-ttu-id="02bd1-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="02bd1-149">0x00000008</span></span>                                 |
| <span data-ttu-id="02bd1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-150">System-Flags</span></span>           | <span data-ttu-id="02bd1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02bd1-151">0x00000010</span></span>                                 |
| <span data-ttu-id="02bd1-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="02bd1-152">Classes used in</span></span>        | [<span data-ttu-id="02bd1-153">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="02bd1-153">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="02bd1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="02bd1-154">Windows Server 2003</span></span>



| <span data-ttu-id="02bd1-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="02bd1-155">Entry</span></span> | <span data-ttu-id="02bd1-156">Значение</span><span class="sxs-lookup"><span data-stu-id="02bd1-156">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="02bd1-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="02bd1-157">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02bd1-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="02bd1-159">System-Only</span></span>            | <span data-ttu-id="02bd1-160">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-160">True</span></span>                                       |
| <span data-ttu-id="02bd1-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="02bd1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="02bd1-162">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-162">True</span></span>                                       |
| <span data-ttu-id="02bd1-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="02bd1-163">Is Indexed</span></span>             | <span data-ttu-id="02bd1-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-164">False</span></span>                                      |
| <span data-ttu-id="02bd1-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="02bd1-165">In Global Catalog</span></span>      | <span data-ttu-id="02bd1-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-166">False</span></span>                                      |
| <span data-ttu-id="02bd1-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="02bd1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="02bd1-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="02bd1-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="02bd1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02bd1-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02bd1-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-171">Search-Flags</span></span>           | <span data-ttu-id="02bd1-172">0x00000008</span><span class="sxs-lookup"><span data-stu-id="02bd1-172">0x00000008</span></span>                                 |
| <span data-ttu-id="02bd1-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-173">System-Flags</span></span>           | <span data-ttu-id="02bd1-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02bd1-174">0x00000010</span></span>                                 |
| <span data-ttu-id="02bd1-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="02bd1-175">Classes used in</span></span>        | [<span data-ttu-id="02bd1-176">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="02bd1-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="02bd1-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="02bd1-177">ADAM</span></span>



| <span data-ttu-id="02bd1-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="02bd1-178">Entry</span></span> | <span data-ttu-id="02bd1-179">Значение</span><span class="sxs-lookup"><span data-stu-id="02bd1-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="02bd1-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="02bd1-180">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02bd1-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="02bd1-182">System-Only</span></span>            | <span data-ttu-id="02bd1-183">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-183">True</span></span>                                       |
| <span data-ttu-id="02bd1-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="02bd1-184">Is-Single-Valued</span></span>       | <span data-ttu-id="02bd1-185">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-185">True</span></span>                                       |
| <span data-ttu-id="02bd1-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="02bd1-186">Is Indexed</span></span>             | <span data-ttu-id="02bd1-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-187">False</span></span>                                      |
| <span data-ttu-id="02bd1-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="02bd1-188">In Global Catalog</span></span>      | <span data-ttu-id="02bd1-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-189">False</span></span>                                      |
| <span data-ttu-id="02bd1-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="02bd1-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="02bd1-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="02bd1-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="02bd1-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02bd1-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02bd1-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-194">Search-Flags</span></span>           | <span data-ttu-id="02bd1-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="02bd1-195">0x00000008</span></span>                                 |
| <span data-ttu-id="02bd1-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-196">System-Flags</span></span>           | <span data-ttu-id="02bd1-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02bd1-197">0x00000010</span></span>                                 |
| <span data-ttu-id="02bd1-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="02bd1-198">Classes used in</span></span>        | [<span data-ttu-id="02bd1-199">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="02bd1-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="02bd1-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="02bd1-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="02bd1-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="02bd1-201">Entry</span></span> | <span data-ttu-id="02bd1-202">Значение</span><span class="sxs-lookup"><span data-stu-id="02bd1-202">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="02bd1-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="02bd1-203">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02bd1-204">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="02bd1-205">System-Only</span></span>            | <span data-ttu-id="02bd1-206">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-206">True</span></span>                                       |
| <span data-ttu-id="02bd1-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="02bd1-207">Is-Single-Valued</span></span>       | <span data-ttu-id="02bd1-208">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-208">True</span></span>                                       |
| <span data-ttu-id="02bd1-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="02bd1-209">Is Indexed</span></span>             | <span data-ttu-id="02bd1-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-210">False</span></span>                                      |
| <span data-ttu-id="02bd1-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="02bd1-211">In Global Catalog</span></span>      | <span data-ttu-id="02bd1-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-212">False</span></span>                                      |
| <span data-ttu-id="02bd1-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="02bd1-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="02bd1-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="02bd1-214">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="02bd1-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02bd1-215">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02bd1-216">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-217">Search-Flags</span></span>           | <span data-ttu-id="02bd1-218">0x00000008</span><span class="sxs-lookup"><span data-stu-id="02bd1-218">0x00000008</span></span>                                 |
| <span data-ttu-id="02bd1-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-219">System-Flags</span></span>           | <span data-ttu-id="02bd1-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02bd1-220">0x00000010</span></span>                                 |
| <span data-ttu-id="02bd1-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="02bd1-221">Classes used in</span></span>        | [<span data-ttu-id="02bd1-222">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="02bd1-222">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="02bd1-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02bd1-223">Windows Server 2008</span></span>



| <span data-ttu-id="02bd1-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="02bd1-224">Entry</span></span> | <span data-ttu-id="02bd1-225">Значение</span><span class="sxs-lookup"><span data-stu-id="02bd1-225">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="02bd1-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="02bd1-226">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02bd1-227">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="02bd1-228">System-Only</span></span>            | <span data-ttu-id="02bd1-229">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-229">True</span></span>                                       |
| <span data-ttu-id="02bd1-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="02bd1-230">Is-Single-Valued</span></span>       | <span data-ttu-id="02bd1-231">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-231">True</span></span>                                       |
| <span data-ttu-id="02bd1-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="02bd1-232">Is Indexed</span></span>             | <span data-ttu-id="02bd1-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-233">False</span></span>                                      |
| <span data-ttu-id="02bd1-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="02bd1-234">In Global Catalog</span></span>      | <span data-ttu-id="02bd1-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-235">False</span></span>                                      |
| <span data-ttu-id="02bd1-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="02bd1-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="02bd1-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="02bd1-237">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="02bd1-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02bd1-238">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02bd1-239">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-240">Search-Flags</span></span>           | <span data-ttu-id="02bd1-241">0x00000008</span><span class="sxs-lookup"><span data-stu-id="02bd1-241">0x00000008</span></span>                                 |
| <span data-ttu-id="02bd1-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-242">System-Flags</span></span>           | <span data-ttu-id="02bd1-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02bd1-243">0x00000010</span></span>                                 |
| <span data-ttu-id="02bd1-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="02bd1-244">Classes used in</span></span>        | [<span data-ttu-id="02bd1-245">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="02bd1-245">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="02bd1-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="02bd1-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="02bd1-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="02bd1-247">Entry</span></span> | <span data-ttu-id="02bd1-248">Значение</span><span class="sxs-lookup"><span data-stu-id="02bd1-248">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="02bd1-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="02bd1-249">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02bd1-250">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="02bd1-251">System-Only</span></span>            | <span data-ttu-id="02bd1-252">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-252">True</span></span>                                       |
| <span data-ttu-id="02bd1-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="02bd1-253">Is-Single-Valued</span></span>       | <span data-ttu-id="02bd1-254">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-254">True</span></span>                                       |
| <span data-ttu-id="02bd1-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="02bd1-255">Is Indexed</span></span>             | <span data-ttu-id="02bd1-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-256">False</span></span>                                      |
| <span data-ttu-id="02bd1-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="02bd1-257">In Global Catalog</span></span>      | <span data-ttu-id="02bd1-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-258">False</span></span>                                      |
| <span data-ttu-id="02bd1-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="02bd1-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="02bd1-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="02bd1-260">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="02bd1-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02bd1-261">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02bd1-262">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-263">Search-Flags</span></span>           | <span data-ttu-id="02bd1-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="02bd1-264">0x00000008</span></span>                                 |
| <span data-ttu-id="02bd1-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-265">System-Flags</span></span>           | <span data-ttu-id="02bd1-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02bd1-266">0x00000010</span></span>                                 |
| <span data-ttu-id="02bd1-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="02bd1-267">Classes used in</span></span>        | [<span data-ttu-id="02bd1-268">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="02bd1-268">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="02bd1-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="02bd1-269">Windows Server 2012</span></span>



| <span data-ttu-id="02bd1-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="02bd1-270">Entry</span></span> | <span data-ttu-id="02bd1-271">Значение</span><span class="sxs-lookup"><span data-stu-id="02bd1-271">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="02bd1-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="02bd1-272">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="02bd1-273">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="02bd1-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="02bd1-274">System-Only</span></span>            | <span data-ttu-id="02bd1-275">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-275">True</span></span>                                       |
| <span data-ttu-id="02bd1-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="02bd1-276">Is-Single-Valued</span></span>       | <span data-ttu-id="02bd1-277">True</span><span class="sxs-lookup"><span data-stu-id="02bd1-277">True</span></span>                                       |
| <span data-ttu-id="02bd1-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="02bd1-278">Is Indexed</span></span>             | <span data-ttu-id="02bd1-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-279">False</span></span>                                      |
| <span data-ttu-id="02bd1-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="02bd1-280">In Global Catalog</span></span>      | <span data-ttu-id="02bd1-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="02bd1-281">False</span></span>                                      |
| <span data-ttu-id="02bd1-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="02bd1-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="02bd1-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="02bd1-283">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="02bd1-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="02bd1-284">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="02bd1-285">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="02bd1-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-286">Search-Flags</span></span>           | <span data-ttu-id="02bd1-287">0x00000008</span><span class="sxs-lookup"><span data-stu-id="02bd1-287">0x00000008</span></span>                                 |
| <span data-ttu-id="02bd1-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="02bd1-288">System-Flags</span></span>           | <span data-ttu-id="02bd1-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="02bd1-289">0x00000010</span></span>                                 |
| <span data-ttu-id="02bd1-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="02bd1-290">Classes used in</span></span>        | [<span data-ttu-id="02bd1-291">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="02bd1-291">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





