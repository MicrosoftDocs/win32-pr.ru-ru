---
title: Атрибут "предыдущий — родительский ЦС"
description: Ссылка на центры сертификации, которые выдавали последний сертификат с истекшим сроком действия для центра сертификации.
ms.assetid: 9772d6cb-1105-426c-9982-473b4c1bf0d8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов предыдущего и родительского ЦС
- Схема AD атрибута Превиауспарентка
topic_type:
- apiref
api_name:
- Previous-Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a4c89652ef7ffffdc731614cfc57572b3edcde
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104072050"
---
# <a name="previous-parent-ca-attribute"></a><span data-ttu-id="c63ce-105">Атрибут "предыдущий — родительский ЦС"</span><span class="sxs-lookup"><span data-stu-id="c63ce-105">Previous-Parent-CA attribute</span></span>

<span data-ttu-id="c63ce-106">Ссылка на центры сертификации, которые выдавали последний сертификат с истекшим сроком действия для центра сертификации.</span><span class="sxs-lookup"><span data-stu-id="c63ce-106">Reference to the certification authorities that issued the last expired certificate for a certification authority.</span></span>



| <span data-ttu-id="c63ce-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c63ce-107">Entry</span></span> | <span data-ttu-id="c63ce-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c63ce-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c63ce-109">CN</span><span class="sxs-lookup"><span data-stu-id="c63ce-109">CN</span></span>                | <span data-ttu-id="c63ce-110">Предыдущий-родительский ЦС</span><span class="sxs-lookup"><span data-stu-id="c63ce-110">Previous-Parent-CA</span></span>                      |
| <span data-ttu-id="c63ce-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c63ce-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c63ce-112">превиауспарентка</span><span class="sxs-lookup"><span data-stu-id="c63ce-112">previousParentCA</span></span>                        |
| <span data-ttu-id="c63ce-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c63ce-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c63ce-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c63ce-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c63ce-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c63ce-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c63ce-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c63ce-116">Attribute-Id</span></span>      | <span data-ttu-id="c63ce-117">1.2.840.113556.1.4.694</span><span class="sxs-lookup"><span data-stu-id="c63ce-117">1.2.840.113556.1.4.694</span></span>                  |
| <span data-ttu-id="c63ce-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c63ce-118">System-Id-Guid</span></span>    | <span data-ttu-id="c63ce-119">963d273d-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c63ce-119">963d273d-48be-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="c63ce-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c63ce-120">Syntax</span></span>            | [<span data-ttu-id="c63ce-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c63ce-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c63ce-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c63ce-122">Implementations</span></span>

