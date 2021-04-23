---
title: SD-Rights-действующий атрибут
description: Этот сконструированный атрибут возвращает одиночное значение DWORD, которое может иметь до трех бит Set OWNER \_ Security \_ информатиондакл \_ Security Информатионсакл Security \_ \_ \_ (если задан бит), то у пользователя есть доступ на запись к соответствующей части дескриптора безопасности. Владелец означает как владельца, так и группу.
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- SD-Rights — действующая схема Active Directory
- Схема AD атрибута Сдригхтсеффективе
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac449cd18b3fb75a61f04fffc266c290b7763295
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893286"
---
# <a name="sd-rights-effective-attribute"></a><span data-ttu-id="c42be-106">SD-Rights-действующий атрибут</span><span class="sxs-lookup"><span data-stu-id="c42be-106">SD-Rights-Effective attribute</span></span>

<span data-ttu-id="c42be-107">Этот сконструированный атрибут возвращает одиночное значение **DWORD** , которое может иметь до трех наборов битов:</span><span class="sxs-lookup"><span data-stu-id="c42be-107">This constructed attribute returns a single **DWORD** value that can have up to three bits set:</span></span>

-   <span data-ttu-id="c42be-108">\_ \_ сведения о безопасности владельца</span><span class="sxs-lookup"><span data-stu-id="c42be-108">OWNER\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="c42be-109">\_ \_ сведения о безопасности DACL</span><span class="sxs-lookup"><span data-stu-id="c42be-109">DACL\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="c42be-110">\_ \_ сведения о безопасности SACL</span><span class="sxs-lookup"><span data-stu-id="c42be-110">SACL\_SECURITY\_INFORMATION</span></span>

<span data-ttu-id="c42be-111">Если задан бит, то пользователь имеет доступ на запись к соответствующей части дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="c42be-111">If a bit is set, then the user has write access to the corresponding part of the security descriptor.</span></span> <span data-ttu-id="c42be-112">Владелец означает как владельца, так и группу.</span><span class="sxs-lookup"><span data-stu-id="c42be-112">Owner means both owner and group.</span></span>



| <span data-ttu-id="c42be-113">Ввод</span><span class="sxs-lookup"><span data-stu-id="c42be-113">Entry</span></span> | <span data-ttu-id="c42be-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c42be-114">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c42be-115">CN</span><span class="sxs-lookup"><span data-stu-id="c42be-115">CN</span></span>                | <span data-ttu-id="c42be-116">SD-Rights-эффективен</span><span class="sxs-lookup"><span data-stu-id="c42be-116">SD-Rights-Effective</span></span>                  |
| <span data-ttu-id="c42be-117">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c42be-117">Ldap-Display-Name</span></span> | <span data-ttu-id="c42be-118">сдригхтсеффективе</span><span class="sxs-lookup"><span data-stu-id="c42be-118">sDRightsEffective</span></span>                    |
| <span data-ttu-id="c42be-119">Размер</span><span class="sxs-lookup"><span data-stu-id="c42be-119">Size</span></span>              | \-                                   |
| <span data-ttu-id="c42be-120">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c42be-120">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c42be-121">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c42be-121">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c42be-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c42be-122">Attribute-Id</span></span>      | <span data-ttu-id="c42be-123">1.2.840.113556.1.4.1304</span><span class="sxs-lookup"><span data-stu-id="c42be-123">1.2.840.113556.1.4.1304</span></span>              |
| <span data-ttu-id="c42be-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c42be-124">System-Id-Guid</span></span>    | <span data-ttu-id="c42be-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c42be-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="c42be-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c42be-126">Syntax</span></span>            | [<span data-ttu-id="c42be-127">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="c42be-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c42be-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c42be-128">Implementations</span></span>

