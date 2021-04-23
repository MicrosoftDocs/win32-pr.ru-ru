---
title: Атрибут Canonical-Name
description: Имя объекта в каноническом формате.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Canonical-Name
- Схема AD атрибута Каноникалнаме
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 487476271456fa0465e8d47791f5376f33617eb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893933"
---
# <a name="canonical-name-attribute"></a><span data-ttu-id="44e6b-105">Атрибут Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="44e6b-105">Canonical-Name attribute</span></span>

<span data-ttu-id="44e6b-106">Имя объекта в каноническом формате.</span><span class="sxs-lookup"><span data-stu-id="44e6b-106">The name of the object in canonical format.</span></span> <span data-ttu-id="44e6b-107">myserver2.fabrikam.com/users/jeffsmith — это пример различающегося имени в каноническом формате.</span><span class="sxs-lookup"><span data-stu-id="44e6b-107">myserver2.fabrikam.com/users/jeffsmith is an example of a distinguished name in canonical format.</span></span> <span data-ttu-id="44e6b-108">Это сконструированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="44e6b-108">This is a constructed attribute.</span></span> <span data-ttu-id="44e6b-109">Возвращаемые результаты идентичны функциям, возвращаемым следующей функцией Active Directory: DsCrackNames (NULL, \_ флаг имени DS \_ , \_ только синтаксис \_ , \_ полное доменное имя DS \_ 1779 \_ , \_ каноническое \_ имя DS,...).</span><span class="sxs-lookup"><span data-stu-id="44e6b-109">The results returned are identical to those returned by the following Active Directory function: DsCrackNames(NULL, DS\_NAME\_FLAG\_SYNTACTICAL\_ONLY, DS\_FQDN\_1779\_NAME, DS\_CANONICAL\_NAME, ...).</span></span>

