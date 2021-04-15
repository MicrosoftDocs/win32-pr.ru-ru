---
title: Атрибут списка Global-Address-List
description: Этот атрибут используется в контейнере Microsoft Exchange для хранения различающегося имени только что созданного глобального списка адресов (GAL).
ms.assetid: 0da2bafe-ecdf-4b75-9461-08a35151b85c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута списка глобальных адресов
- Схема AD атрибута Глобаладдресслист
topic_type:
- apiref
api_name:
- Global-Address-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28178dfd6621593ee60e6e07043be544445cb6e7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654831"
---
# <a name="global-address-list-attribute"></a><span data-ttu-id="2885b-105">Атрибут списка Global-Address-List</span><span class="sxs-lookup"><span data-stu-id="2885b-105">Global-Address-List attribute</span></span>

<span data-ttu-id="2885b-106">Этот атрибут используется в контейнере Microsoft Exchange для хранения различающегося имени только что созданного глобального списка адресов (GAL).</span><span class="sxs-lookup"><span data-stu-id="2885b-106">This attribute is used on a Microsoft Exchange container to store the distinguished name of a newly created global address list (GAL).</span></span> <span data-ttu-id="2885b-107">Этот атрибут должен иметь запись, прежде чем можно будет включить клиентские интерфейсы MAPI для использования глобального списка адресов.</span><span class="sxs-lookup"><span data-stu-id="2885b-107">This attribute must have an entry before you can enable Messaging Application Programming Interface (MAPI) clients to use a GAL.</span></span>