-   [<span data-ttu-id="c42be-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c42be-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c42be-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c42be-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c42be-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c42be-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c42be-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c42be-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c42be-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c42be-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c42be-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c42be-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c42be-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c42be-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c42be-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c42be-136">Windows 2000 Server</span></span>



| <span data-ttu-id="c42be-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="c42be-137">Entry</span></span> | <span data-ttu-id="c42be-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c42be-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c42be-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c42be-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c42be-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="c42be-141">System-Only</span></span>            | <span data-ttu-id="c42be-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-142">False</span></span>                           |
| <span data-ttu-id="c42be-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c42be-143">Is-Single-Valued</span></span>       | <span data-ttu-id="c42be-144">True</span><span class="sxs-lookup"><span data-stu-id="c42be-144">True</span></span>                            |
| <span data-ttu-id="c42be-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c42be-145">Is Indexed</span></span>             | <span data-ttu-id="c42be-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-146">False</span></span>                           |
| <span data-ttu-id="c42be-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c42be-147">In Global Catalog</span></span>      | <span data-ttu-id="c42be-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-148">False</span></span>                           |
| <span data-ttu-id="c42be-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c42be-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="c42be-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c42be-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c42be-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c42be-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c42be-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c42be-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c42be-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-153">Search-Flags</span></span>           | <span data-ttu-id="c42be-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c42be-154">0x00000000</span></span>                      |
| <span data-ttu-id="c42be-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-155">System-Flags</span></span>           | <span data-ttu-id="c42be-156">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c42be-156">0x08000014</span></span>                      |
| <span data-ttu-id="c42be-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c42be-157">Classes used in</span></span>        | [<span data-ttu-id="c42be-158">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c42be-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c42be-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c42be-159">Windows Server 2003</span></span>



| <span data-ttu-id="c42be-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="c42be-160">Entry</span></span> | <span data-ttu-id="c42be-161">Значение</span><span class="sxs-lookup"><span data-stu-id="c42be-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c42be-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c42be-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c42be-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c42be-164">System-Only</span></span>            | <span data-ttu-id="c42be-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-165">False</span></span>                           |
| <span data-ttu-id="c42be-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c42be-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c42be-167">True</span><span class="sxs-lookup"><span data-stu-id="c42be-167">True</span></span>                            |
| <span data-ttu-id="c42be-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c42be-168">Is Indexed</span></span>             | <span data-ttu-id="c42be-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-169">False</span></span>                           |
| <span data-ttu-id="c42be-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c42be-170">In Global Catalog</span></span>      | <span data-ttu-id="c42be-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-171">False</span></span>                           |
| <span data-ttu-id="c42be-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c42be-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c42be-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c42be-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c42be-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c42be-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c42be-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c42be-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c42be-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-176">Search-Flags</span></span>           | <span data-ttu-id="c42be-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c42be-177">0x00000000</span></span>                      |
| <span data-ttu-id="c42be-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-178">System-Flags</span></span>           | <span data-ttu-id="c42be-179">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c42be-179">0x08000014</span></span>                      |
| <span data-ttu-id="c42be-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c42be-180">Classes used in</span></span>        | [<span data-ttu-id="c42be-181">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c42be-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c42be-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="c42be-182">ADAM</span></span>



| <span data-ttu-id="c42be-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="c42be-183">Entry</span></span> | <span data-ttu-id="c42be-184">Значение</span><span class="sxs-lookup"><span data-stu-id="c42be-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c42be-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c42be-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c42be-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="c42be-187">System-Only</span></span>            | <span data-ttu-id="c42be-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-188">False</span></span>                           |
| <span data-ttu-id="c42be-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c42be-189">Is-Single-Valued</span></span>       | <span data-ttu-id="c42be-190">True</span><span class="sxs-lookup"><span data-stu-id="c42be-190">True</span></span>                            |
| <span data-ttu-id="c42be-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c42be-191">Is Indexed</span></span>             | <span data-ttu-id="c42be-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-192">False</span></span>                           |
| <span data-ttu-id="c42be-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c42be-193">In Global Catalog</span></span>      | <span data-ttu-id="c42be-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-194">False</span></span>                           |
| <span data-ttu-id="c42be-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c42be-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="c42be-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c42be-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c42be-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c42be-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c42be-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c42be-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c42be-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-199">Search-Flags</span></span>           | <span data-ttu-id="c42be-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c42be-200">0x00000000</span></span>                      |
| <span data-ttu-id="c42be-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-201">System-Flags</span></span>           | <span data-ttu-id="c42be-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c42be-202">0x08000014</span></span>                      |
| <span data-ttu-id="c42be-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c42be-203">Classes used in</span></span>        | [<span data-ttu-id="c42be-204">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c42be-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c42be-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c42be-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c42be-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="c42be-206">Entry</span></span> | <span data-ttu-id="c42be-207">Значение</span><span class="sxs-lookup"><span data-stu-id="c42be-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c42be-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c42be-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c42be-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c42be-210">System-Only</span></span>            | <span data-ttu-id="c42be-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-211">False</span></span>                           |
| <span data-ttu-id="c42be-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c42be-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c42be-213">True</span><span class="sxs-lookup"><span data-stu-id="c42be-213">True</span></span>                            |
| <span data-ttu-id="c42be-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c42be-214">Is Indexed</span></span>             | <span data-ttu-id="c42be-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-215">False</span></span>                           |
| <span data-ttu-id="c42be-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c42be-216">In Global Catalog</span></span>      | <span data-ttu-id="c42be-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-217">False</span></span>                           |
| <span data-ttu-id="c42be-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c42be-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c42be-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c42be-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c42be-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c42be-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c42be-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c42be-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c42be-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-222">Search-Flags</span></span>           | <span data-ttu-id="c42be-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c42be-223">0x00000000</span></span>                      |
| <span data-ttu-id="c42be-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-224">System-Flags</span></span>           | <span data-ttu-id="c42be-225">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c42be-225">0x08000014</span></span>                      |
| <span data-ttu-id="c42be-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c42be-226">Classes used in</span></span>        | [<span data-ttu-id="c42be-227">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c42be-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c42be-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c42be-228">Windows Server 2008</span></span>



| <span data-ttu-id="c42be-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="c42be-229">Entry</span></span> | <span data-ttu-id="c42be-230">Значение</span><span class="sxs-lookup"><span data-stu-id="c42be-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c42be-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c42be-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c42be-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="c42be-233">System-Only</span></span>            | <span data-ttu-id="c42be-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-234">False</span></span>                           |
| <span data-ttu-id="c42be-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c42be-235">Is-Single-Valued</span></span>       | <span data-ttu-id="c42be-236">True</span><span class="sxs-lookup"><span data-stu-id="c42be-236">True</span></span>                            |
| <span data-ttu-id="c42be-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c42be-237">Is Indexed</span></span>             | <span data-ttu-id="c42be-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-238">False</span></span>                           |
| <span data-ttu-id="c42be-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c42be-239">In Global Catalog</span></span>      | <span data-ttu-id="c42be-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-240">False</span></span>                           |
| <span data-ttu-id="c42be-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c42be-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="c42be-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c42be-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c42be-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c42be-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c42be-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c42be-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c42be-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-245">Search-Flags</span></span>           | <span data-ttu-id="c42be-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c42be-246">0x00000000</span></span>                      |
| <span data-ttu-id="c42be-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-247">System-Flags</span></span>           | <span data-ttu-id="c42be-248">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c42be-248">0x08000014</span></span>                      |
| <span data-ttu-id="c42be-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c42be-249">Classes used in</span></span>        | [<span data-ttu-id="c42be-250">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c42be-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c42be-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c42be-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c42be-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="c42be-252">Entry</span></span> | <span data-ttu-id="c42be-253">Значение</span><span class="sxs-lookup"><span data-stu-id="c42be-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c42be-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c42be-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c42be-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="c42be-256">System-Only</span></span>            | <span data-ttu-id="c42be-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-257">False</span></span>                           |
| <span data-ttu-id="c42be-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c42be-258">Is-Single-Valued</span></span>       | <span data-ttu-id="c42be-259">True</span><span class="sxs-lookup"><span data-stu-id="c42be-259">True</span></span>                            |
| <span data-ttu-id="c42be-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c42be-260">Is Indexed</span></span>             | <span data-ttu-id="c42be-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-261">False</span></span>                           |
| <span data-ttu-id="c42be-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c42be-262">In Global Catalog</span></span>      | <span data-ttu-id="c42be-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-263">False</span></span>                           |
| <span data-ttu-id="c42be-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c42be-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="c42be-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c42be-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c42be-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c42be-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c42be-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c42be-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c42be-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-268">Search-Flags</span></span>           | <span data-ttu-id="c42be-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c42be-269">0x00000000</span></span>                      |
| <span data-ttu-id="c42be-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-270">System-Flags</span></span>           | <span data-ttu-id="c42be-271">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c42be-271">0x08000014</span></span>                      |
| <span data-ttu-id="c42be-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c42be-272">Classes used in</span></span>        | [<span data-ttu-id="c42be-273">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c42be-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c42be-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c42be-274">Windows Server 2012</span></span>



| <span data-ttu-id="c42be-275">Ввод</span><span class="sxs-lookup"><span data-stu-id="c42be-275">Entry</span></span> | <span data-ttu-id="c42be-276">Значение</span><span class="sxs-lookup"><span data-stu-id="c42be-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c42be-277">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c42be-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c42be-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c42be-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="c42be-279">System-Only</span></span>            | <span data-ttu-id="c42be-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-280">False</span></span>                           |
| <span data-ttu-id="c42be-281">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c42be-281">Is-Single-Valued</span></span>       | <span data-ttu-id="c42be-282">True</span><span class="sxs-lookup"><span data-stu-id="c42be-282">True</span></span>                            |
| <span data-ttu-id="c42be-283">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c42be-283">Is Indexed</span></span>             | <span data-ttu-id="c42be-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-284">False</span></span>                           |
| <span data-ttu-id="c42be-285">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c42be-285">In Global Catalog</span></span>      | <span data-ttu-id="c42be-286">Неверно</span><span class="sxs-lookup"><span data-stu-id="c42be-286">False</span></span>                           |
| <span data-ttu-id="c42be-287">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c42be-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="c42be-288">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c42be-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c42be-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c42be-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c42be-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c42be-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c42be-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-291">Search-Flags</span></span>           | <span data-ttu-id="c42be-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c42be-292">0x00000000</span></span>                      |
| <span data-ttu-id="c42be-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c42be-293">System-Flags</span></span>           | <span data-ttu-id="c42be-294">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c42be-294">0x08000014</span></span>                      |
| <span data-ttu-id="c42be-295">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c42be-295">Classes used in</span></span>        | [<span data-ttu-id="c42be-296">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c42be-296">**Top**</span></span>](c-top.md)<br/> |



 

 





