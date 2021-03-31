---
title: Атрибут Template-Roots
description: Этот атрибут используется в контейнере конфигурации Exchange для указания места хранения контейнеров шаблонов. Эти сведения используются поставщиком Active Directory MAPI.
ms.assetid: 1416ce4a-ca07-4ca9-8ea1-e1a6ad19e7ad
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Template-Roots
- Схема AD атрибута Темплатерутс
topic_type:
- apiref
api_name:
- Template-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761c6d3d79bbf45e9a4d391b612956d6893cd314
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804823"
---
# <a name="template-roots-attribute"></a><span data-ttu-id="584ab-106">Атрибут Template-Roots</span><span class="sxs-lookup"><span data-stu-id="584ab-106">Template-Roots attribute</span></span>

<span data-ttu-id="584ab-107">Этот атрибут используется в контейнере конфигурации Exchange для указания места хранения контейнеров шаблонов.</span><span class="sxs-lookup"><span data-stu-id="584ab-107">This attribute is used on the Exchange config container to indicate where the template containers are stored.</span></span> <span data-ttu-id="584ab-108">Эти сведения используются поставщиком Active Directory MAPI.</span><span class="sxs-lookup"><span data-stu-id="584ab-108">This information is used by the Active Directory MAPI provider.</span></span>



| <span data-ttu-id="584ab-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="584ab-109">Entry</span></span> | <span data-ttu-id="584ab-110">Значение</span><span class="sxs-lookup"><span data-stu-id="584ab-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="584ab-111">CN</span><span class="sxs-lookup"><span data-stu-id="584ab-111">CN</span></span>                | <span data-ttu-id="584ab-112">Template-Roots</span><span class="sxs-lookup"><span data-stu-id="584ab-112">Template-Roots</span></span>                          |
| <span data-ttu-id="584ab-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="584ab-113">Ldap-Display-Name</span></span> | <span data-ttu-id="584ab-114">темплатерутс</span><span class="sxs-lookup"><span data-stu-id="584ab-114">templateRoots</span></span>                           |
| <span data-ttu-id="584ab-115">Размер</span><span class="sxs-lookup"><span data-stu-id="584ab-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="584ab-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="584ab-116">Update Privilege</span></span>  | <span data-ttu-id="584ab-117">Используется системой.</span><span class="sxs-lookup"><span data-stu-id="584ab-117">This is used by the system.</span></span>             |
| <span data-ttu-id="584ab-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="584ab-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="584ab-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="584ab-119">Attribute-Id</span></span>      | <span data-ttu-id="584ab-120">1.2.840.113556.1.4.1346</span><span class="sxs-lookup"><span data-stu-id="584ab-120">1.2.840.113556.1.4.1346</span></span>                 |
| <span data-ttu-id="584ab-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="584ab-121">System-Id-Guid</span></span>    | <span data-ttu-id="584ab-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="584ab-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span></span>    |
| <span data-ttu-id="584ab-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="584ab-123">Syntax</span></span>            | [<span data-ttu-id="584ab-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="584ab-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="584ab-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="584ab-125">Implementations</span></span>

