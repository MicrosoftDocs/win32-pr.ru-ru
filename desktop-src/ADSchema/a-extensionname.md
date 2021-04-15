---
title: Атрибут Extension-Name
description: Имя страницы свойств, используемой для расширения пользовательского интерфейса объекта каталога.
ms.assetid: 7afa3363-00ac-4651-8a5c-b36b4ee8bf88
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Extension-Name
- Схема AD атрибута extensionName
topic_type:
- apiref
api_name:
- Extension-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841685edbafbc761b1531f29f16d45657b57011d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654857"
---
# <a name="extension-name-attribute"></a><span data-ttu-id="dd8da-105">Атрибут Extension-Name</span><span class="sxs-lookup"><span data-stu-id="dd8da-105">Extension-Name attribute</span></span>

<span data-ttu-id="dd8da-106">Имя страницы свойств, используемой для расширения пользовательского интерфейса объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="dd8da-106">The name of a property page used to extend the UI of a directory object.</span></span>



| <span data-ttu-id="dd8da-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="dd8da-107">Entry</span></span> | <span data-ttu-id="dd8da-108">Значение</span><span class="sxs-lookup"><span data-stu-id="dd8da-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="dd8da-109">CN</span><span class="sxs-lookup"><span data-stu-id="dd8da-109">CN</span></span>                | <span data-ttu-id="dd8da-110">Extension-Name</span><span class="sxs-lookup"><span data-stu-id="dd8da-110">Extension-Name</span></span>                              |
| <span data-ttu-id="dd8da-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="dd8da-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dd8da-112">extensionName</span><span class="sxs-lookup"><span data-stu-id="dd8da-112">extensionName</span></span>                               |
| <span data-ttu-id="dd8da-113">Размер</span><span class="sxs-lookup"><span data-stu-id="dd8da-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="dd8da-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="dd8da-114">Update Privilege</span></span>  | <span data-ttu-id="dd8da-115">Создатель объекта расширения.</span><span class="sxs-lookup"><span data-stu-id="dd8da-115">The creator of the extension object.</span></span>        |
| <span data-ttu-id="dd8da-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="dd8da-116">Update Frequency</span></span>  | <span data-ttu-id="dd8da-117">При создании нового расширения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dd8da-117">Whenever a new UI extension is created.</span></span>     |
| <span data-ttu-id="dd8da-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dd8da-118">Attribute-Id</span></span>      | <span data-ttu-id="dd8da-119">1.2.840.113556.1.2.227</span><span class="sxs-lookup"><span data-stu-id="dd8da-119">1.2.840.113556.1.2.227</span></span>                      |
| <span data-ttu-id="dd8da-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="dd8da-120">System-Id-Guid</span></span>    | <span data-ttu-id="dd8da-121">bf967972-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="dd8da-121">bf967972-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="dd8da-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd8da-122">Syntax</span></span>            | [<span data-ttu-id="dd8da-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="dd8da-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="dd8da-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="dd8da-124">Implementations</span></span>

