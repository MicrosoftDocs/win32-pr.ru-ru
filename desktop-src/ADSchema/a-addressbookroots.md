---
title: Адресная книга-атрибут корней
description: Используется Exchange. Exchange настраивает деревья контейнеров адресной книги для отображения в адресной книге MAPI. Этот атрибут в объекте конфигурации Exchange содержит список корней деревьев контейнеров адресной книги. | Адресная книга-атрибут корней
ms.assetid: 7e6d2677-9818-4870-8429-50f73f9c8c1f
ms.tgt_platform: multiple
keywords:
- Адресная книга — схема AD атрибута корней
- Схема AD атрибута Аддрессбукрутс
topic_type:
- apiref
api_name:
- Address-Book-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab195744bb7fb5029a9a48aeca55d703e6e05b62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105656753"
---
# <a name="address-book-roots-attribute"></a><span data-ttu-id="4fcc1-108">Адресная книга-атрибут корней</span><span class="sxs-lookup"><span data-stu-id="4fcc1-108">Address-Book-Roots attribute</span></span>

<span data-ttu-id="4fcc1-109">Используется Exchange.</span><span class="sxs-lookup"><span data-stu-id="4fcc1-109">Used by Exchange.</span></span> <span data-ttu-id="4fcc1-110">Exchange настраивает деревья контейнеров адресной книги для отображения в адресной книге MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fcc1-110">Exchange configures trees of address book containers to show up in the MAPI address book.</span></span> <span data-ttu-id="4fcc1-111">Этот атрибут в объекте конфигурации Exchange содержит список корней деревьев контейнеров адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4fcc1-111">This attribute on the Exchange Config object lists the roots of the address book container trees.</span></span>



