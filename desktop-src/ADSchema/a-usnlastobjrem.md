---
title: Атрибут USN-Last-obj-REM
description: Содержит порядковый номер обновления (USN) для последнего несистемного объекта, который был удален с сервера.
ms.assetid: 34718bea-fa19-4084-b97f-d72a1681c3f4
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "USN-Last-obj-REM"
- Схема AD атрибута Уснластобжрем
topic_type:
- apiref
api_name:
- USN-Last-Obj-Rem
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9836bd93ca065fdfa53b0246a5bab0142e84ced6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536110"
---
# <a name="usn-last-obj-rem-attribute"></a><span data-ttu-id="7a9d1-105">Атрибут USN-Last-obj-REM</span><span class="sxs-lookup"><span data-stu-id="7a9d1-105">USN-Last-Obj-Rem attribute</span></span>

<span data-ttu-id="7a9d1-106">Содержит порядковый номер обновления (USN) для последнего несистемного объекта, который был удален с сервера.</span><span class="sxs-lookup"><span data-stu-id="7a9d1-106">Contains the update sequence number (USN) for the last non-system object that was removed from a server.</span></span>



| <span data-ttu-id="7a9d1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a9d1-107">Entry</span></span> | <span data-ttu-id="7a9d1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7a9d1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7a9d1-109">CN</span><span class="sxs-lookup"><span data-stu-id="7a9d1-109">CN</span></span>                | <span data-ttu-id="7a9d1-110">USN-Last-obj-REM</span><span class="sxs-lookup"><span data-stu-id="7a9d1-110">USN-Last-Obj-Rem</span></span>                     |
| <span data-ttu-id="7a9d1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7a9d1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7a9d1-112">уснластобжрем</span><span class="sxs-lookup"><span data-stu-id="7a9d1-112">uSNLastObjRem</span></span>                        |
| <span data-ttu-id="7a9d1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7a9d1-113">Size</span></span>              | <span data-ttu-id="7a9d1-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="7a9d1-114">8 bytes</span></span>                              |
| <span data-ttu-id="7a9d1-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7a9d1-115">Update Privilege</span></span>  | <span data-ttu-id="7a9d1-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="7a9d1-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="7a9d1-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7a9d1-117">Update Frequency</span></span>  | <span data-ttu-id="7a9d1-118">При каждом изменении объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="7a9d1-118">Whenever a directory object changes.</span></span> |
| <span data-ttu-id="7a9d1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7a9d1-119">Attribute-Id</span></span>      | <span data-ttu-id="7a9d1-120">1.2.840.113556.1.2.121</span><span class="sxs-lookup"><span data-stu-id="7a9d1-120">1.2.840.113556.1.2.121</span></span>               |
| <span data-ttu-id="7a9d1-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7a9d1-121">System-Id-Guid</span></span>    | <span data-ttu-id="7a9d1-122">bf967a73-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7a9d1-122">bf967a73-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="7a9d1-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a9d1-123">Syntax</span></span>            | [<span data-ttu-id="7a9d1-124">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-124">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="7a9d1-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7a9d1-125">Implementations</span></span>

