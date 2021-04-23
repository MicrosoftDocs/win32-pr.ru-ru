---
title: Атрибут ms-DS-SPN-суффиксов
description: Этот атрибут описывает суффиксы имен узлов DNS, используемых серверами в лесу. Эти DNS-суффиксы будут использоваться совместно с другими лесами, которые имеют доверие между лесами с этим лесом.
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-SPN-суффиксов
- Схема AD атрибута msDS-Спнсуффиксес
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91f7ce8c92e8a81437d90bb0d80383b9ad334ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989695"
---
# <a name="ms-ds-spn-suffixes-attribute"></a><span data-ttu-id="7d435-106">Атрибут ms-DS-SPN-суффиксов</span><span class="sxs-lookup"><span data-stu-id="7d435-106">ms-DS-SPN-Suffixes attribute</span></span>

<span data-ttu-id="7d435-107">Этот атрибут описывает суффиксы имен узлов DNS, используемых серверами в лесу.</span><span class="sxs-lookup"><span data-stu-id="7d435-107">This attribute describes the suffixes of DNS host names used by servers in the forest.</span></span> <span data-ttu-id="7d435-108">Эти DNS-суффиксы будут использоваться совместно с другими лесами, которые имеют доверие между лесами с этим лесом.</span><span class="sxs-lookup"><span data-stu-id="7d435-108">These DNS suffixes will be shared with other forests that have cross-forest trust with this forest.</span></span>



