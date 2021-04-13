---
title: Атрибут COM-CLSID
description: Этот атрибут содержит идентификатор GUID, связанный с этим классом объектов.
ms.assetid: 2de3b0c4-5fb6-43c1-9aa7-9c98048c095e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута CLSID COM
- Схема AD атрибута Комклсид
topic_type:
- apiref
api_name:
- COM-CLSID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52430f53721866651ab1242353af36ba8c193553
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493599"
---
# <a name="com-clsid-attribute"></a><span data-ttu-id="14517-105">Атрибут COM-CLSID</span><span class="sxs-lookup"><span data-stu-id="14517-105">COM-CLSID attribute</span></span>

<span data-ttu-id="14517-106">Этот атрибут содержит идентификатор GUID, связанный с этим классом объектов.</span><span class="sxs-lookup"><span data-stu-id="14517-106">This attribute contains the GUID that is associated to this object class.</span></span>



| <span data-ttu-id="14517-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="14517-107">Entry</span></span> | <span data-ttu-id="14517-108">Значение</span><span class="sxs-lookup"><span data-stu-id="14517-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="14517-109">CN</span><span class="sxs-lookup"><span data-stu-id="14517-109">CN</span></span>                | <span data-ttu-id="14517-110">CLSID COM</span><span class="sxs-lookup"><span data-stu-id="14517-110">COM-CLSID</span></span>                                   |
| <span data-ttu-id="14517-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="14517-111">Ldap-Display-Name</span></span> | <span data-ttu-id="14517-112">комклсид</span><span class="sxs-lookup"><span data-stu-id="14517-112">cOMCLSID</span></span>                                    |
| <span data-ttu-id="14517-113">Размер</span><span class="sxs-lookup"><span data-stu-id="14517-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="14517-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="14517-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="14517-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="14517-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="14517-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="14517-116">Attribute-Id</span></span>      | <span data-ttu-id="14517-117">1.2.840.113556.1.4.249</span><span class="sxs-lookup"><span data-stu-id="14517-117">1.2.840.113556.1.4.249</span></span>                      |
| <span data-ttu-id="14517-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="14517-118">System-Id-Guid</span></span>    | <span data-ttu-id="14517-119">281416d9-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="14517-119">281416d9-1968-11d0-a28f-00aa003049e2</span></span>        |
| <span data-ttu-id="14517-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14517-120">Syntax</span></span>            | [<span data-ttu-id="14517-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="14517-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="14517-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="14517-122">Implementations</span></span>

-   [<span data-ttu-id="14517-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="14517-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="14517-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="14517-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="14517-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="14517-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="14517-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="14517-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="14517-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14517-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="14517-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="14517-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="14517-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14517-129">Windows 2000 Server</span></span>



| <span data-ttu-id="14517-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="14517-130">Entry</span></span> | <span data-ttu-id="14517-131">Значение</span><span class="sxs-lookup"><span data-stu-id="14517-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="14517-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14517-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14517-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="14517-134">System-Only</span></span>            | <span data-ttu-id="14517-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-135">False</span></span>                                                        |
| <span data-ttu-id="14517-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14517-136">Is-Single-Valued</span></span>       | <span data-ttu-id="14517-137">True</span><span class="sxs-lookup"><span data-stu-id="14517-137">True</span></span>                                                         |
| <span data-ttu-id="14517-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14517-138">Is Indexed</span></span>             | <span data-ttu-id="14517-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-139">False</span></span>                                                        |
| <span data-ttu-id="14517-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14517-140">In Global Catalog</span></span>      | <span data-ttu-id="14517-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-141">False</span></span>                                                        |
| <span data-ttu-id="14517-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14517-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="14517-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14517-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="14517-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14517-144">Range-Lower</span></span>            | <span data-ttu-id="14517-145">36</span><span class="sxs-lookup"><span data-stu-id="14517-145">36</span></span>                                                           |
| <span data-ttu-id="14517-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14517-146">Range-Upper</span></span>            | <span data-ttu-id="14517-147">36</span><span class="sxs-lookup"><span data-stu-id="14517-147">36</span></span>                                                           |
| <span data-ttu-id="14517-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-148">Search-Flags</span></span>           | <span data-ttu-id="14517-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14517-149">0x00000000</span></span>                                                   |
| <span data-ttu-id="14517-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-150">System-Flags</span></span>           | <span data-ttu-id="14517-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14517-151">0x00000010</span></span>                                                   |
| <span data-ttu-id="14517-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14517-152">Classes used in</span></span>        | [<span data-ttu-id="14517-153">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="14517-153">**Class-Registration**</span></span>](c-classregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="14517-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14517-154">Windows Server 2003</span></span>



| <span data-ttu-id="14517-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="14517-155">Entry</span></span> | <span data-ttu-id="14517-156">Значение</span><span class="sxs-lookup"><span data-stu-id="14517-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="14517-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14517-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14517-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="14517-159">System-Only</span></span>            | <span data-ttu-id="14517-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-160">False</span></span>                                                        |
| <span data-ttu-id="14517-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14517-161">Is-Single-Valued</span></span>       | <span data-ttu-id="14517-162">True</span><span class="sxs-lookup"><span data-stu-id="14517-162">True</span></span>                                                         |
| <span data-ttu-id="14517-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14517-163">Is Indexed</span></span>             | <span data-ttu-id="14517-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-164">False</span></span>                                                        |
| <span data-ttu-id="14517-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14517-165">In Global Catalog</span></span>      | <span data-ttu-id="14517-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-166">False</span></span>                                                        |
| <span data-ttu-id="14517-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14517-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="14517-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14517-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="14517-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14517-169">Range-Lower</span></span>            | <span data-ttu-id="14517-170">36</span><span class="sxs-lookup"><span data-stu-id="14517-170">36</span></span>                                                           |
| <span data-ttu-id="14517-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14517-171">Range-Upper</span></span>            | <span data-ttu-id="14517-172">36</span><span class="sxs-lookup"><span data-stu-id="14517-172">36</span></span>                                                           |
| <span data-ttu-id="14517-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-173">Search-Flags</span></span>           | <span data-ttu-id="14517-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14517-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="14517-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-175">System-Flags</span></span>           | <span data-ttu-id="14517-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14517-176">0x00000010</span></span>                                                   |
| <span data-ttu-id="14517-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14517-177">Classes used in</span></span>        | [<span data-ttu-id="14517-178">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="14517-178">**Class-Registration**</span></span>](c-classregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="14517-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="14517-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="14517-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="14517-180">Entry</span></span> | <span data-ttu-id="14517-181">Значение</span><span class="sxs-lookup"><span data-stu-id="14517-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="14517-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14517-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14517-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="14517-184">System-Only</span></span>            | <span data-ttu-id="14517-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-185">False</span></span>                                                        |
| <span data-ttu-id="14517-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14517-186">Is-Single-Valued</span></span>       | <span data-ttu-id="14517-187">True</span><span class="sxs-lookup"><span data-stu-id="14517-187">True</span></span>                                                         |
| <span data-ttu-id="14517-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14517-188">Is Indexed</span></span>             | <span data-ttu-id="14517-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-189">False</span></span>                                                        |
| <span data-ttu-id="14517-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14517-190">In Global Catalog</span></span>      | <span data-ttu-id="14517-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-191">False</span></span>                                                        |
| <span data-ttu-id="14517-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14517-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="14517-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14517-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="14517-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14517-194">Range-Lower</span></span>            | <span data-ttu-id="14517-195">36</span><span class="sxs-lookup"><span data-stu-id="14517-195">36</span></span>                                                           |
| <span data-ttu-id="14517-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14517-196">Range-Upper</span></span>            | <span data-ttu-id="14517-197">36</span><span class="sxs-lookup"><span data-stu-id="14517-197">36</span></span>                                                           |
| <span data-ttu-id="14517-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-198">Search-Flags</span></span>           | <span data-ttu-id="14517-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14517-199">0x00000000</span></span>                                                   |
| <span data-ttu-id="14517-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-200">System-Flags</span></span>           | <span data-ttu-id="14517-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14517-201">0x00000010</span></span>                                                   |
| <span data-ttu-id="14517-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14517-202">Classes used in</span></span>        | [<span data-ttu-id="14517-203">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="14517-203">**Class-Registration**</span></span>](c-classregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="14517-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14517-204">Windows Server 2008</span></span>



| <span data-ttu-id="14517-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="14517-205">Entry</span></span> | <span data-ttu-id="14517-206">Значение</span><span class="sxs-lookup"><span data-stu-id="14517-206">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="14517-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14517-207">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14517-208">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="14517-209">System-Only</span></span>            | <span data-ttu-id="14517-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-210">False</span></span>                                                        |
| <span data-ttu-id="14517-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14517-211">Is-Single-Valued</span></span>       | <span data-ttu-id="14517-212">True</span><span class="sxs-lookup"><span data-stu-id="14517-212">True</span></span>                                                         |
| <span data-ttu-id="14517-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14517-213">Is Indexed</span></span>             | <span data-ttu-id="14517-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-214">False</span></span>                                                        |
| <span data-ttu-id="14517-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14517-215">In Global Catalog</span></span>      | <span data-ttu-id="14517-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-216">False</span></span>                                                        |
| <span data-ttu-id="14517-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14517-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="14517-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14517-218">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="14517-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14517-219">Range-Lower</span></span>            | <span data-ttu-id="14517-220">36</span><span class="sxs-lookup"><span data-stu-id="14517-220">36</span></span>                                                           |
| <span data-ttu-id="14517-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14517-221">Range-Upper</span></span>            | <span data-ttu-id="14517-222">36</span><span class="sxs-lookup"><span data-stu-id="14517-222">36</span></span>                                                           |
| <span data-ttu-id="14517-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-223">Search-Flags</span></span>           | <span data-ttu-id="14517-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14517-224">0x00000000</span></span>                                                   |
| <span data-ttu-id="14517-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-225">System-Flags</span></span>           | <span data-ttu-id="14517-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14517-226">0x00000010</span></span>                                                   |
| <span data-ttu-id="14517-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14517-227">Classes used in</span></span>        | [<span data-ttu-id="14517-228">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="14517-228">**Class-Registration**</span></span>](c-classregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="14517-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14517-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="14517-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="14517-230">Entry</span></span> | <span data-ttu-id="14517-231">Значение</span><span class="sxs-lookup"><span data-stu-id="14517-231">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="14517-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14517-232">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14517-233">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="14517-234">System-Only</span></span>            | <span data-ttu-id="14517-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-235">False</span></span>                                                        |
| <span data-ttu-id="14517-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14517-236">Is-Single-Valued</span></span>       | <span data-ttu-id="14517-237">True</span><span class="sxs-lookup"><span data-stu-id="14517-237">True</span></span>                                                         |
| <span data-ttu-id="14517-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14517-238">Is Indexed</span></span>             | <span data-ttu-id="14517-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-239">False</span></span>                                                        |
| <span data-ttu-id="14517-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14517-240">In Global Catalog</span></span>      | <span data-ttu-id="14517-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-241">False</span></span>                                                        |
| <span data-ttu-id="14517-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14517-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="14517-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14517-243">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="14517-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14517-244">Range-Lower</span></span>            | <span data-ttu-id="14517-245">36</span><span class="sxs-lookup"><span data-stu-id="14517-245">36</span></span>                                                           |
| <span data-ttu-id="14517-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14517-246">Range-Upper</span></span>            | <span data-ttu-id="14517-247">36</span><span class="sxs-lookup"><span data-stu-id="14517-247">36</span></span>                                                           |
| <span data-ttu-id="14517-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-248">Search-Flags</span></span>           | <span data-ttu-id="14517-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14517-249">0x00000000</span></span>                                                   |
| <span data-ttu-id="14517-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-250">System-Flags</span></span>           | <span data-ttu-id="14517-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14517-251">0x00000010</span></span>                                                   |
| <span data-ttu-id="14517-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14517-252">Classes used in</span></span>        | [<span data-ttu-id="14517-253">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="14517-253">**Class-Registration**</span></span>](c-classregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="14517-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14517-254">Windows Server 2012</span></span>



| <span data-ttu-id="14517-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="14517-255">Entry</span></span> | <span data-ttu-id="14517-256">Значение</span><span class="sxs-lookup"><span data-stu-id="14517-256">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="14517-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14517-257">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14517-258">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="14517-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="14517-259">System-Only</span></span>            | <span data-ttu-id="14517-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-260">False</span></span>                                                        |
| <span data-ttu-id="14517-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14517-261">Is-Single-Valued</span></span>       | <span data-ttu-id="14517-262">True</span><span class="sxs-lookup"><span data-stu-id="14517-262">True</span></span>                                                         |
| <span data-ttu-id="14517-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14517-263">Is Indexed</span></span>             | <span data-ttu-id="14517-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-264">False</span></span>                                                        |
| <span data-ttu-id="14517-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14517-265">In Global Catalog</span></span>      | <span data-ttu-id="14517-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="14517-266">False</span></span>                                                        |
| <span data-ttu-id="14517-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14517-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="14517-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14517-268">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="14517-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14517-269">Range-Lower</span></span>            | <span data-ttu-id="14517-270">36</span><span class="sxs-lookup"><span data-stu-id="14517-270">36</span></span>                                                           |
| <span data-ttu-id="14517-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14517-271">Range-Upper</span></span>            | <span data-ttu-id="14517-272">36</span><span class="sxs-lookup"><span data-stu-id="14517-272">36</span></span>                                                           |
| <span data-ttu-id="14517-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-273">Search-Flags</span></span>           | <span data-ttu-id="14517-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14517-274">0x00000000</span></span>                                                   |
| <span data-ttu-id="14517-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14517-275">System-Flags</span></span>           | <span data-ttu-id="14517-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14517-276">0x00000010</span></span>                                                   |
| <span data-ttu-id="14517-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14517-277">Classes used in</span></span>        | [<span data-ttu-id="14517-278">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="14517-278">**Class-Registration**</span></span>](c-classregistration.md)<br/> |



 

 