-   [<span data-ttu-id="7a9d1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7a9d1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7a9d1-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7a9d1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7a9d1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7a9d1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7a9d1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7a9d1-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a9d1-133">Windows 2000 Server</span></span>



| <span data-ttu-id="7a9d1-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a9d1-134">Entry</span></span> | <span data-ttu-id="7a9d1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7a9d1-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7a9d1-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a9d1-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7a9d1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9d1-137">MAPI-Id</span></span>                | <span data-ttu-id="7a9d1-138">0x8156</span><span class="sxs-lookup"><span data-stu-id="7a9d1-138">0x8156</span></span>                          |
| <span data-ttu-id="7a9d1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9d1-139">System-Only</span></span>            | <span data-ttu-id="7a9d1-140">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-140">True</span></span>                            |
| <span data-ttu-id="7a9d1-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a9d1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9d1-142">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-142">True</span></span>                            |
| <span data-ttu-id="7a9d1-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a9d1-143">Is Indexed</span></span>             | <span data-ttu-id="7a9d1-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a9d1-144">False</span></span>                           |
| <span data-ttu-id="7a9d1-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a9d1-145">In Global Catalog</span></span>      | <span data-ttu-id="7a9d1-146">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-146">True</span></span>                            |
| <span data-ttu-id="7a9d1-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a9d1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9d1-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a9d1-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7a9d1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9d1-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9d1-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-151">Search-Flags</span></span>           | <span data-ttu-id="7a9d1-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9d1-152">0x00000000</span></span>                      |
| <span data-ttu-id="7a9d1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-153">System-Flags</span></span>           | <span data-ttu-id="7a9d1-154">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7a9d1-154">0x00000013</span></span>                      |
| <span data-ttu-id="7a9d1-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a9d1-155">Classes used in</span></span>        | [<span data-ttu-id="7a9d1-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7a9d1-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a9d1-157">Windows Server 2003</span></span>



| <span data-ttu-id="7a9d1-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a9d1-158">Entry</span></span> | <span data-ttu-id="7a9d1-159">Значение</span><span class="sxs-lookup"><span data-stu-id="7a9d1-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7a9d1-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a9d1-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7a9d1-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9d1-161">MAPI-Id</span></span>                | <span data-ttu-id="7a9d1-162">0x8156</span><span class="sxs-lookup"><span data-stu-id="7a9d1-162">0x8156</span></span>                          |
| <span data-ttu-id="7a9d1-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9d1-163">System-Only</span></span>            | <span data-ttu-id="7a9d1-164">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-164">True</span></span>                            |
| <span data-ttu-id="7a9d1-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a9d1-165">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9d1-166">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-166">True</span></span>                            |
| <span data-ttu-id="7a9d1-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a9d1-167">Is Indexed</span></span>             | <span data-ttu-id="7a9d1-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a9d1-168">False</span></span>                           |
| <span data-ttu-id="7a9d1-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a9d1-169">In Global Catalog</span></span>      | <span data-ttu-id="7a9d1-170">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-170">True</span></span>                            |
| <span data-ttu-id="7a9d1-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a9d1-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9d1-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a9d1-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7a9d1-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9d1-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9d1-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-175">Search-Flags</span></span>           | <span data-ttu-id="7a9d1-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9d1-176">0x00000000</span></span>                      |
| <span data-ttu-id="7a9d1-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-177">System-Flags</span></span>           | <span data-ttu-id="7a9d1-178">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7a9d1-178">0x00000013</span></span>                      |
| <span data-ttu-id="7a9d1-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a9d1-179">Classes used in</span></span>        | [<span data-ttu-id="7a9d1-180">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7a9d1-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="7a9d1-181">ADAM</span></span>



| <span data-ttu-id="7a9d1-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a9d1-182">Entry</span></span> | <span data-ttu-id="7a9d1-183">Значение</span><span class="sxs-lookup"><span data-stu-id="7a9d1-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7a9d1-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a9d1-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7a9d1-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9d1-185">MAPI-Id</span></span>                | <span data-ttu-id="7a9d1-186">0x8156</span><span class="sxs-lookup"><span data-stu-id="7a9d1-186">0x8156</span></span>                          |
| <span data-ttu-id="7a9d1-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9d1-187">System-Only</span></span>            | <span data-ttu-id="7a9d1-188">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-188">True</span></span>                            |
| <span data-ttu-id="7a9d1-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a9d1-189">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9d1-190">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-190">True</span></span>                            |
| <span data-ttu-id="7a9d1-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a9d1-191">Is Indexed</span></span>             | <span data-ttu-id="7a9d1-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a9d1-192">False</span></span>                           |
| <span data-ttu-id="7a9d1-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a9d1-193">In Global Catalog</span></span>      | <span data-ttu-id="7a9d1-194">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-194">True</span></span>                            |
| <span data-ttu-id="7a9d1-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a9d1-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9d1-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a9d1-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7a9d1-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9d1-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9d1-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-199">Search-Flags</span></span>           | <span data-ttu-id="7a9d1-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9d1-200">0x00000000</span></span>                      |
| <span data-ttu-id="7a9d1-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-201">System-Flags</span></span>           | <span data-ttu-id="7a9d1-202">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7a9d1-202">0x00000013</span></span>                      |
| <span data-ttu-id="7a9d1-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a9d1-203">Classes used in</span></span>        | [<span data-ttu-id="7a9d1-204">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7a9d1-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7a9d1-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7a9d1-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a9d1-206">Entry</span></span> | <span data-ttu-id="7a9d1-207">Значение</span><span class="sxs-lookup"><span data-stu-id="7a9d1-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7a9d1-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a9d1-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7a9d1-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9d1-209">MAPI-Id</span></span>                | <span data-ttu-id="7a9d1-210">0x8156</span><span class="sxs-lookup"><span data-stu-id="7a9d1-210">0x8156</span></span>                          |
| <span data-ttu-id="7a9d1-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9d1-211">System-Only</span></span>            | <span data-ttu-id="7a9d1-212">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-212">True</span></span>                            |
| <span data-ttu-id="7a9d1-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a9d1-213">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9d1-214">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-214">True</span></span>                            |
| <span data-ttu-id="7a9d1-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a9d1-215">Is Indexed</span></span>             | <span data-ttu-id="7a9d1-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a9d1-216">False</span></span>                           |
| <span data-ttu-id="7a9d1-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a9d1-217">In Global Catalog</span></span>      | <span data-ttu-id="7a9d1-218">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-218">True</span></span>                            |
| <span data-ttu-id="7a9d1-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a9d1-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9d1-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a9d1-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7a9d1-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9d1-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9d1-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-223">Search-Flags</span></span>           | <span data-ttu-id="7a9d1-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9d1-224">0x00000000</span></span>                      |
| <span data-ttu-id="7a9d1-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-225">System-Flags</span></span>           | <span data-ttu-id="7a9d1-226">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7a9d1-226">0x00000013</span></span>                      |
| <span data-ttu-id="7a9d1-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a9d1-227">Classes used in</span></span>        | [<span data-ttu-id="7a9d1-228">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7a9d1-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a9d1-229">Windows Server 2008</span></span>



| <span data-ttu-id="7a9d1-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a9d1-230">Entry</span></span> | <span data-ttu-id="7a9d1-231">Значение</span><span class="sxs-lookup"><span data-stu-id="7a9d1-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7a9d1-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a9d1-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7a9d1-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9d1-233">MAPI-Id</span></span>                | <span data-ttu-id="7a9d1-234">0x8156</span><span class="sxs-lookup"><span data-stu-id="7a9d1-234">0x8156</span></span>                          |
| <span data-ttu-id="7a9d1-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9d1-235">System-Only</span></span>            | <span data-ttu-id="7a9d1-236">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-236">True</span></span>                            |
| <span data-ttu-id="7a9d1-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a9d1-237">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9d1-238">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-238">True</span></span>                            |
| <span data-ttu-id="7a9d1-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a9d1-239">Is Indexed</span></span>             | <span data-ttu-id="7a9d1-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a9d1-240">False</span></span>                           |
| <span data-ttu-id="7a9d1-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a9d1-241">In Global Catalog</span></span>      | <span data-ttu-id="7a9d1-242">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-242">True</span></span>                            |
| <span data-ttu-id="7a9d1-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a9d1-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9d1-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a9d1-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7a9d1-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9d1-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9d1-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-247">Search-Flags</span></span>           | <span data-ttu-id="7a9d1-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9d1-248">0x00000000</span></span>                      |
| <span data-ttu-id="7a9d1-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-249">System-Flags</span></span>           | <span data-ttu-id="7a9d1-250">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7a9d1-250">0x00000013</span></span>                      |
| <span data-ttu-id="7a9d1-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a9d1-251">Classes used in</span></span>        | [<span data-ttu-id="7a9d1-252">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7a9d1-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a9d1-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7a9d1-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a9d1-254">Entry</span></span> | <span data-ttu-id="7a9d1-255">Значение</span><span class="sxs-lookup"><span data-stu-id="7a9d1-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7a9d1-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a9d1-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7a9d1-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9d1-257">MAPI-Id</span></span>                | <span data-ttu-id="7a9d1-258">0x8156</span><span class="sxs-lookup"><span data-stu-id="7a9d1-258">0x8156</span></span>                          |
| <span data-ttu-id="7a9d1-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9d1-259">System-Only</span></span>            | <span data-ttu-id="7a9d1-260">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-260">True</span></span>                            |
| <span data-ttu-id="7a9d1-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a9d1-261">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9d1-262">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-262">True</span></span>                            |
| <span data-ttu-id="7a9d1-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a9d1-263">Is Indexed</span></span>             | <span data-ttu-id="7a9d1-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a9d1-264">False</span></span>                           |
| <span data-ttu-id="7a9d1-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a9d1-265">In Global Catalog</span></span>      | <span data-ttu-id="7a9d1-266">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-266">True</span></span>                            |
| <span data-ttu-id="7a9d1-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a9d1-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9d1-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a9d1-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7a9d1-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9d1-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9d1-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-271">Search-Flags</span></span>           | <span data-ttu-id="7a9d1-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9d1-272">0x00000000</span></span>                      |
| <span data-ttu-id="7a9d1-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-273">System-Flags</span></span>           | <span data-ttu-id="7a9d1-274">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7a9d1-274">0x00000013</span></span>                      |
| <span data-ttu-id="7a9d1-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a9d1-275">Classes used in</span></span>        | [<span data-ttu-id="7a9d1-276">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7a9d1-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a9d1-277">Windows Server 2012</span></span>



| <span data-ttu-id="7a9d1-278">Ввод</span><span class="sxs-lookup"><span data-stu-id="7a9d1-278">Entry</span></span> | <span data-ttu-id="7a9d1-279">Значение</span><span class="sxs-lookup"><span data-stu-id="7a9d1-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7a9d1-280">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7a9d1-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7a9d1-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9d1-281">MAPI-Id</span></span>                | <span data-ttu-id="7a9d1-282">0x8156</span><span class="sxs-lookup"><span data-stu-id="7a9d1-282">0x8156</span></span>                          |
| <span data-ttu-id="7a9d1-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9d1-283">System-Only</span></span>            | <span data-ttu-id="7a9d1-284">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-284">True</span></span>                            |
| <span data-ttu-id="7a9d1-285">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7a9d1-285">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9d1-286">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-286">True</span></span>                            |
| <span data-ttu-id="7a9d1-287">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7a9d1-287">Is Indexed</span></span>             | <span data-ttu-id="7a9d1-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="7a9d1-288">False</span></span>                           |
| <span data-ttu-id="7a9d1-289">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7a9d1-289">In Global Catalog</span></span>      | <span data-ttu-id="7a9d1-290">True</span><span class="sxs-lookup"><span data-stu-id="7a9d1-290">True</span></span>                            |
| <span data-ttu-id="7a9d1-291">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7a9d1-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9d1-292">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7a9d1-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7a9d1-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9d1-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9d1-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7a9d1-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-295">Search-Flags</span></span>           | <span data-ttu-id="7a9d1-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9d1-296">0x00000000</span></span>                      |
| <span data-ttu-id="7a9d1-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9d1-297">System-Flags</span></span>           | <span data-ttu-id="7a9d1-298">0x00000013</span><span class="sxs-lookup"><span data-stu-id="7a9d1-298">0x00000013</span></span>                      |
| <span data-ttu-id="7a9d1-299">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7a9d1-299">Classes used in</span></span>        | [<span data-ttu-id="7a9d1-300">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-300">**Top**</span></span>](c-top.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="7a9d1-301">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a9d1-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a9d1-302">**USN-DSA-Last-obj-removed**</span><span class="sxs-lookup"><span data-stu-id="7a9d1-302">**USN-DSA-Last-Obj-Removed**</span></span>](a-usndsalastobjremoved.md)
</dt> </dl>

 

 