| <span data-ttu-id="7d435-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="7d435-109">Entry</span></span> | <span data-ttu-id="7d435-110">Значение</span><span class="sxs-lookup"><span data-stu-id="7d435-110">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="7d435-111">CN</span><span class="sxs-lookup"><span data-stu-id="7d435-111">CN</span></span>                | <span data-ttu-id="7d435-112">Суффиксы MS-DS-SPN</span><span class="sxs-lookup"><span data-stu-id="7d435-112">ms-DS-SPN-Suffixes</span></span>                           |
| <span data-ttu-id="7d435-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7d435-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7d435-114">msDS-Спнсуффиксес</span><span class="sxs-lookup"><span data-stu-id="7d435-114">msDS-SPNSuffixes</span></span>                             |
| <span data-ttu-id="7d435-115">Размер</span><span class="sxs-lookup"><span data-stu-id="7d435-115">Size</span></span>              | <span data-ttu-id="7d435-116">255 байт</span><span class="sxs-lookup"><span data-stu-id="7d435-116">255 bytes</span></span>                                    |
| <span data-ttu-id="7d435-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7d435-117">Update Privilege</span></span>  | <span data-ttu-id="7d435-118">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="7d435-118">Domain administrator</span></span>                         |
| <span data-ttu-id="7d435-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7d435-119">Update Frequency</span></span>  | <span data-ttu-id="7d435-120">Когда серверы в лесу получают новый суффикс.</span><span class="sxs-lookup"><span data-stu-id="7d435-120">When servers in the forest get a new suffix.</span></span> |
| <span data-ttu-id="7d435-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7d435-121">Attribute-Id</span></span>      | <span data-ttu-id="7d435-122">1.2.840.113556.1.4.1715</span><span class="sxs-lookup"><span data-stu-id="7d435-122">1.2.840.113556.1.4.1715</span></span>                      |
| <span data-ttu-id="7d435-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7d435-123">System-Id-Guid</span></span>    | <span data-ttu-id="7d435-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span><span class="sxs-lookup"><span data-stu-id="7d435-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span></span>         |
| <span data-ttu-id="7d435-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d435-125">Syntax</span></span>            | [<span data-ttu-id="7d435-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="7d435-126">**String(Unicode)**</span></span>](s-string-unicode.md)  |



## <a name="implementations"></a><span data-ttu-id="7d435-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7d435-127">Implementations</span></span>

-   [<span data-ttu-id="7d435-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7d435-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7d435-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7d435-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7d435-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7d435-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7d435-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7d435-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7d435-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7d435-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7d435-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7d435-133">Windows Server 2003</span></span>



| <span data-ttu-id="7d435-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="7d435-134">Entry</span></span> | <span data-ttu-id="7d435-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7d435-135">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7d435-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7d435-136">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d435-137">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d435-138">System-Only</span></span>            | <span data-ttu-id="7d435-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-139">False</span></span>                                                         |
| <span data-ttu-id="7d435-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7d435-140">Is-Single-Valued</span></span>       | <span data-ttu-id="7d435-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-141">False</span></span>                                                         |
| <span data-ttu-id="7d435-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7d435-142">Is Indexed</span></span>             | <span data-ttu-id="7d435-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-143">False</span></span>                                                         |
| <span data-ttu-id="7d435-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7d435-144">In Global Catalog</span></span>      | <span data-ttu-id="7d435-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-145">False</span></span>                                                         |
| <span data-ttu-id="7d435-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7d435-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d435-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7d435-147">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="7d435-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d435-148">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d435-149">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-150">Search-Flags</span></span>           | <span data-ttu-id="7d435-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d435-151">0x00000000</span></span>                                                    |
| <span data-ttu-id="7d435-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-152">System-Flags</span></span>           | <span data-ttu-id="7d435-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d435-153">0x00000010</span></span>                                                    |
| <span data-ttu-id="7d435-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7d435-154">Classes used in</span></span>        | [<span data-ttu-id="7d435-155">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="7d435-155">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7d435-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7d435-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7d435-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="7d435-157">Entry</span></span> | <span data-ttu-id="7d435-158">Значение</span><span class="sxs-lookup"><span data-stu-id="7d435-158">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7d435-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7d435-159">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d435-160">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d435-161">System-Only</span></span>            | <span data-ttu-id="7d435-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-162">False</span></span>                                                         |
| <span data-ttu-id="7d435-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7d435-163">Is-Single-Valued</span></span>       | <span data-ttu-id="7d435-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-164">False</span></span>                                                         |
| <span data-ttu-id="7d435-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7d435-165">Is Indexed</span></span>             | <span data-ttu-id="7d435-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-166">False</span></span>                                                         |
| <span data-ttu-id="7d435-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7d435-167">In Global Catalog</span></span>      | <span data-ttu-id="7d435-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-168">False</span></span>                                                         |
| <span data-ttu-id="7d435-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7d435-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d435-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7d435-170">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="7d435-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d435-171">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d435-172">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-173">Search-Flags</span></span>           | <span data-ttu-id="7d435-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d435-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="7d435-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-175">System-Flags</span></span>           | <span data-ttu-id="7d435-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d435-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="7d435-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7d435-177">Classes used in</span></span>        | [<span data-ttu-id="7d435-178">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="7d435-178">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7d435-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d435-179">Windows Server 2008</span></span>



| <span data-ttu-id="7d435-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="7d435-180">Entry</span></span> | <span data-ttu-id="7d435-181">Значение</span><span class="sxs-lookup"><span data-stu-id="7d435-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7d435-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7d435-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d435-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d435-184">System-Only</span></span>            | <span data-ttu-id="7d435-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-185">False</span></span>                                                         |
| <span data-ttu-id="7d435-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7d435-186">Is-Single-Valued</span></span>       | <span data-ttu-id="7d435-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-187">False</span></span>                                                         |
| <span data-ttu-id="7d435-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7d435-188">Is Indexed</span></span>             | <span data-ttu-id="7d435-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-189">False</span></span>                                                         |
| <span data-ttu-id="7d435-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7d435-190">In Global Catalog</span></span>      | <span data-ttu-id="7d435-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-191">False</span></span>                                                         |
| <span data-ttu-id="7d435-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7d435-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d435-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7d435-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="7d435-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d435-194">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d435-195">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-196">Search-Flags</span></span>           | <span data-ttu-id="7d435-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d435-197">0x00000000</span></span>                                                    |
| <span data-ttu-id="7d435-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-198">System-Flags</span></span>           | <span data-ttu-id="7d435-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d435-199">0x00000010</span></span>                                                    |
| <span data-ttu-id="7d435-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7d435-200">Classes used in</span></span>        | [<span data-ttu-id="7d435-201">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="7d435-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7d435-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d435-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7d435-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="7d435-203">Entry</span></span> | <span data-ttu-id="7d435-204">Значение</span><span class="sxs-lookup"><span data-stu-id="7d435-204">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7d435-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7d435-205">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d435-206">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d435-207">System-Only</span></span>            | <span data-ttu-id="7d435-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-208">False</span></span>                                                         |
| <span data-ttu-id="7d435-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7d435-209">Is-Single-Valued</span></span>       | <span data-ttu-id="7d435-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-210">False</span></span>                                                         |
| <span data-ttu-id="7d435-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7d435-211">Is Indexed</span></span>             | <span data-ttu-id="7d435-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-212">False</span></span>                                                         |
| <span data-ttu-id="7d435-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7d435-213">In Global Catalog</span></span>      | <span data-ttu-id="7d435-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-214">False</span></span>                                                         |
| <span data-ttu-id="7d435-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7d435-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d435-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7d435-216">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="7d435-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d435-217">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d435-218">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-219">Search-Flags</span></span>           | <span data-ttu-id="7d435-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d435-220">0x00000000</span></span>                                                    |
| <span data-ttu-id="7d435-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-221">System-Flags</span></span>           | <span data-ttu-id="7d435-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d435-222">0x00000010</span></span>                                                    |
| <span data-ttu-id="7d435-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7d435-223">Classes used in</span></span>        | [<span data-ttu-id="7d435-224">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="7d435-224">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7d435-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d435-225">Windows Server 2012</span></span>



| <span data-ttu-id="7d435-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="7d435-226">Entry</span></span> | <span data-ttu-id="7d435-227">Значение</span><span class="sxs-lookup"><span data-stu-id="7d435-227">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7d435-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7d435-228">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7d435-229">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="7d435-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="7d435-230">System-Only</span></span>            | <span data-ttu-id="7d435-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-231">False</span></span>                                                         |
| <span data-ttu-id="7d435-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7d435-232">Is-Single-Valued</span></span>       | <span data-ttu-id="7d435-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-233">False</span></span>                                                         |
| <span data-ttu-id="7d435-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7d435-234">Is Indexed</span></span>             | <span data-ttu-id="7d435-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-235">False</span></span>                                                         |
| <span data-ttu-id="7d435-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7d435-236">In Global Catalog</span></span>      | <span data-ttu-id="7d435-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="7d435-237">False</span></span>                                                         |
| <span data-ttu-id="7d435-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7d435-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="7d435-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7d435-239">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="7d435-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7d435-240">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7d435-241">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="7d435-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-242">Search-Flags</span></span>           | <span data-ttu-id="7d435-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d435-243">0x00000000</span></span>                                                    |
| <span data-ttu-id="7d435-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7d435-244">System-Flags</span></span>           | <span data-ttu-id="7d435-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d435-245">0x00000010</span></span>                                                    |
| <span data-ttu-id="7d435-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7d435-246">Classes used in</span></span>        | [<span data-ttu-id="7d435-247">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="7d435-247">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