| <span data-ttu-id="4fcc1-112">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fcc1-112">Entry</span></span> | <span data-ttu-id="4fcc1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcc1-113">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="4fcc1-114">CN</span><span class="sxs-lookup"><span data-stu-id="4fcc1-114">CN</span></span>                | <span data-ttu-id="4fcc1-115">Адресная книга-корни</span><span class="sxs-lookup"><span data-stu-id="4fcc1-115">Address-Book-Roots</span></span>                      |
| <span data-ttu-id="4fcc1-116">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4fcc1-116">Ldap-Display-Name</span></span> | <span data-ttu-id="4fcc1-117">аддрессбукрутс</span><span class="sxs-lookup"><span data-stu-id="4fcc1-117">addressBookRoots</span></span>                        |
| <span data-ttu-id="4fcc1-118">Размер</span><span class="sxs-lookup"><span data-stu-id="4fcc1-118">Size</span></span>              | \-                                      |
| <span data-ttu-id="4fcc1-119">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4fcc1-119">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="4fcc1-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4fcc1-120">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="4fcc1-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4fcc1-121">Attribute-Id</span></span>      | <span data-ttu-id="4fcc1-122">1.2.840.113556.1.4.1244</span><span class="sxs-lookup"><span data-stu-id="4fcc1-122">1.2.840.113556.1.4.1244</span></span>                 |
| <span data-ttu-id="4fcc1-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4fcc1-123">System-Id-Guid</span></span>    | <span data-ttu-id="4fcc1-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="4fcc1-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="4fcc1-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fcc1-125">Syntax</span></span>            | [<span data-ttu-id="4fcc1-126">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-126">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="4fcc1-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4fcc1-127">Implementations</span></span>

-   [<span data-ttu-id="4fcc1-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4fcc1-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4fcc1-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4fcc1-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4fcc1-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4fcc1-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4fcc1-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4fcc1-134">Windows 2000 Server</span></span>



| <span data-ttu-id="4fcc1-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fcc1-135">Entry</span></span> | <span data-ttu-id="4fcc1-136">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcc1-136">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcc1-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fcc1-137">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fcc1-138">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fcc1-139">System-Only</span></span>            | <span data-ttu-id="4fcc1-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-140">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fcc1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="4fcc1-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-142">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fcc1-143">Is Indexed</span></span>             | <span data-ttu-id="4fcc1-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-144">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fcc1-145">In Global Catalog</span></span>      | <span data-ttu-id="4fcc1-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-146">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fcc1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fcc1-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fcc1-148">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="4fcc1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fcc1-149">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fcc1-150">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-151">Search-Flags</span></span>           | <span data-ttu-id="4fcc1-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fcc1-152">0x00000000</span></span>                                                                           |
| <span data-ttu-id="4fcc1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-153">System-Flags</span></span>           | <span data-ttu-id="4fcc1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fcc1-154">0x00000010</span></span>                                                                           |
| <span data-ttu-id="4fcc1-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fcc1-155">Classes used in</span></span>        | [<span data-ttu-id="4fcc1-156">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-156">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4fcc1-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4fcc1-157">Windows Server 2003</span></span>



| <span data-ttu-id="4fcc1-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fcc1-158">Entry</span></span> | <span data-ttu-id="4fcc1-159">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcc1-159">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcc1-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fcc1-160">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fcc1-161">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fcc1-162">System-Only</span></span>            | <span data-ttu-id="4fcc1-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-163">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fcc1-164">Is-Single-Valued</span></span>       | <span data-ttu-id="4fcc1-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-165">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fcc1-166">Is Indexed</span></span>             | <span data-ttu-id="4fcc1-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-167">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fcc1-168">In Global Catalog</span></span>      | <span data-ttu-id="4fcc1-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-169">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fcc1-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fcc1-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fcc1-171">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="4fcc1-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fcc1-172">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fcc1-173">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-174">Search-Flags</span></span>           | <span data-ttu-id="4fcc1-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fcc1-175">0x00000000</span></span>                                                                           |
| <span data-ttu-id="4fcc1-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-176">System-Flags</span></span>           | <span data-ttu-id="4fcc1-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fcc1-177">0x00000010</span></span>                                                                           |
| <span data-ttu-id="4fcc1-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fcc1-178">Classes used in</span></span>        | [<span data-ttu-id="4fcc1-179">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-179">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4fcc1-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4fcc1-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4fcc1-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fcc1-181">Entry</span></span> | <span data-ttu-id="4fcc1-182">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcc1-182">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcc1-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fcc1-183">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fcc1-184">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fcc1-185">System-Only</span></span>            | <span data-ttu-id="4fcc1-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-186">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fcc1-187">Is-Single-Valued</span></span>       | <span data-ttu-id="4fcc1-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-188">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fcc1-189">Is Indexed</span></span>             | <span data-ttu-id="4fcc1-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-190">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fcc1-191">In Global Catalog</span></span>      | <span data-ttu-id="4fcc1-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-192">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fcc1-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fcc1-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fcc1-194">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="4fcc1-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fcc1-195">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fcc1-196">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-197">Search-Flags</span></span>           | <span data-ttu-id="4fcc1-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fcc1-198">0x00000000</span></span>                                                                           |
| <span data-ttu-id="4fcc1-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-199">System-Flags</span></span>           | <span data-ttu-id="4fcc1-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fcc1-200">0x00000010</span></span>                                                                           |
| <span data-ttu-id="4fcc1-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fcc1-201">Classes used in</span></span>        | [<span data-ttu-id="4fcc1-202">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-202">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4fcc1-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fcc1-203">Windows Server 2008</span></span>



| <span data-ttu-id="4fcc1-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fcc1-204">Entry</span></span> | <span data-ttu-id="4fcc1-205">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcc1-205">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcc1-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fcc1-206">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fcc1-207">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fcc1-208">System-Only</span></span>            | <span data-ttu-id="4fcc1-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-209">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fcc1-210">Is-Single-Valued</span></span>       | <span data-ttu-id="4fcc1-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-211">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fcc1-212">Is Indexed</span></span>             | <span data-ttu-id="4fcc1-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-213">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fcc1-214">In Global Catalog</span></span>      | <span data-ttu-id="4fcc1-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-215">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fcc1-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fcc1-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fcc1-217">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="4fcc1-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fcc1-218">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fcc1-219">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-220">Search-Flags</span></span>           | <span data-ttu-id="4fcc1-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fcc1-221">0x00000000</span></span>                                                                           |
| <span data-ttu-id="4fcc1-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-222">System-Flags</span></span>           | <span data-ttu-id="4fcc1-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fcc1-223">0x00000010</span></span>                                                                           |
| <span data-ttu-id="4fcc1-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fcc1-224">Classes used in</span></span>        | [<span data-ttu-id="4fcc1-225">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-225">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4fcc1-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4fcc1-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4fcc1-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fcc1-227">Entry</span></span> | <span data-ttu-id="4fcc1-228">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcc1-228">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcc1-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fcc1-229">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fcc1-230">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fcc1-231">System-Only</span></span>            | <span data-ttu-id="4fcc1-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-232">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fcc1-233">Is-Single-Valued</span></span>       | <span data-ttu-id="4fcc1-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-234">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fcc1-235">Is Indexed</span></span>             | <span data-ttu-id="4fcc1-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-236">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fcc1-237">In Global Catalog</span></span>      | <span data-ttu-id="4fcc1-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-238">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fcc1-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fcc1-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fcc1-240">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="4fcc1-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fcc1-241">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fcc1-242">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-243">Search-Flags</span></span>           | <span data-ttu-id="4fcc1-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fcc1-244">0x00000000</span></span>                                                                           |
| <span data-ttu-id="4fcc1-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-245">System-Flags</span></span>           | <span data-ttu-id="4fcc1-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fcc1-246">0x00000010</span></span>                                                                           |
| <span data-ttu-id="4fcc1-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fcc1-247">Classes used in</span></span>        | [<span data-ttu-id="4fcc1-248">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-248">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4fcc1-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4fcc1-249">Windows Server 2012</span></span>



| <span data-ttu-id="4fcc1-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fcc1-250">Entry</span></span> | <span data-ttu-id="4fcc1-251">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcc1-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcc1-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fcc1-252">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fcc1-253">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="4fcc1-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fcc1-254">System-Only</span></span>            | <span data-ttu-id="4fcc1-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-255">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fcc1-256">Is-Single-Valued</span></span>       | <span data-ttu-id="4fcc1-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-257">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fcc1-258">Is Indexed</span></span>             | <span data-ttu-id="4fcc1-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-259">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fcc1-260">In Global Catalog</span></span>      | <span data-ttu-id="4fcc1-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fcc1-261">False</span></span>                                                                                |
| <span data-ttu-id="4fcc1-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fcc1-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fcc1-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fcc1-263">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="4fcc1-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fcc1-264">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fcc1-265">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="4fcc1-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-266">Search-Flags</span></span>           | <span data-ttu-id="4fcc1-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fcc1-267">0x00000000</span></span>                                                                           |
| <span data-ttu-id="4fcc1-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fcc1-268">System-Flags</span></span>           | <span data-ttu-id="4fcc1-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fcc1-269">0x00000010</span></span>                                                                           |
| <span data-ttu-id="4fcc1-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fcc1-270">Classes used in</span></span>        | [<span data-ttu-id="4fcc1-271">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="4fcc1-271">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





