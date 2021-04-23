---
title: атрибут Мссфу-30-Order-Number
description: Содержит значение, используемое NIS для проверки изменения схемы.
ms.assetid: b2e83980-2de4-4001-b65a-8073c9258b27
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Мссфу-30-Order-Number
- Схема AD атрибута msSFU30OrderNumber
topic_type:
- apiref
api_name:
- msSFU-30-Order-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af67f1b5d6fdff8ca4a7739276443d67fa35679f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138582"
---
# <a name="mssfu-30-order-number-attribute"></a><span data-ttu-id="b7de5-105">атрибут Мссфу-30-Order-Number</span><span class="sxs-lookup"><span data-stu-id="b7de5-105">msSFU-30-Order-Number attribute</span></span>

<span data-ttu-id="b7de5-106">Содержит значение, используемое NIS для проверки изменения схемы.</span><span class="sxs-lookup"><span data-stu-id="b7de5-106">Contains a value that is used by NIS to check if the map has changed.</span></span> <span data-ttu-id="b7de5-107">При каждом изменении данных, хранящихся в объекте [**мссфу-30-Domain-info**](c-mssfu30domaininfo.md) , это значение увеличивается.</span><span class="sxs-lookup"><span data-stu-id="b7de5-107">Every time the data stored in the [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) object changes, this value is incremented.</span></span> <span data-ttu-id="b7de5-108">Это значение используется для контроля изменений данных между вызовами **ипксфер** .</span><span class="sxs-lookup"><span data-stu-id="b7de5-108">This value is used to track data changes between **ypxfer** calls.</span></span>