-   [<span data-ttu-id="c63ce-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c63ce-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c63ce-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c63ce-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c63ce-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c63ce-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c63ce-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c63ce-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c63ce-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c63ce-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c63ce-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c63ce-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c63ce-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c63ce-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c63ce-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="c63ce-130">Entry</span></span> | <span data-ttu-id="c63ce-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c63ce-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c63ce-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c63ce-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63ce-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63ce-134">System-Only</span></span>            | <span data-ttu-id="c63ce-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-135">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c63ce-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c63ce-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-137">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c63ce-138">Is Indexed</span></span>             | <span data-ttu-id="c63ce-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-139">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c63ce-140">In Global Catalog</span></span>      | <span data-ttu-id="c63ce-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-141">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c63ce-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63ce-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c63ce-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c63ce-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63ce-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63ce-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-146">Search-Flags</span></span>           | <span data-ttu-id="c63ce-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63ce-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="c63ce-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-148">System-Flags</span></span>           | <span data-ttu-id="c63ce-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63ce-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="c63ce-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c63ce-150">Classes used in</span></span>        | [<span data-ttu-id="c63ce-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="c63ce-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c63ce-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c63ce-152">Windows Server 2003</span></span>



| <span data-ttu-id="c63ce-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="c63ce-153">Entry</span></span> | <span data-ttu-id="c63ce-154">Значение</span><span class="sxs-lookup"><span data-stu-id="c63ce-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c63ce-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c63ce-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63ce-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63ce-157">System-Only</span></span>            | <span data-ttu-id="c63ce-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-158">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c63ce-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c63ce-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-160">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c63ce-161">Is Indexed</span></span>             | <span data-ttu-id="c63ce-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-162">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c63ce-163">In Global Catalog</span></span>      | <span data-ttu-id="c63ce-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-164">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c63ce-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63ce-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c63ce-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c63ce-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63ce-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63ce-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-169">Search-Flags</span></span>           | <span data-ttu-id="c63ce-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63ce-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="c63ce-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-171">System-Flags</span></span>           | <span data-ttu-id="c63ce-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63ce-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="c63ce-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c63ce-173">Classes used in</span></span>        | [<span data-ttu-id="c63ce-174">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="c63ce-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c63ce-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c63ce-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c63ce-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="c63ce-176">Entry</span></span> | <span data-ttu-id="c63ce-177">Значение</span><span class="sxs-lookup"><span data-stu-id="c63ce-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c63ce-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c63ce-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63ce-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63ce-180">System-Only</span></span>            | <span data-ttu-id="c63ce-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-181">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c63ce-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c63ce-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-183">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c63ce-184">Is Indexed</span></span>             | <span data-ttu-id="c63ce-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-185">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c63ce-186">In Global Catalog</span></span>      | <span data-ttu-id="c63ce-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-187">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c63ce-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63ce-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c63ce-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c63ce-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63ce-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63ce-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-192">Search-Flags</span></span>           | <span data-ttu-id="c63ce-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63ce-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="c63ce-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-194">System-Flags</span></span>           | <span data-ttu-id="c63ce-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63ce-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="c63ce-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c63ce-196">Classes used in</span></span>        | [<span data-ttu-id="c63ce-197">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="c63ce-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c63ce-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c63ce-198">Windows Server 2008</span></span>



| <span data-ttu-id="c63ce-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="c63ce-199">Entry</span></span> | <span data-ttu-id="c63ce-200">Значение</span><span class="sxs-lookup"><span data-stu-id="c63ce-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c63ce-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c63ce-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63ce-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63ce-203">System-Only</span></span>            | <span data-ttu-id="c63ce-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-204">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c63ce-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c63ce-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-206">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c63ce-207">Is Indexed</span></span>             | <span data-ttu-id="c63ce-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-208">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c63ce-209">In Global Catalog</span></span>      | <span data-ttu-id="c63ce-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-210">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c63ce-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63ce-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c63ce-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c63ce-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63ce-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63ce-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-215">Search-Flags</span></span>           | <span data-ttu-id="c63ce-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63ce-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="c63ce-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-217">System-Flags</span></span>           | <span data-ttu-id="c63ce-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63ce-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="c63ce-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c63ce-219">Classes used in</span></span>        | [<span data-ttu-id="c63ce-220">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="c63ce-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c63ce-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c63ce-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c63ce-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="c63ce-222">Entry</span></span> | <span data-ttu-id="c63ce-223">Значение</span><span class="sxs-lookup"><span data-stu-id="c63ce-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c63ce-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c63ce-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63ce-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63ce-226">System-Only</span></span>            | <span data-ttu-id="c63ce-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-227">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c63ce-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c63ce-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-229">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c63ce-230">Is Indexed</span></span>             | <span data-ttu-id="c63ce-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-231">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c63ce-232">In Global Catalog</span></span>      | <span data-ttu-id="c63ce-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-233">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c63ce-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63ce-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c63ce-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c63ce-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63ce-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63ce-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-238">Search-Flags</span></span>           | <span data-ttu-id="c63ce-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63ce-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="c63ce-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-240">System-Flags</span></span>           | <span data-ttu-id="c63ce-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63ce-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="c63ce-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c63ce-242">Classes used in</span></span>        | [<span data-ttu-id="c63ce-243">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="c63ce-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c63ce-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c63ce-244">Windows Server 2012</span></span>



| <span data-ttu-id="c63ce-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="c63ce-245">Entry</span></span> | <span data-ttu-id="c63ce-246">Значение</span><span class="sxs-lookup"><span data-stu-id="c63ce-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="c63ce-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c63ce-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c63ce-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="c63ce-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c63ce-249">System-Only</span></span>            | <span data-ttu-id="c63ce-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-250">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c63ce-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c63ce-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-252">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c63ce-253">Is Indexed</span></span>             | <span data-ttu-id="c63ce-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-254">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c63ce-255">In Global Catalog</span></span>      | <span data-ttu-id="c63ce-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="c63ce-256">False</span></span>                                                                  |
| <span data-ttu-id="c63ce-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c63ce-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c63ce-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c63ce-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="c63ce-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c63ce-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c63ce-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="c63ce-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-261">Search-Flags</span></span>           | <span data-ttu-id="c63ce-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c63ce-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="c63ce-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c63ce-263">System-Flags</span></span>           | <span data-ttu-id="c63ce-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c63ce-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="c63ce-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c63ce-265">Classes used in</span></span>        | [<span data-ttu-id="c63ce-266">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="c63ce-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