<span data-ttu-id="44e6b-110">Дополнительные сведения о форматах имен см. в разделе [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span><span class="sxs-lookup"><span data-stu-id="44e6b-110">For more information about name formats, see [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span></span>



| <span data-ttu-id="44e6b-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="44e6b-111">Entry</span></span> | <span data-ttu-id="44e6b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="44e6b-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="44e6b-113">CN</span><span class="sxs-lookup"><span data-stu-id="44e6b-113">CN</span></span>                | <span data-ttu-id="44e6b-114">Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="44e6b-114">Canonical-Name</span></span>                              |
| <span data-ttu-id="44e6b-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="44e6b-115">Ldap-Display-Name</span></span> | <span data-ttu-id="44e6b-116">canonicalName</span><span class="sxs-lookup"><span data-stu-id="44e6b-116">canonicalName</span></span>                               |
| <span data-ttu-id="44e6b-117">Размер</span><span class="sxs-lookup"><span data-stu-id="44e6b-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="44e6b-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="44e6b-118">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="44e6b-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="44e6b-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="44e6b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="44e6b-120">Attribute-Id</span></span>      | <span data-ttu-id="44e6b-121">1.2.840.113556.1.4.916</span><span class="sxs-lookup"><span data-stu-id="44e6b-121">1.2.840.113556.1.4.916</span></span>                      |
| <span data-ttu-id="44e6b-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="44e6b-122">System-Id-Guid</span></span>    | <span data-ttu-id="44e6b-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="44e6b-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="44e6b-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44e6b-124">Syntax</span></span>            | [<span data-ttu-id="44e6b-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="44e6b-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="44e6b-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="44e6b-126">Implementations</span></span>

-   [<span data-ttu-id="44e6b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="44e6b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="44e6b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="44e6b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="44e6b-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="44e6b-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="44e6b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="44e6b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="44e6b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="44e6b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="44e6b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="44e6b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="44e6b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="44e6b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="44e6b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44e6b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="44e6b-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="44e6b-135">Entry</span></span> | <span data-ttu-id="44e6b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="44e6b-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="44e6b-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44e6b-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44e6b-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="44e6b-139">System-Only</span></span>            | <span data-ttu-id="44e6b-140">True</span><span class="sxs-lookup"><span data-stu-id="44e6b-140">True</span></span>                            |
| <span data-ttu-id="44e6b-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44e6b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="44e6b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-142">False</span></span>                           |
| <span data-ttu-id="44e6b-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44e6b-143">Is Indexed</span></span>             | <span data-ttu-id="44e6b-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-144">False</span></span>                           |
| <span data-ttu-id="44e6b-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44e6b-145">In Global Catalog</span></span>      | <span data-ttu-id="44e6b-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-146">False</span></span>                           |
| <span data-ttu-id="44e6b-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44e6b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="44e6b-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44e6b-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="44e6b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44e6b-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="44e6b-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44e6b-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="44e6b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-151">Search-Flags</span></span>           | <span data-ttu-id="44e6b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44e6b-152">0x00000000</span></span>                      |
| <span data-ttu-id="44e6b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-153">System-Flags</span></span>           | <span data-ttu-id="44e6b-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="44e6b-154">0x08000014</span></span>                      |
| <span data-ttu-id="44e6b-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44e6b-155">Classes used in</span></span>        | [<span data-ttu-id="44e6b-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="44e6b-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="44e6b-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="44e6b-157">Windows Server 2003</span></span>



| <span data-ttu-id="44e6b-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="44e6b-158">Entry</span></span> | <span data-ttu-id="44e6b-159">Значение</span><span class="sxs-lookup"><span data-stu-id="44e6b-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="44e6b-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44e6b-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44e6b-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="44e6b-162">System-Only</span></span>            | <span data-ttu-id="44e6b-163">True</span><span class="sxs-lookup"><span data-stu-id="44e6b-163">True</span></span>                            |
| <span data-ttu-id="44e6b-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44e6b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="44e6b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-165">False</span></span>                           |
| <span data-ttu-id="44e6b-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44e6b-166">Is Indexed</span></span>             | <span data-ttu-id="44e6b-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-167">False</span></span>                           |
| <span data-ttu-id="44e6b-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44e6b-168">In Global Catalog</span></span>      | <span data-ttu-id="44e6b-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-169">False</span></span>                           |
| <span data-ttu-id="44e6b-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44e6b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="44e6b-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44e6b-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="44e6b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44e6b-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="44e6b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44e6b-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="44e6b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-174">Search-Flags</span></span>           | <span data-ttu-id="44e6b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44e6b-175">0x00000000</span></span>                      |
| <span data-ttu-id="44e6b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-176">System-Flags</span></span>           | <span data-ttu-id="44e6b-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="44e6b-177">0x08000014</span></span>                      |
| <span data-ttu-id="44e6b-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44e6b-178">Classes used in</span></span>        | [<span data-ttu-id="44e6b-179">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="44e6b-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="44e6b-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="44e6b-180">ADAM</span></span>



| <span data-ttu-id="44e6b-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="44e6b-181">Entry</span></span> | <span data-ttu-id="44e6b-182">Значение</span><span class="sxs-lookup"><span data-stu-id="44e6b-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="44e6b-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44e6b-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44e6b-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="44e6b-185">System-Only</span></span>            | <span data-ttu-id="44e6b-186">True</span><span class="sxs-lookup"><span data-stu-id="44e6b-186">True</span></span>                            |
| <span data-ttu-id="44e6b-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44e6b-187">Is-Single-Valued</span></span>       | <span data-ttu-id="44e6b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-188">False</span></span>                           |
| <span data-ttu-id="44e6b-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44e6b-189">Is Indexed</span></span>             | <span data-ttu-id="44e6b-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-190">False</span></span>                           |
| <span data-ttu-id="44e6b-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44e6b-191">In Global Catalog</span></span>      | <span data-ttu-id="44e6b-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-192">False</span></span>                           |
| <span data-ttu-id="44e6b-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44e6b-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="44e6b-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44e6b-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="44e6b-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44e6b-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="44e6b-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44e6b-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="44e6b-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-197">Search-Flags</span></span>           | <span data-ttu-id="44e6b-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44e6b-198">0x00000000</span></span>                      |
| <span data-ttu-id="44e6b-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-199">System-Flags</span></span>           | <span data-ttu-id="44e6b-200">0x08000014</span><span class="sxs-lookup"><span data-stu-id="44e6b-200">0x08000014</span></span>                      |
| <span data-ttu-id="44e6b-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44e6b-201">Classes used in</span></span>        | [<span data-ttu-id="44e6b-202">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="44e6b-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="44e6b-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="44e6b-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="44e6b-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="44e6b-204">Entry</span></span> | <span data-ttu-id="44e6b-205">Значение</span><span class="sxs-lookup"><span data-stu-id="44e6b-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="44e6b-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44e6b-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44e6b-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="44e6b-208">System-Only</span></span>            | <span data-ttu-id="44e6b-209">True</span><span class="sxs-lookup"><span data-stu-id="44e6b-209">True</span></span>                            |
| <span data-ttu-id="44e6b-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44e6b-210">Is-Single-Valued</span></span>       | <span data-ttu-id="44e6b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-211">False</span></span>                           |
| <span data-ttu-id="44e6b-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44e6b-212">Is Indexed</span></span>             | <span data-ttu-id="44e6b-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-213">False</span></span>                           |
| <span data-ttu-id="44e6b-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44e6b-214">In Global Catalog</span></span>      | <span data-ttu-id="44e6b-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-215">False</span></span>                           |
| <span data-ttu-id="44e6b-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44e6b-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="44e6b-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44e6b-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="44e6b-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44e6b-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="44e6b-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44e6b-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="44e6b-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-220">Search-Flags</span></span>           | <span data-ttu-id="44e6b-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44e6b-221">0x00000000</span></span>                      |
| <span data-ttu-id="44e6b-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-222">System-Flags</span></span>           | <span data-ttu-id="44e6b-223">0x08000014</span><span class="sxs-lookup"><span data-stu-id="44e6b-223">0x08000014</span></span>                      |
| <span data-ttu-id="44e6b-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44e6b-224">Classes used in</span></span>        | [<span data-ttu-id="44e6b-225">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="44e6b-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="44e6b-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44e6b-226">Windows Server 2008</span></span>



| <span data-ttu-id="44e6b-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="44e6b-227">Entry</span></span> | <span data-ttu-id="44e6b-228">Значение</span><span class="sxs-lookup"><span data-stu-id="44e6b-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="44e6b-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44e6b-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44e6b-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="44e6b-231">System-Only</span></span>            | <span data-ttu-id="44e6b-232">True</span><span class="sxs-lookup"><span data-stu-id="44e6b-232">True</span></span>                            |
| <span data-ttu-id="44e6b-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44e6b-233">Is-Single-Valued</span></span>       | <span data-ttu-id="44e6b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-234">False</span></span>                           |
| <span data-ttu-id="44e6b-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44e6b-235">Is Indexed</span></span>             | <span data-ttu-id="44e6b-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-236">False</span></span>                           |
| <span data-ttu-id="44e6b-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44e6b-237">In Global Catalog</span></span>      | <span data-ttu-id="44e6b-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-238">False</span></span>                           |
| <span data-ttu-id="44e6b-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44e6b-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="44e6b-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44e6b-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="44e6b-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44e6b-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="44e6b-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44e6b-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="44e6b-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-243">Search-Flags</span></span>           | <span data-ttu-id="44e6b-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44e6b-244">0x00000000</span></span>                      |
| <span data-ttu-id="44e6b-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-245">System-Flags</span></span>           | <span data-ttu-id="44e6b-246">0x08000014</span><span class="sxs-lookup"><span data-stu-id="44e6b-246">0x08000014</span></span>                      |
| <span data-ttu-id="44e6b-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44e6b-247">Classes used in</span></span>        | [<span data-ttu-id="44e6b-248">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="44e6b-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="44e6b-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="44e6b-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="44e6b-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="44e6b-250">Entry</span></span> | <span data-ttu-id="44e6b-251">Значение</span><span class="sxs-lookup"><span data-stu-id="44e6b-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="44e6b-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44e6b-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44e6b-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="44e6b-254">System-Only</span></span>            | <span data-ttu-id="44e6b-255">True</span><span class="sxs-lookup"><span data-stu-id="44e6b-255">True</span></span>                            |
| <span data-ttu-id="44e6b-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44e6b-256">Is-Single-Valued</span></span>       | <span data-ttu-id="44e6b-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-257">False</span></span>                           |
| <span data-ttu-id="44e6b-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44e6b-258">Is Indexed</span></span>             | <span data-ttu-id="44e6b-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-259">False</span></span>                           |
| <span data-ttu-id="44e6b-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44e6b-260">In Global Catalog</span></span>      | <span data-ttu-id="44e6b-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-261">False</span></span>                           |
| <span data-ttu-id="44e6b-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44e6b-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="44e6b-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44e6b-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="44e6b-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44e6b-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="44e6b-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44e6b-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="44e6b-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-266">Search-Flags</span></span>           | <span data-ttu-id="44e6b-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44e6b-267">0x00000000</span></span>                      |
| <span data-ttu-id="44e6b-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-268">System-Flags</span></span>           | <span data-ttu-id="44e6b-269">0x08000014</span><span class="sxs-lookup"><span data-stu-id="44e6b-269">0x08000014</span></span>                      |
| <span data-ttu-id="44e6b-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44e6b-270">Classes used in</span></span>        | [<span data-ttu-id="44e6b-271">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="44e6b-271">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="44e6b-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44e6b-272">Windows Server 2012</span></span>



| <span data-ttu-id="44e6b-273">Ввод</span><span class="sxs-lookup"><span data-stu-id="44e6b-273">Entry</span></span> | <span data-ttu-id="44e6b-274">Значение</span><span class="sxs-lookup"><span data-stu-id="44e6b-274">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="44e6b-275">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44e6b-275">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44e6b-276">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="44e6b-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="44e6b-277">System-Only</span></span>            | <span data-ttu-id="44e6b-278">True</span><span class="sxs-lookup"><span data-stu-id="44e6b-278">True</span></span>                            |
| <span data-ttu-id="44e6b-279">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44e6b-279">Is-Single-Valued</span></span>       | <span data-ttu-id="44e6b-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-280">False</span></span>                           |
| <span data-ttu-id="44e6b-281">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44e6b-281">Is Indexed</span></span>             | <span data-ttu-id="44e6b-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-282">False</span></span>                           |
| <span data-ttu-id="44e6b-283">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44e6b-283">In Global Catalog</span></span>      | <span data-ttu-id="44e6b-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="44e6b-284">False</span></span>                           |
| <span data-ttu-id="44e6b-285">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44e6b-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="44e6b-286">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44e6b-286">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="44e6b-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44e6b-287">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="44e6b-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44e6b-288">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="44e6b-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-289">Search-Flags</span></span>           | <span data-ttu-id="44e6b-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44e6b-290">0x00000000</span></span>                      |
| <span data-ttu-id="44e6b-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44e6b-291">System-Flags</span></span>           | <span data-ttu-id="44e6b-292">0x08000014</span><span class="sxs-lookup"><span data-stu-id="44e6b-292">0x08000014</span></span>                      |
| <span data-ttu-id="44e6b-293">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44e6b-293">Classes used in</span></span>        | [<span data-ttu-id="44e6b-294">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="44e6b-294">**Top**</span></span>](c-top.md)<br/> |



 