| <span data-ttu-id="2885b-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="2885b-108">Entry</span></span> | <span data-ttu-id="2885b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="2885b-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2885b-110">CN</span><span class="sxs-lookup"><span data-stu-id="2885b-110">CN</span></span>                | <span data-ttu-id="2885b-111">Список Global-Address-List</span><span class="sxs-lookup"><span data-stu-id="2885b-111">Global-Address-List</span></span>                     |
| <span data-ttu-id="2885b-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2885b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="2885b-113">глобаладдресслист</span><span class="sxs-lookup"><span data-stu-id="2885b-113">globalAddressList</span></span>                       |
| <span data-ttu-id="2885b-114">Размер</span><span class="sxs-lookup"><span data-stu-id="2885b-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="2885b-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2885b-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="2885b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2885b-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2885b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2885b-117">Attribute-Id</span></span>      | <span data-ttu-id="2885b-118">1.2.840.113556.1.4.1245</span><span class="sxs-lookup"><span data-stu-id="2885b-118">1.2.840.113556.1.4.1245</span></span>                 |
| <span data-ttu-id="2885b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2885b-119">System-Id-Guid</span></span>    | <span data-ttu-id="2885b-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="2885b-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="2885b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2885b-121">Syntax</span></span>            | [<span data-ttu-id="2885b-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2885b-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2885b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2885b-123">Implementations</span></span>

-   [<span data-ttu-id="2885b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2885b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2885b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2885b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2885b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2885b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2885b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2885b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2885b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2885b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2885b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2885b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2885b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2885b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2885b-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="2885b-131">Entry</span></span> | <span data-ttu-id="2885b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2885b-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2885b-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2885b-133">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2885b-134">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2885b-135">System-Only</span></span>            | <span data-ttu-id="2885b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-136">False</span></span>                                                                                |
| <span data-ttu-id="2885b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2885b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2885b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-138">False</span></span>                                                                                |
| <span data-ttu-id="2885b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2885b-139">Is Indexed</span></span>             | <span data-ttu-id="2885b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-140">False</span></span>                                                                                |
| <span data-ttu-id="2885b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2885b-141">In Global Catalog</span></span>      | <span data-ttu-id="2885b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-142">False</span></span>                                                                                |
| <span data-ttu-id="2885b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2885b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2885b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2885b-144">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2885b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2885b-145">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2885b-146">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-147">Search-Flags</span></span>           | <span data-ttu-id="2885b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2885b-148">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2885b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-149">System-Flags</span></span>           | <span data-ttu-id="2885b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2885b-150">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2885b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2885b-151">Classes used in</span></span>        | [<span data-ttu-id="2885b-152">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2885b-152">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2885b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2885b-153">Windows Server 2003</span></span>



| <span data-ttu-id="2885b-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="2885b-154">Entry</span></span> | <span data-ttu-id="2885b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="2885b-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2885b-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2885b-156">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2885b-157">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2885b-158">System-Only</span></span>            | <span data-ttu-id="2885b-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-159">False</span></span>                                                                                |
| <span data-ttu-id="2885b-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2885b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2885b-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-161">False</span></span>                                                                                |
| <span data-ttu-id="2885b-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2885b-162">Is Indexed</span></span>             | <span data-ttu-id="2885b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-163">False</span></span>                                                                                |
| <span data-ttu-id="2885b-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2885b-164">In Global Catalog</span></span>      | <span data-ttu-id="2885b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-165">False</span></span>                                                                                |
| <span data-ttu-id="2885b-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2885b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2885b-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2885b-167">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2885b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2885b-168">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2885b-169">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-170">Search-Flags</span></span>           | <span data-ttu-id="2885b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2885b-171">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2885b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-172">System-Flags</span></span>           | <span data-ttu-id="2885b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2885b-173">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2885b-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2885b-174">Classes used in</span></span>        | [<span data-ttu-id="2885b-175">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2885b-175">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2885b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2885b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2885b-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="2885b-177">Entry</span></span> | <span data-ttu-id="2885b-178">Значение</span><span class="sxs-lookup"><span data-stu-id="2885b-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2885b-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2885b-179">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2885b-180">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2885b-181">System-Only</span></span>            | <span data-ttu-id="2885b-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-182">False</span></span>                                                                                |
| <span data-ttu-id="2885b-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2885b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2885b-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-184">False</span></span>                                                                                |
| <span data-ttu-id="2885b-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2885b-185">Is Indexed</span></span>             | <span data-ttu-id="2885b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-186">False</span></span>                                                                                |
| <span data-ttu-id="2885b-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2885b-187">In Global Catalog</span></span>      | <span data-ttu-id="2885b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-188">False</span></span>                                                                                |
| <span data-ttu-id="2885b-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2885b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2885b-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2885b-190">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2885b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2885b-191">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2885b-192">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-193">Search-Flags</span></span>           | <span data-ttu-id="2885b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2885b-194">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2885b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-195">System-Flags</span></span>           | <span data-ttu-id="2885b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2885b-196">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2885b-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2885b-197">Classes used in</span></span>        | [<span data-ttu-id="2885b-198">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2885b-198">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2885b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2885b-199">Windows Server 2008</span></span>



| <span data-ttu-id="2885b-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="2885b-200">Entry</span></span> | <span data-ttu-id="2885b-201">Значение</span><span class="sxs-lookup"><span data-stu-id="2885b-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2885b-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2885b-202">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2885b-203">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2885b-204">System-Only</span></span>            | <span data-ttu-id="2885b-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-205">False</span></span>                                                                                |
| <span data-ttu-id="2885b-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2885b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2885b-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-207">False</span></span>                                                                                |
| <span data-ttu-id="2885b-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2885b-208">Is Indexed</span></span>             | <span data-ttu-id="2885b-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-209">False</span></span>                                                                                |
| <span data-ttu-id="2885b-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2885b-210">In Global Catalog</span></span>      | <span data-ttu-id="2885b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-211">False</span></span>                                                                                |
| <span data-ttu-id="2885b-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2885b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2885b-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2885b-213">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2885b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2885b-214">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2885b-215">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-216">Search-Flags</span></span>           | <span data-ttu-id="2885b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2885b-217">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2885b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-218">System-Flags</span></span>           | <span data-ttu-id="2885b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2885b-219">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2885b-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2885b-220">Classes used in</span></span>        | [<span data-ttu-id="2885b-221">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2885b-221">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2885b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2885b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2885b-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="2885b-223">Entry</span></span> | <span data-ttu-id="2885b-224">Значение</span><span class="sxs-lookup"><span data-stu-id="2885b-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2885b-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2885b-225">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2885b-226">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2885b-227">System-Only</span></span>            | <span data-ttu-id="2885b-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-228">False</span></span>                                                                                |
| <span data-ttu-id="2885b-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2885b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2885b-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-230">False</span></span>                                                                                |
| <span data-ttu-id="2885b-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2885b-231">Is Indexed</span></span>             | <span data-ttu-id="2885b-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-232">False</span></span>                                                                                |
| <span data-ttu-id="2885b-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2885b-233">In Global Catalog</span></span>      | <span data-ttu-id="2885b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-234">False</span></span>                                                                                |
| <span data-ttu-id="2885b-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2885b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2885b-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2885b-236">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2885b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2885b-237">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2885b-238">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-239">Search-Flags</span></span>           | <span data-ttu-id="2885b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2885b-240">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2885b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-241">System-Flags</span></span>           | <span data-ttu-id="2885b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2885b-242">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2885b-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2885b-243">Classes used in</span></span>        | [<span data-ttu-id="2885b-244">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2885b-244">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2885b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2885b-245">Windows Server 2012</span></span>



| <span data-ttu-id="2885b-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="2885b-246">Entry</span></span> | <span data-ttu-id="2885b-247">Значение</span><span class="sxs-lookup"><span data-stu-id="2885b-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2885b-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2885b-248">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2885b-249">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="2885b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2885b-250">System-Only</span></span>            | <span data-ttu-id="2885b-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-251">False</span></span>                                                                                |
| <span data-ttu-id="2885b-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2885b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2885b-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-253">False</span></span>                                                                                |
| <span data-ttu-id="2885b-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2885b-254">Is Indexed</span></span>             | <span data-ttu-id="2885b-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-255">False</span></span>                                                                                |
| <span data-ttu-id="2885b-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2885b-256">In Global Catalog</span></span>      | <span data-ttu-id="2885b-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2885b-257">False</span></span>                                                                                |
| <span data-ttu-id="2885b-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2885b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2885b-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2885b-259">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="2885b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2885b-260">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2885b-261">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="2885b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-262">Search-Flags</span></span>           | <span data-ttu-id="2885b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2885b-263">0x00000000</span></span>                                                                           |
| <span data-ttu-id="2885b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2885b-264">System-Flags</span></span>           | <span data-ttu-id="2885b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2885b-265">0x00000010</span></span>                                                                           |
| <span data-ttu-id="2885b-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2885b-266">Classes used in</span></span>        | [<span data-ttu-id="2885b-267">**MS-дов-Configuration-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2885b-267">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