| <span data-ttu-id="b7de5-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7de5-109">Entry</span></span> | <span data-ttu-id="b7de5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b7de5-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b7de5-111">CN</span><span class="sxs-lookup"><span data-stu-id="b7de5-111">CN</span></span>                | <span data-ttu-id="b7de5-112">Мссфу-30-порядок-номер</span><span class="sxs-lookup"><span data-stu-id="b7de5-112">msSFU-30-Order-Number</span></span>                       |
| <span data-ttu-id="b7de5-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b7de5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b7de5-114">msSFU30OrderNumber</span><span class="sxs-lookup"><span data-stu-id="b7de5-114">msSFU30OrderNumber</span></span>                          |
| <span data-ttu-id="b7de5-115">Размер</span><span class="sxs-lookup"><span data-stu-id="b7de5-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="b7de5-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b7de5-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b7de5-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b7de5-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b7de5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7de5-118">Attribute-Id</span></span>      | <span data-ttu-id="b7de5-119">1.2.840.113556.1.6.18.1.308</span><span class="sxs-lookup"><span data-stu-id="b7de5-119">1.2.840.113556.1.6.18.1.308</span></span>                 |
| <span data-ttu-id="b7de5-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b7de5-120">System-Id-Guid</span></span>    | <span data-ttu-id="b7de5-121">02625f05-d1ee-4f9f-b366-55266becb95c</span><span class="sxs-lookup"><span data-stu-id="b7de5-121">02625f05-d1ee-4f9f-b366-55266becb95c</span></span>        |
| <span data-ttu-id="b7de5-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7de5-122">Syntax</span></span>            | [<span data-ttu-id="b7de5-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="b7de5-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b7de5-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b7de5-124">Implementations</span></span>

-   [<span data-ttu-id="b7de5-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7de5-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7de5-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7de5-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7de5-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7de5-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7de5-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7de5-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7de5-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7de5-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7de5-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7de5-130">Entry</span></span> | <span data-ttu-id="b7de5-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b7de5-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b7de5-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7de5-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7de5-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7de5-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7de5-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7de5-134">System-Only</span></span>            | <span data-ttu-id="b7de5-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7de5-135">False</span></span>                                                          |
| <span data-ttu-id="b7de5-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7de5-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b7de5-137">True</span><span class="sxs-lookup"><span data-stu-id="b7de5-137">True</span></span>                                                           |
| <span data-ttu-id="b7de5-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7de5-138">Is Indexed</span></span>             | <span data-ttu-id="b7de5-139">True</span><span class="sxs-lookup"><span data-stu-id="b7de5-139">True</span></span>                                                           |
| <span data-ttu-id="b7de5-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7de5-140">In Global Catalog</span></span>      | <span data-ttu-id="b7de5-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7de5-141">False</span></span>                                                          |
| <span data-ttu-id="b7de5-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7de5-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7de5-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7de5-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b7de5-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7de5-144">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="b7de5-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7de5-145">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="b7de5-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7de5-146">Search-Flags</span></span>           | <span data-ttu-id="b7de5-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7de5-147">0x00000001</span></span>                                                     |
| <span data-ttu-id="b7de5-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7de5-148">System-Flags</span></span>           | <span data-ttu-id="b7de5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7de5-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="b7de5-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7de5-150">Classes used in</span></span>        | [<span data-ttu-id="b7de5-151">**Мссфу-30 — сведения о домене**</span><span class="sxs-lookup"><span data-stu-id="b7de5-151">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7de5-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7de5-152">Windows Server 2008</span></span>



| <span data-ttu-id="b7de5-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7de5-153">Entry</span></span> | <span data-ttu-id="b7de5-154">Значение</span><span class="sxs-lookup"><span data-stu-id="b7de5-154">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b7de5-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7de5-155">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7de5-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7de5-156">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7de5-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7de5-157">System-Only</span></span>            | <span data-ttu-id="b7de5-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7de5-158">False</span></span>                                                          |
| <span data-ttu-id="b7de5-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7de5-159">Is-Single-Valued</span></span>       | <span data-ttu-id="b7de5-160">True</span><span class="sxs-lookup"><span data-stu-id="b7de5-160">True</span></span>                                                           |
| <span data-ttu-id="b7de5-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7de5-161">Is Indexed</span></span>             | <span data-ttu-id="b7de5-162">True</span><span class="sxs-lookup"><span data-stu-id="b7de5-162">True</span></span>                                                           |
| <span data-ttu-id="b7de5-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7de5-163">In Global Catalog</span></span>      | <span data-ttu-id="b7de5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7de5-164">False</span></span>                                                          |
| <span data-ttu-id="b7de5-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7de5-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7de5-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7de5-166">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b7de5-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7de5-167">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="b7de5-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7de5-168">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="b7de5-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7de5-169">Search-Flags</span></span>           | <span data-ttu-id="b7de5-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7de5-170">0x00000001</span></span>                                                     |
| <span data-ttu-id="b7de5-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7de5-171">System-Flags</span></span>           | <span data-ttu-id="b7de5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7de5-172">0x00000000</span></span>                                                     |
| <span data-ttu-id="b7de5-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7de5-173">Classes used in</span></span>        | [<span data-ttu-id="b7de5-174">**Мссфу-30 — сведения о домене**</span><span class="sxs-lookup"><span data-stu-id="b7de5-174">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7de5-175">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7de5-175">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7de5-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7de5-176">Entry</span></span> | <span data-ttu-id="b7de5-177">Значение</span><span class="sxs-lookup"><span data-stu-id="b7de5-177">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b7de5-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7de5-178">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7de5-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7de5-179">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7de5-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7de5-180">System-Only</span></span>            | <span data-ttu-id="b7de5-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7de5-181">False</span></span>                                                          |
| <span data-ttu-id="b7de5-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7de5-182">Is-Single-Valued</span></span>       | <span data-ttu-id="b7de5-183">True</span><span class="sxs-lookup"><span data-stu-id="b7de5-183">True</span></span>                                                           |
| <span data-ttu-id="b7de5-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7de5-184">Is Indexed</span></span>             | <span data-ttu-id="b7de5-185">True</span><span class="sxs-lookup"><span data-stu-id="b7de5-185">True</span></span>                                                           |
| <span data-ttu-id="b7de5-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7de5-186">In Global Catalog</span></span>      | <span data-ttu-id="b7de5-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7de5-187">False</span></span>                                                          |
| <span data-ttu-id="b7de5-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7de5-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7de5-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7de5-189">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b7de5-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7de5-190">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="b7de5-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7de5-191">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="b7de5-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7de5-192">Search-Flags</span></span>           | <span data-ttu-id="b7de5-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7de5-193">0x00000001</span></span>                                                     |
| <span data-ttu-id="b7de5-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7de5-194">System-Flags</span></span>           | <span data-ttu-id="b7de5-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7de5-195">0x00000000</span></span>                                                     |
| <span data-ttu-id="b7de5-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7de5-196">Classes used in</span></span>        | [<span data-ttu-id="b7de5-197">**Мссфу-30 — сведения о домене**</span><span class="sxs-lookup"><span data-stu-id="b7de5-197">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7de5-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7de5-198">Windows Server 2012</span></span>



| <span data-ttu-id="b7de5-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7de5-199">Entry</span></span> | <span data-ttu-id="b7de5-200">Значение</span><span class="sxs-lookup"><span data-stu-id="b7de5-200">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b7de5-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7de5-201">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7de5-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7de5-202">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b7de5-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7de5-203">System-Only</span></span>            | <span data-ttu-id="b7de5-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7de5-204">False</span></span>                                                          |
| <span data-ttu-id="b7de5-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7de5-205">Is-Single-Valued</span></span>       | <span data-ttu-id="b7de5-206">True</span><span class="sxs-lookup"><span data-stu-id="b7de5-206">True</span></span>                                                           |
| <span data-ttu-id="b7de5-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7de5-207">Is Indexed</span></span>             | <span data-ttu-id="b7de5-208">True</span><span class="sxs-lookup"><span data-stu-id="b7de5-208">True</span></span>                                                           |
| <span data-ttu-id="b7de5-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7de5-209">In Global Catalog</span></span>      | <span data-ttu-id="b7de5-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7de5-210">False</span></span>                                                          |
| <span data-ttu-id="b7de5-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7de5-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7de5-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7de5-212">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b7de5-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7de5-213">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="b7de5-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7de5-214">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="b7de5-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7de5-215">Search-Flags</span></span>           | <span data-ttu-id="b7de5-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7de5-216">0x00000001</span></span>                                                     |
| <span data-ttu-id="b7de5-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7de5-217">System-Flags</span></span>           | <span data-ttu-id="b7de5-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7de5-218">0x00000000</span></span>                                                     |
| <span data-ttu-id="b7de5-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7de5-219">Classes used in</span></span>        | [<span data-ttu-id="b7de5-220">**Мссфу-30 — сведения о домене**</span><span class="sxs-lookup"><span data-stu-id="b7de5-220">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



 

 