-   [<span data-ttu-id="584ab-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="584ab-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="584ab-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="584ab-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="584ab-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="584ab-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="584ab-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="584ab-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="584ab-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="584ab-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="584ab-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="584ab-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="584ab-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="584ab-132">Windows 2000 Server</span></span>



| <span data-ttu-id="584ab-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="584ab-133">Entry</span></span> | <span data-ttu-id="584ab-134">Значение</span><span class="sxs-lookup"><span data-stu-id="584ab-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="584ab-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="584ab-135">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="584ab-136">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="584ab-137">System-Only</span></span>            | <span data-ttu-id="584ab-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-138">False</span></span>                                                                                |
| <span data-ttu-id="584ab-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="584ab-139">Is-Single-Valued</span></span>       | <span data-ttu-id="584ab-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-140">False</span></span>                                                                                |
| <span data-ttu-id="584ab-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="584ab-141">Is Indexed</span></span>             | <span data-ttu-id="584ab-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-142">False</span></span>                                                                                |
| <span data-ttu-id="584ab-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="584ab-143">In Global Catalog</span></span>      | <span data-ttu-id="584ab-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-144">False</span></span>                                                                                |
| <span data-ttu-id="584ab-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="584ab-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="584ab-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="584ab-146">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="584ab-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="584ab-147">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="584ab-148">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-149">Search-Flags</span></span>           | <span data-ttu-id="584ab-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="584ab-150">0x00000000</span></span>                                                                           |
| <span data-ttu-id="584ab-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-151">System-Flags</span></span>           | <span data-ttu-id="584ab-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="584ab-152">0x00000010</span></span>                                                                           |
| <span data-ttu-id="584ab-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="584ab-153">Classes used in</span></span>        | [<span data-ttu-id="584ab-154">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="584ab-154">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="584ab-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="584ab-155">Windows Server 2003</span></span>



| <span data-ttu-id="584ab-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="584ab-156">Entry</span></span> | <span data-ttu-id="584ab-157">Значение</span><span class="sxs-lookup"><span data-stu-id="584ab-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="584ab-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="584ab-158">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="584ab-159">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="584ab-160">System-Only</span></span>            | <span data-ttu-id="584ab-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-161">False</span></span>                                                                                |
| <span data-ttu-id="584ab-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="584ab-162">Is-Single-Valued</span></span>       | <span data-ttu-id="584ab-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-163">False</span></span>                                                                                |
| <span data-ttu-id="584ab-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="584ab-164">Is Indexed</span></span>             | <span data-ttu-id="584ab-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-165">False</span></span>                                                                                |
| <span data-ttu-id="584ab-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="584ab-166">In Global Catalog</span></span>      | <span data-ttu-id="584ab-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-167">False</span></span>                                                                                |
| <span data-ttu-id="584ab-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="584ab-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="584ab-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="584ab-169">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="584ab-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="584ab-170">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="584ab-171">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-172">Search-Flags</span></span>           | <span data-ttu-id="584ab-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="584ab-173">0x00000000</span></span>                                                                           |
| <span data-ttu-id="584ab-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-174">System-Flags</span></span>           | <span data-ttu-id="584ab-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="584ab-175">0x00000010</span></span>                                                                           |
| <span data-ttu-id="584ab-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="584ab-176">Classes used in</span></span>        | [<span data-ttu-id="584ab-177">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="584ab-177">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="584ab-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="584ab-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="584ab-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="584ab-179">Entry</span></span> | <span data-ttu-id="584ab-180">Значение</span><span class="sxs-lookup"><span data-stu-id="584ab-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="584ab-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="584ab-181">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="584ab-182">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="584ab-183">System-Only</span></span>            | <span data-ttu-id="584ab-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-184">False</span></span>                                                                                |
| <span data-ttu-id="584ab-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="584ab-185">Is-Single-Valued</span></span>       | <span data-ttu-id="584ab-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-186">False</span></span>                                                                                |
| <span data-ttu-id="584ab-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="584ab-187">Is Indexed</span></span>             | <span data-ttu-id="584ab-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-188">False</span></span>                                                                                |
| <span data-ttu-id="584ab-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="584ab-189">In Global Catalog</span></span>      | <span data-ttu-id="584ab-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-190">False</span></span>                                                                                |
| <span data-ttu-id="584ab-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="584ab-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="584ab-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="584ab-192">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="584ab-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="584ab-193">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="584ab-194">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-195">Search-Flags</span></span>           | <span data-ttu-id="584ab-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="584ab-196">0x00000000</span></span>                                                                           |
| <span data-ttu-id="584ab-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-197">System-Flags</span></span>           | <span data-ttu-id="584ab-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="584ab-198">0x00000010</span></span>                                                                           |
| <span data-ttu-id="584ab-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="584ab-199">Classes used in</span></span>        | [<span data-ttu-id="584ab-200">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="584ab-200">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="584ab-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="584ab-201">Windows Server 2008</span></span>



| <span data-ttu-id="584ab-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="584ab-202">Entry</span></span> | <span data-ttu-id="584ab-203">Значение</span><span class="sxs-lookup"><span data-stu-id="584ab-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="584ab-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="584ab-204">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="584ab-205">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="584ab-206">System-Only</span></span>            | <span data-ttu-id="584ab-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-207">False</span></span>                                                                                |
| <span data-ttu-id="584ab-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="584ab-208">Is-Single-Valued</span></span>       | <span data-ttu-id="584ab-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-209">False</span></span>                                                                                |
| <span data-ttu-id="584ab-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="584ab-210">Is Indexed</span></span>             | <span data-ttu-id="584ab-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-211">False</span></span>                                                                                |
| <span data-ttu-id="584ab-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="584ab-212">In Global Catalog</span></span>      | <span data-ttu-id="584ab-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-213">False</span></span>                                                                                |
| <span data-ttu-id="584ab-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="584ab-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="584ab-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="584ab-215">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="584ab-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="584ab-216">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="584ab-217">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-218">Search-Flags</span></span>           | <span data-ttu-id="584ab-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="584ab-219">0x00000000</span></span>                                                                           |
| <span data-ttu-id="584ab-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-220">System-Flags</span></span>           | <span data-ttu-id="584ab-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="584ab-221">0x00000010</span></span>                                                                           |
| <span data-ttu-id="584ab-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="584ab-222">Classes used in</span></span>        | [<span data-ttu-id="584ab-223">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="584ab-223">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="584ab-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="584ab-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="584ab-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="584ab-225">Entry</span></span> | <span data-ttu-id="584ab-226">Значение</span><span class="sxs-lookup"><span data-stu-id="584ab-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="584ab-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="584ab-227">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="584ab-228">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="584ab-229">System-Only</span></span>            | <span data-ttu-id="584ab-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-230">False</span></span>                                                                                |
| <span data-ttu-id="584ab-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="584ab-231">Is-Single-Valued</span></span>       | <span data-ttu-id="584ab-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-232">False</span></span>                                                                                |
| <span data-ttu-id="584ab-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="584ab-233">Is Indexed</span></span>             | <span data-ttu-id="584ab-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-234">False</span></span>                                                                                |
| <span data-ttu-id="584ab-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="584ab-235">In Global Catalog</span></span>      | <span data-ttu-id="584ab-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-236">False</span></span>                                                                                |
| <span data-ttu-id="584ab-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="584ab-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="584ab-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="584ab-238">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="584ab-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="584ab-239">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="584ab-240">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-241">Search-Flags</span></span>           | <span data-ttu-id="584ab-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="584ab-242">0x00000000</span></span>                                                                           |
| <span data-ttu-id="584ab-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-243">System-Flags</span></span>           | <span data-ttu-id="584ab-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="584ab-244">0x00000010</span></span>                                                                           |
| <span data-ttu-id="584ab-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="584ab-245">Classes used in</span></span>        | [<span data-ttu-id="584ab-246">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="584ab-246">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="584ab-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="584ab-247">Windows Server 2012</span></span>



| <span data-ttu-id="584ab-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="584ab-248">Entry</span></span> | <span data-ttu-id="584ab-249">Значение</span><span class="sxs-lookup"><span data-stu-id="584ab-249">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="584ab-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="584ab-250">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="584ab-251">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="584ab-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="584ab-252">System-Only</span></span>            | <span data-ttu-id="584ab-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-253">False</span></span>                                                                                |
| <span data-ttu-id="584ab-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="584ab-254">Is-Single-Valued</span></span>       | <span data-ttu-id="584ab-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-255">False</span></span>                                                                                |
| <span data-ttu-id="584ab-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="584ab-256">Is Indexed</span></span>             | <span data-ttu-id="584ab-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-257">False</span></span>                                                                                |
| <span data-ttu-id="584ab-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="584ab-258">In Global Catalog</span></span>      | <span data-ttu-id="584ab-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="584ab-259">False</span></span>                                                                                |
| <span data-ttu-id="584ab-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="584ab-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="584ab-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="584ab-261">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="584ab-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="584ab-262">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="584ab-263">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="584ab-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-264">Search-Flags</span></span>           | <span data-ttu-id="584ab-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="584ab-265">0x00000000</span></span>                                                                           |
| <span data-ttu-id="584ab-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="584ab-266">System-Flags</span></span>           | <span data-ttu-id="584ab-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="584ab-267">0x00000010</span></span>                                                                           |
| <span data-ttu-id="584ab-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="584ab-268">Classes used in</span></span>        | [<span data-ttu-id="584ab-269">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="584ab-269">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





