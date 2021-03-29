---
title: ГПК-WQL-атрибут Filter
description: Используется для хранения строки, содержащей идентификатор GUID для фильтра и пути к пространству имен WMI.
ms.assetid: ea76239b-79e2-49b2-a848-a924450d332a
ms.tgt_platform: multiple
keywords:
- ГПК-WQL-фильтр атрибутов Active Directory
- Схема AD атрибута Гпквклфилтер
topic_type:
- apiref
api_name:
- GPC-WQL-Filter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9a6b8d3715c1692e93579d3c94cdfa44f4192e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893598"
---
# <a name="gpc-wql-filter-attribute"></a><span data-ttu-id="7ddeb-105">ГПК-WQL-атрибут Filter</span><span class="sxs-lookup"><span data-stu-id="7ddeb-105">GPC-WQL-Filter attribute</span></span>

<span data-ttu-id="7ddeb-106">Используется для хранения строки, содержащей идентификатор GUID для фильтра и пути к пространству имен WMI.</span><span class="sxs-lookup"><span data-stu-id="7ddeb-106">Used to store a string that contains a GUID for the filter and a WMI namespace path.</span></span>



| <span data-ttu-id="7ddeb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ddeb-107">Entry</span></span> | <span data-ttu-id="7ddeb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7ddeb-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="7ddeb-109">CN</span><span class="sxs-lookup"><span data-stu-id="7ddeb-109">CN</span></span>                | <span data-ttu-id="7ddeb-110">ГПК-WQL-Filter</span><span class="sxs-lookup"><span data-stu-id="7ddeb-110">GPC-WQL-Filter</span></span>                                                                  |
| <span data-ttu-id="7ddeb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7ddeb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7ddeb-112">гпквклфилтер</span><span class="sxs-lookup"><span data-stu-id="7ddeb-112">gPCWQLFilter</span></span>                                                                    |
| <span data-ttu-id="7ddeb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7ddeb-113">Size</span></span>              | \-                                                                              |
| <span data-ttu-id="7ddeb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7ddeb-114">Update Privilege</span></span>  | <span data-ttu-id="7ddeb-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="7ddeb-115">Domain administrator</span></span>                                                            |
| <span data-ttu-id="7ddeb-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7ddeb-116">Update Frequency</span></span>  | <span data-ttu-id="7ddeb-117">Только в том случае, если администратор изменяет свойство Filter в пользовательском интерфейсе групповая политика.</span><span class="sxs-lookup"><span data-stu-id="7ddeb-117">Only when the administrator changes the filter property in the Group Policy UI.</span></span> |
| <span data-ttu-id="7ddeb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7ddeb-118">Attribute-Id</span></span>      | <span data-ttu-id="7ddeb-119">1.2.840.113556.1.4.1694</span><span class="sxs-lookup"><span data-stu-id="7ddeb-119">1.2.840.113556.1.4.1694</span></span>                                                         |
| <span data-ttu-id="7ddeb-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7ddeb-120">System-Id-Guid</span></span>    | <span data-ttu-id="7ddeb-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span><span class="sxs-lookup"><span data-stu-id="7ddeb-121">7bd4c7a6-1add-4436-8c04-3999a880154c</span></span>                                            |
| <span data-ttu-id="7ddeb-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ddeb-122">Syntax</span></span>            | [<span data-ttu-id="7ddeb-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="7ddeb-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7ddeb-124">Implementations</span></span>

-   [<span data-ttu-id="7ddeb-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7ddeb-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7ddeb-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7ddeb-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7ddeb-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7ddeb-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ddeb-130">Windows Server 2003</span></span>



| <span data-ttu-id="7ddeb-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ddeb-131">Entry</span></span> | <span data-ttu-id="7ddeb-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7ddeb-132">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7ddeb-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ddeb-133">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ddeb-134">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ddeb-135">System-Only</span></span>            | <span data-ttu-id="7ddeb-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-136">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ddeb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7ddeb-138">True</span><span class="sxs-lookup"><span data-stu-id="7ddeb-138">True</span></span>                                                                |
| <span data-ttu-id="7ddeb-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ddeb-139">Is Indexed</span></span>             | <span data-ttu-id="7ddeb-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-140">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ddeb-141">In Global Catalog</span></span>      | <span data-ttu-id="7ddeb-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-142">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ddeb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ddeb-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ddeb-144">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7ddeb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ddeb-145">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ddeb-146">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-147">Search-Flags</span></span>           | <span data-ttu-id="7ddeb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ddeb-148">0x00000000</span></span>                                                          |
| <span data-ttu-id="7ddeb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-149">System-Flags</span></span>           | <span data-ttu-id="7ddeb-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ddeb-150">0x00000010</span></span>                                                          |
| <span data-ttu-id="7ddeb-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ddeb-151">Classes used in</span></span>        | [<span data-ttu-id="7ddeb-152">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-152">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7ddeb-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7ddeb-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7ddeb-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ddeb-154">Entry</span></span> | <span data-ttu-id="7ddeb-155">Значение</span><span class="sxs-lookup"><span data-stu-id="7ddeb-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7ddeb-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ddeb-156">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ddeb-157">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ddeb-158">System-Only</span></span>            | <span data-ttu-id="7ddeb-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-159">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ddeb-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7ddeb-161">True</span><span class="sxs-lookup"><span data-stu-id="7ddeb-161">True</span></span>                                                                |
| <span data-ttu-id="7ddeb-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ddeb-162">Is Indexed</span></span>             | <span data-ttu-id="7ddeb-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-163">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ddeb-164">In Global Catalog</span></span>      | <span data-ttu-id="7ddeb-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-165">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ddeb-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ddeb-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ddeb-167">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7ddeb-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ddeb-168">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ddeb-169">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-170">Search-Flags</span></span>           | <span data-ttu-id="7ddeb-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ddeb-171">0x00000000</span></span>                                                          |
| <span data-ttu-id="7ddeb-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-172">System-Flags</span></span>           | <span data-ttu-id="7ddeb-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ddeb-173">0x00000010</span></span>                                                          |
| <span data-ttu-id="7ddeb-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ddeb-174">Classes used in</span></span>        | [<span data-ttu-id="7ddeb-175">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-175">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7ddeb-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ddeb-176">Windows Server 2008</span></span>



| <span data-ttu-id="7ddeb-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ddeb-177">Entry</span></span> | <span data-ttu-id="7ddeb-178">Значение</span><span class="sxs-lookup"><span data-stu-id="7ddeb-178">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7ddeb-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ddeb-179">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ddeb-180">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ddeb-181">System-Only</span></span>            | <span data-ttu-id="7ddeb-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-182">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ddeb-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7ddeb-184">True</span><span class="sxs-lookup"><span data-stu-id="7ddeb-184">True</span></span>                                                                |
| <span data-ttu-id="7ddeb-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ddeb-185">Is Indexed</span></span>             | <span data-ttu-id="7ddeb-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-186">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ddeb-187">In Global Catalog</span></span>      | <span data-ttu-id="7ddeb-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-188">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ddeb-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ddeb-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ddeb-190">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7ddeb-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ddeb-191">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ddeb-192">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-193">Search-Flags</span></span>           | <span data-ttu-id="7ddeb-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ddeb-194">0x00000000</span></span>                                                          |
| <span data-ttu-id="7ddeb-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-195">System-Flags</span></span>           | <span data-ttu-id="7ddeb-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ddeb-196">0x00000010</span></span>                                                          |
| <span data-ttu-id="7ddeb-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ddeb-197">Classes used in</span></span>        | [<span data-ttu-id="7ddeb-198">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-198">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7ddeb-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ddeb-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7ddeb-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ddeb-200">Entry</span></span> | <span data-ttu-id="7ddeb-201">Значение</span><span class="sxs-lookup"><span data-stu-id="7ddeb-201">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7ddeb-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ddeb-202">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ddeb-203">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ddeb-204">System-Only</span></span>            | <span data-ttu-id="7ddeb-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-205">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ddeb-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7ddeb-207">True</span><span class="sxs-lookup"><span data-stu-id="7ddeb-207">True</span></span>                                                                |
| <span data-ttu-id="7ddeb-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ddeb-208">Is Indexed</span></span>             | <span data-ttu-id="7ddeb-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-209">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ddeb-210">In Global Catalog</span></span>      | <span data-ttu-id="7ddeb-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-211">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ddeb-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ddeb-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ddeb-213">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7ddeb-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ddeb-214">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ddeb-215">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-216">Search-Flags</span></span>           | <span data-ttu-id="7ddeb-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ddeb-217">0x00000000</span></span>                                                          |
| <span data-ttu-id="7ddeb-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-218">System-Flags</span></span>           | <span data-ttu-id="7ddeb-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ddeb-219">0x00000010</span></span>                                                          |
| <span data-ttu-id="7ddeb-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ddeb-220">Classes used in</span></span>        | [<span data-ttu-id="7ddeb-221">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-221">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7ddeb-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ddeb-222">Windows Server 2012</span></span>



| <span data-ttu-id="7ddeb-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="7ddeb-223">Entry</span></span> | <span data-ttu-id="7ddeb-224">Значение</span><span class="sxs-lookup"><span data-stu-id="7ddeb-224">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7ddeb-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7ddeb-225">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7ddeb-226">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="7ddeb-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7ddeb-227">System-Only</span></span>            | <span data-ttu-id="7ddeb-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-228">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7ddeb-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7ddeb-230">True</span><span class="sxs-lookup"><span data-stu-id="7ddeb-230">True</span></span>                                                                |
| <span data-ttu-id="7ddeb-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7ddeb-231">Is Indexed</span></span>             | <span data-ttu-id="7ddeb-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-232">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7ddeb-233">In Global Catalog</span></span>      | <span data-ttu-id="7ddeb-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="7ddeb-234">False</span></span>                                                               |
| <span data-ttu-id="7ddeb-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7ddeb-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7ddeb-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7ddeb-236">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="7ddeb-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7ddeb-237">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7ddeb-238">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="7ddeb-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-239">Search-Flags</span></span>           | <span data-ttu-id="7ddeb-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7ddeb-240">0x00000000</span></span>                                                          |
| <span data-ttu-id="7ddeb-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7ddeb-241">System-Flags</span></span>           | <span data-ttu-id="7ddeb-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ddeb-242">0x00000010</span></span>                                                          |
| <span data-ttu-id="7ddeb-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7ddeb-243">Classes used in</span></span>        | [<span data-ttu-id="7ddeb-244">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="7ddeb-244">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





