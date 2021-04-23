---
title: Атрибут ms-DS-AZ-Application-Name
description: Строка, однозначно идентифицирующая объект приложения.
ms.assetid: 693a47f4-d3ae-4fae-8e5e-cbce41d00d45
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-AZ-Application-Name
- Схема AD атрибута msDS-Азаппликатионнаме
topic_type:
- apiref
api_name:
- ms-DS-Az-Application-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24166af15a250ec284eeb600b81bb8bb7d264369
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655460"
---
# <a name="ms-ds-az-application-name-attribute"></a><span data-ttu-id="b2db2-105">Атрибут ms-DS-AZ-Application-Name</span><span class="sxs-lookup"><span data-stu-id="b2db2-105">ms-DS-Az-Application-Name attribute</span></span>

<span data-ttu-id="b2db2-106">Строка, однозначно идентифицирующая объект приложения.</span><span class="sxs-lookup"><span data-stu-id="b2db2-106">A string that uniquely identifies an application object.</span></span>



| <span data-ttu-id="b2db2-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2db2-107">Entry</span></span> | <span data-ttu-id="b2db2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b2db2-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b2db2-109">CN</span><span class="sxs-lookup"><span data-stu-id="b2db2-109">CN</span></span>                | <span data-ttu-id="b2db2-110">MS-DS-AZ-имя приложения</span><span class="sxs-lookup"><span data-stu-id="b2db2-110">ms-DS-Az-Application-Name</span></span>                   |
| <span data-ttu-id="b2db2-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b2db2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b2db2-112">msDS-Азаппликатионнаме</span><span class="sxs-lookup"><span data-stu-id="b2db2-112">msDS-AzApplicationName</span></span>                      |
| <span data-ttu-id="b2db2-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b2db2-113">Size</span></span>              | <span data-ttu-id="b2db2-114">128 символов</span><span class="sxs-lookup"><span data-stu-id="b2db2-114">128 characters</span></span>                              |
| <span data-ttu-id="b2db2-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b2db2-115">Update Privilege</span></span>  | <span data-ttu-id="b2db2-116">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="b2db2-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="b2db2-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b2db2-117">Update Frequency</span></span>  | <span data-ttu-id="b2db2-118">Во время инициализации или изменения политики.</span><span class="sxs-lookup"><span data-stu-id="b2db2-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="b2db2-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b2db2-119">Attribute-Id</span></span>      | <span data-ttu-id="b2db2-120">1.2.840.113556.1.4.1798</span><span class="sxs-lookup"><span data-stu-id="b2db2-120">1.2.840.113556.1.4.1798</span></span>                     |
| <span data-ttu-id="b2db2-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b2db2-121">System-Id-Guid</span></span>    | <span data-ttu-id="b2db2-122">db5b0728-6208-4876-83b7-95d3e5695275</span><span class="sxs-lookup"><span data-stu-id="b2db2-122">db5b0728-6208-4876-83b7-95d3e5695275</span></span>        |
| <span data-ttu-id="b2db2-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2db2-123">Syntax</span></span>            | [<span data-ttu-id="b2db2-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="b2db2-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b2db2-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b2db2-125">Implementations</span></span>

-   [<span data-ttu-id="b2db2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b2db2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b2db2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b2db2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b2db2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b2db2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b2db2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b2db2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b2db2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b2db2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b2db2-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2db2-131">Windows Server 2003</span></span>



| <span data-ttu-id="b2db2-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2db2-132">Entry</span></span> | <span data-ttu-id="b2db2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b2db2-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b2db2-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2db2-134">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2db2-135">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2db2-136">System-Only</span></span>            | <span data-ttu-id="b2db2-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-137">False</span></span>                                                           |
| <span data-ttu-id="b2db2-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2db2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b2db2-139">True</span><span class="sxs-lookup"><span data-stu-id="b2db2-139">True</span></span>                                                            |
| <span data-ttu-id="b2db2-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2db2-140">Is Indexed</span></span>             | <span data-ttu-id="b2db2-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-141">False</span></span>                                                           |
| <span data-ttu-id="b2db2-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2db2-142">In Global Catalog</span></span>      | <span data-ttu-id="b2db2-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-143">False</span></span>                                                           |
| <span data-ttu-id="b2db2-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2db2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2db2-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2db2-145">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b2db2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2db2-146">Range-Lower</span></span>            | <span data-ttu-id="b2db2-147">0</span><span class="sxs-lookup"><span data-stu-id="b2db2-147">0</span></span>                                                               |
| <span data-ttu-id="b2db2-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2db2-148">Range-Upper</span></span>            | <span data-ttu-id="b2db2-149">512</span><span class="sxs-lookup"><span data-stu-id="b2db2-149">512</span></span>                                                             |
| <span data-ttu-id="b2db2-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-150">Search-Flags</span></span>           | <span data-ttu-id="b2db2-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2db2-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="b2db2-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-152">System-Flags</span></span>           | <span data-ttu-id="b2db2-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2db2-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="b2db2-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2db2-154">Classes used in</span></span>        | [<span data-ttu-id="b2db2-155">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="b2db2-155">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b2db2-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b2db2-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b2db2-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2db2-157">Entry</span></span> | <span data-ttu-id="b2db2-158">Значение</span><span class="sxs-lookup"><span data-stu-id="b2db2-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b2db2-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2db2-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2db2-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2db2-161">System-Only</span></span>            | <span data-ttu-id="b2db2-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-162">False</span></span>                                                           |
| <span data-ttu-id="b2db2-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2db2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b2db2-164">True</span><span class="sxs-lookup"><span data-stu-id="b2db2-164">True</span></span>                                                            |
| <span data-ttu-id="b2db2-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2db2-165">Is Indexed</span></span>             | <span data-ttu-id="b2db2-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-166">False</span></span>                                                           |
| <span data-ttu-id="b2db2-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2db2-167">In Global Catalog</span></span>      | <span data-ttu-id="b2db2-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-168">False</span></span>                                                           |
| <span data-ttu-id="b2db2-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2db2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2db2-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2db2-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b2db2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2db2-171">Range-Lower</span></span>            | <span data-ttu-id="b2db2-172">0</span><span class="sxs-lookup"><span data-stu-id="b2db2-172">0</span></span>                                                               |
| <span data-ttu-id="b2db2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2db2-173">Range-Upper</span></span>            | <span data-ttu-id="b2db2-174">512</span><span class="sxs-lookup"><span data-stu-id="b2db2-174">512</span></span>                                                             |
| <span data-ttu-id="b2db2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-175">Search-Flags</span></span>           | <span data-ttu-id="b2db2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2db2-176">0x00000000</span></span>                                                      |
| <span data-ttu-id="b2db2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-177">System-Flags</span></span>           | <span data-ttu-id="b2db2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2db2-178">0x00000010</span></span>                                                      |
| <span data-ttu-id="b2db2-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2db2-179">Classes used in</span></span>        | [<span data-ttu-id="b2db2-180">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="b2db2-180">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b2db2-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2db2-181">Windows Server 2008</span></span>



| <span data-ttu-id="b2db2-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2db2-182">Entry</span></span> | <span data-ttu-id="b2db2-183">Значение</span><span class="sxs-lookup"><span data-stu-id="b2db2-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b2db2-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2db2-184">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2db2-185">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2db2-186">System-Only</span></span>            | <span data-ttu-id="b2db2-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-187">False</span></span>                                                           |
| <span data-ttu-id="b2db2-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2db2-188">Is-Single-Valued</span></span>       | <span data-ttu-id="b2db2-189">True</span><span class="sxs-lookup"><span data-stu-id="b2db2-189">True</span></span>                                                            |
| <span data-ttu-id="b2db2-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2db2-190">Is Indexed</span></span>             | <span data-ttu-id="b2db2-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-191">False</span></span>                                                           |
| <span data-ttu-id="b2db2-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2db2-192">In Global Catalog</span></span>      | <span data-ttu-id="b2db2-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-193">False</span></span>                                                           |
| <span data-ttu-id="b2db2-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2db2-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2db2-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2db2-195">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b2db2-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2db2-196">Range-Lower</span></span>            | <span data-ttu-id="b2db2-197">0</span><span class="sxs-lookup"><span data-stu-id="b2db2-197">0</span></span>                                                               |
| <span data-ttu-id="b2db2-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2db2-198">Range-Upper</span></span>            | <span data-ttu-id="b2db2-199">512</span><span class="sxs-lookup"><span data-stu-id="b2db2-199">512</span></span>                                                             |
| <span data-ttu-id="b2db2-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-200">Search-Flags</span></span>           | <span data-ttu-id="b2db2-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2db2-201">0x00000000</span></span>                                                      |
| <span data-ttu-id="b2db2-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-202">System-Flags</span></span>           | <span data-ttu-id="b2db2-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2db2-203">0x00000010</span></span>                                                      |
| <span data-ttu-id="b2db2-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2db2-204">Classes used in</span></span>        | [<span data-ttu-id="b2db2-205">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="b2db2-205">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b2db2-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2db2-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b2db2-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2db2-207">Entry</span></span> | <span data-ttu-id="b2db2-208">Значение</span><span class="sxs-lookup"><span data-stu-id="b2db2-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b2db2-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2db2-209">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2db2-210">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2db2-211">System-Only</span></span>            | <span data-ttu-id="b2db2-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-212">False</span></span>                                                           |
| <span data-ttu-id="b2db2-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2db2-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b2db2-214">True</span><span class="sxs-lookup"><span data-stu-id="b2db2-214">True</span></span>                                                            |
| <span data-ttu-id="b2db2-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2db2-215">Is Indexed</span></span>             | <span data-ttu-id="b2db2-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-216">False</span></span>                                                           |
| <span data-ttu-id="b2db2-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2db2-217">In Global Catalog</span></span>      | <span data-ttu-id="b2db2-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-218">False</span></span>                                                           |
| <span data-ttu-id="b2db2-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2db2-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2db2-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2db2-220">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b2db2-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2db2-221">Range-Lower</span></span>            | <span data-ttu-id="b2db2-222">0</span><span class="sxs-lookup"><span data-stu-id="b2db2-222">0</span></span>                                                               |
| <span data-ttu-id="b2db2-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2db2-223">Range-Upper</span></span>            | <span data-ttu-id="b2db2-224">512</span><span class="sxs-lookup"><span data-stu-id="b2db2-224">512</span></span>                                                             |
| <span data-ttu-id="b2db2-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-225">Search-Flags</span></span>           | <span data-ttu-id="b2db2-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2db2-226">0x00000000</span></span>                                                      |
| <span data-ttu-id="b2db2-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-227">System-Flags</span></span>           | <span data-ttu-id="b2db2-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2db2-228">0x00000010</span></span>                                                      |
| <span data-ttu-id="b2db2-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2db2-229">Classes used in</span></span>        | [<span data-ttu-id="b2db2-230">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="b2db2-230">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b2db2-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2db2-231">Windows Server 2012</span></span>



| <span data-ttu-id="b2db2-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="b2db2-232">Entry</span></span> | <span data-ttu-id="b2db2-233">Значение</span><span class="sxs-lookup"><span data-stu-id="b2db2-233">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b2db2-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b2db2-234">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b2db2-235">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="b2db2-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="b2db2-236">System-Only</span></span>            | <span data-ttu-id="b2db2-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-237">False</span></span>                                                           |
| <span data-ttu-id="b2db2-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b2db2-238">Is-Single-Valued</span></span>       | <span data-ttu-id="b2db2-239">True</span><span class="sxs-lookup"><span data-stu-id="b2db2-239">True</span></span>                                                            |
| <span data-ttu-id="b2db2-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b2db2-240">Is Indexed</span></span>             | <span data-ttu-id="b2db2-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-241">False</span></span>                                                           |
| <span data-ttu-id="b2db2-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b2db2-242">In Global Catalog</span></span>      | <span data-ttu-id="b2db2-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="b2db2-243">False</span></span>                                                           |
| <span data-ttu-id="b2db2-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b2db2-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="b2db2-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b2db2-245">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="b2db2-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b2db2-246">Range-Lower</span></span>            | <span data-ttu-id="b2db2-247">0</span><span class="sxs-lookup"><span data-stu-id="b2db2-247">0</span></span>                                                               |
| <span data-ttu-id="b2db2-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b2db2-248">Range-Upper</span></span>            | <span data-ttu-id="b2db2-249">512</span><span class="sxs-lookup"><span data-stu-id="b2db2-249">512</span></span>                                                             |
| <span data-ttu-id="b2db2-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-250">Search-Flags</span></span>           | <span data-ttu-id="b2db2-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b2db2-251">0x00000000</span></span>                                                      |
| <span data-ttu-id="b2db2-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b2db2-252">System-Flags</span></span>           | <span data-ttu-id="b2db2-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b2db2-253">0x00000010</span></span>                                                      |
| <span data-ttu-id="b2db2-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b2db2-254">Classes used in</span></span>        | [<span data-ttu-id="b2db2-255">**MS-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="b2db2-255">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