-   [<span data-ttu-id="dd8da-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dd8da-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dd8da-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dd8da-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dd8da-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dd8da-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dd8da-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dd8da-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dd8da-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dd8da-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dd8da-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dd8da-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dd8da-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd8da-131">Windows 2000 Server</span></span>



| <span data-ttu-id="dd8da-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="dd8da-132">Entry</span></span> | <span data-ttu-id="dd8da-133">Значение</span><span class="sxs-lookup"><span data-stu-id="dd8da-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dd8da-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dd8da-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dd8da-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd8da-135">MAPI-Id</span></span>                | <span data-ttu-id="dd8da-136">0x80A9</span><span class="sxs-lookup"><span data-stu-id="dd8da-136">0x80A9</span></span>                          |
| <span data-ttu-id="dd8da-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd8da-137">System-Only</span></span>            | <span data-ttu-id="dd8da-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-138">False</span></span>                           |
| <span data-ttu-id="dd8da-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dd8da-139">Is-Single-Valued</span></span>       | <span data-ttu-id="dd8da-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-140">False</span></span>                           |
| <span data-ttu-id="dd8da-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dd8da-141">Is Indexed</span></span>             | <span data-ttu-id="dd8da-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-142">False</span></span>                           |
| <span data-ttu-id="dd8da-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dd8da-143">In Global Catalog</span></span>      | <span data-ttu-id="dd8da-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-144">False</span></span>                           |
| <span data-ttu-id="dd8da-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dd8da-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd8da-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dd8da-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dd8da-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd8da-147">Range-Lower</span></span>            | <span data-ttu-id="dd8da-148">1</span><span class="sxs-lookup"><span data-stu-id="dd8da-148">1</span></span>                               |
| <span data-ttu-id="dd8da-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd8da-149">Range-Upper</span></span>            | <span data-ttu-id="dd8da-150">255</span><span class="sxs-lookup"><span data-stu-id="dd8da-150">255</span></span>                             |
| <span data-ttu-id="dd8da-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-151">Search-Flags</span></span>           | <span data-ttu-id="dd8da-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd8da-152">0x00000000</span></span>                      |
| <span data-ttu-id="dd8da-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-153">System-Flags</span></span>           | <span data-ttu-id="dd8da-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd8da-154">0x00000010</span></span>                      |
| <span data-ttu-id="dd8da-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dd8da-155">Classes used in</span></span>        | [<span data-ttu-id="dd8da-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dd8da-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dd8da-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd8da-157">Windows Server 2003</span></span>



| <span data-ttu-id="dd8da-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="dd8da-158">Entry</span></span> | <span data-ttu-id="dd8da-159">Значение</span><span class="sxs-lookup"><span data-stu-id="dd8da-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dd8da-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dd8da-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dd8da-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd8da-161">MAPI-Id</span></span>                | <span data-ttu-id="dd8da-162">0x80A9</span><span class="sxs-lookup"><span data-stu-id="dd8da-162">0x80A9</span></span>                          |
| <span data-ttu-id="dd8da-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd8da-163">System-Only</span></span>            | <span data-ttu-id="dd8da-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-164">False</span></span>                           |
| <span data-ttu-id="dd8da-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dd8da-165">Is-Single-Valued</span></span>       | <span data-ttu-id="dd8da-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-166">False</span></span>                           |
| <span data-ttu-id="dd8da-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dd8da-167">Is Indexed</span></span>             | <span data-ttu-id="dd8da-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-168">False</span></span>                           |
| <span data-ttu-id="dd8da-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dd8da-169">In Global Catalog</span></span>      | <span data-ttu-id="dd8da-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-170">False</span></span>                           |
| <span data-ttu-id="dd8da-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dd8da-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd8da-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dd8da-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dd8da-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd8da-173">Range-Lower</span></span>            | <span data-ttu-id="dd8da-174">1</span><span class="sxs-lookup"><span data-stu-id="dd8da-174">1</span></span>                               |
| <span data-ttu-id="dd8da-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd8da-175">Range-Upper</span></span>            | <span data-ttu-id="dd8da-176">255</span><span class="sxs-lookup"><span data-stu-id="dd8da-176">255</span></span>                             |
| <span data-ttu-id="dd8da-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-177">Search-Flags</span></span>           | <span data-ttu-id="dd8da-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd8da-178">0x00000000</span></span>                      |
| <span data-ttu-id="dd8da-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-179">System-Flags</span></span>           | <span data-ttu-id="dd8da-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd8da-180">0x00000010</span></span>                      |
| <span data-ttu-id="dd8da-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dd8da-181">Classes used in</span></span>        | [<span data-ttu-id="dd8da-182">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dd8da-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dd8da-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dd8da-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dd8da-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="dd8da-184">Entry</span></span> | <span data-ttu-id="dd8da-185">Значение</span><span class="sxs-lookup"><span data-stu-id="dd8da-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dd8da-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dd8da-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dd8da-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd8da-187">MAPI-Id</span></span>                | <span data-ttu-id="dd8da-188">0x80A9</span><span class="sxs-lookup"><span data-stu-id="dd8da-188">0x80A9</span></span>                          |
| <span data-ttu-id="dd8da-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd8da-189">System-Only</span></span>            | <span data-ttu-id="dd8da-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-190">False</span></span>                           |
| <span data-ttu-id="dd8da-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dd8da-191">Is-Single-Valued</span></span>       | <span data-ttu-id="dd8da-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-192">False</span></span>                           |
| <span data-ttu-id="dd8da-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dd8da-193">Is Indexed</span></span>             | <span data-ttu-id="dd8da-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-194">False</span></span>                           |
| <span data-ttu-id="dd8da-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dd8da-195">In Global Catalog</span></span>      | <span data-ttu-id="dd8da-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-196">False</span></span>                           |
| <span data-ttu-id="dd8da-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dd8da-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd8da-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dd8da-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dd8da-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd8da-199">Range-Lower</span></span>            | <span data-ttu-id="dd8da-200">1</span><span class="sxs-lookup"><span data-stu-id="dd8da-200">1</span></span>                               |
| <span data-ttu-id="dd8da-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd8da-201">Range-Upper</span></span>            | <span data-ttu-id="dd8da-202">255</span><span class="sxs-lookup"><span data-stu-id="dd8da-202">255</span></span>                             |
| <span data-ttu-id="dd8da-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-203">Search-Flags</span></span>           | <span data-ttu-id="dd8da-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd8da-204">0x00000000</span></span>                      |
| <span data-ttu-id="dd8da-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-205">System-Flags</span></span>           | <span data-ttu-id="dd8da-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd8da-206">0x00000010</span></span>                      |
| <span data-ttu-id="dd8da-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dd8da-207">Classes used in</span></span>        | [<span data-ttu-id="dd8da-208">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dd8da-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dd8da-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd8da-209">Windows Server 2008</span></span>



| <span data-ttu-id="dd8da-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="dd8da-210">Entry</span></span> | <span data-ttu-id="dd8da-211">Значение</span><span class="sxs-lookup"><span data-stu-id="dd8da-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dd8da-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dd8da-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dd8da-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd8da-213">MAPI-Id</span></span>                | <span data-ttu-id="dd8da-214">0x80A9</span><span class="sxs-lookup"><span data-stu-id="dd8da-214">0x80A9</span></span>                          |
| <span data-ttu-id="dd8da-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd8da-215">System-Only</span></span>            | <span data-ttu-id="dd8da-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-216">False</span></span>                           |
| <span data-ttu-id="dd8da-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dd8da-217">Is-Single-Valued</span></span>       | <span data-ttu-id="dd8da-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-218">False</span></span>                           |
| <span data-ttu-id="dd8da-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dd8da-219">Is Indexed</span></span>             | <span data-ttu-id="dd8da-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-220">False</span></span>                           |
| <span data-ttu-id="dd8da-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dd8da-221">In Global Catalog</span></span>      | <span data-ttu-id="dd8da-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-222">False</span></span>                           |
| <span data-ttu-id="dd8da-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dd8da-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd8da-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dd8da-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dd8da-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd8da-225">Range-Lower</span></span>            | <span data-ttu-id="dd8da-226">1</span><span class="sxs-lookup"><span data-stu-id="dd8da-226">1</span></span>                               |
| <span data-ttu-id="dd8da-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd8da-227">Range-Upper</span></span>            | <span data-ttu-id="dd8da-228">255</span><span class="sxs-lookup"><span data-stu-id="dd8da-228">255</span></span>                             |
| <span data-ttu-id="dd8da-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-229">Search-Flags</span></span>           | <span data-ttu-id="dd8da-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd8da-230">0x00000000</span></span>                      |
| <span data-ttu-id="dd8da-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-231">System-Flags</span></span>           | <span data-ttu-id="dd8da-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd8da-232">0x00000010</span></span>                      |
| <span data-ttu-id="dd8da-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dd8da-233">Classes used in</span></span>        | [<span data-ttu-id="dd8da-234">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dd8da-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dd8da-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dd8da-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dd8da-236">Ввод</span><span class="sxs-lookup"><span data-stu-id="dd8da-236">Entry</span></span> | <span data-ttu-id="dd8da-237">Значение</span><span class="sxs-lookup"><span data-stu-id="dd8da-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dd8da-238">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dd8da-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dd8da-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd8da-239">MAPI-Id</span></span>                | <span data-ttu-id="dd8da-240">0x80A9</span><span class="sxs-lookup"><span data-stu-id="dd8da-240">0x80A9</span></span>                          |
| <span data-ttu-id="dd8da-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd8da-241">System-Only</span></span>            | <span data-ttu-id="dd8da-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-242">False</span></span>                           |
| <span data-ttu-id="dd8da-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dd8da-243">Is-Single-Valued</span></span>       | <span data-ttu-id="dd8da-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-244">False</span></span>                           |
| <span data-ttu-id="dd8da-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dd8da-245">Is Indexed</span></span>             | <span data-ttu-id="dd8da-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-246">False</span></span>                           |
| <span data-ttu-id="dd8da-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dd8da-247">In Global Catalog</span></span>      | <span data-ttu-id="dd8da-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-248">False</span></span>                           |
| <span data-ttu-id="dd8da-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dd8da-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd8da-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dd8da-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dd8da-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd8da-251">Range-Lower</span></span>            | <span data-ttu-id="dd8da-252">1</span><span class="sxs-lookup"><span data-stu-id="dd8da-252">1</span></span>                               |
| <span data-ttu-id="dd8da-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd8da-253">Range-Upper</span></span>            | <span data-ttu-id="dd8da-254">255</span><span class="sxs-lookup"><span data-stu-id="dd8da-254">255</span></span>                             |
| <span data-ttu-id="dd8da-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-255">Search-Flags</span></span>           | <span data-ttu-id="dd8da-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd8da-256">0x00000000</span></span>                      |
| <span data-ttu-id="dd8da-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-257">System-Flags</span></span>           | <span data-ttu-id="dd8da-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd8da-258">0x00000010</span></span>                      |
| <span data-ttu-id="dd8da-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dd8da-259">Classes used in</span></span>        | [<span data-ttu-id="dd8da-260">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dd8da-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dd8da-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd8da-261">Windows Server 2012</span></span>



| <span data-ttu-id="dd8da-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="dd8da-262">Entry</span></span> | <span data-ttu-id="dd8da-263">Значение</span><span class="sxs-lookup"><span data-stu-id="dd8da-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dd8da-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dd8da-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dd8da-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd8da-265">MAPI-Id</span></span>                | <span data-ttu-id="dd8da-266">0x80A9</span><span class="sxs-lookup"><span data-stu-id="dd8da-266">0x80A9</span></span>                          |
| <span data-ttu-id="dd8da-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd8da-267">System-Only</span></span>            | <span data-ttu-id="dd8da-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-268">False</span></span>                           |
| <span data-ttu-id="dd8da-269">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dd8da-269">Is-Single-Valued</span></span>       | <span data-ttu-id="dd8da-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-270">False</span></span>                           |
| <span data-ttu-id="dd8da-271">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dd8da-271">Is Indexed</span></span>             | <span data-ttu-id="dd8da-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-272">False</span></span>                           |
| <span data-ttu-id="dd8da-273">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dd8da-273">In Global Catalog</span></span>      | <span data-ttu-id="dd8da-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="dd8da-274">False</span></span>                           |
| <span data-ttu-id="dd8da-275">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dd8da-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd8da-276">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dd8da-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dd8da-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd8da-277">Range-Lower</span></span>            | <span data-ttu-id="dd8da-278">1</span><span class="sxs-lookup"><span data-stu-id="dd8da-278">1</span></span>                               |
| <span data-ttu-id="dd8da-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd8da-279">Range-Upper</span></span>            | <span data-ttu-id="dd8da-280">255</span><span class="sxs-lookup"><span data-stu-id="dd8da-280">255</span></span>                             |
| <span data-ttu-id="dd8da-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-281">Search-Flags</span></span>           | <span data-ttu-id="dd8da-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd8da-282">0x00000000</span></span>                      |
| <span data-ttu-id="dd8da-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd8da-283">System-Flags</span></span>           | <span data-ttu-id="dd8da-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd8da-284">0x00000010</span></span>                      |
| <span data-ttu-id="dd8da-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dd8da-285">Classes used in</span></span>        | [<span data-ttu-id="dd8da-286">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dd8da-286">**Top**</span></span>](c-top.md)<br/> |



 

 





