---
title: Атрибут ms-DS-Упдатескрипт
description: Он используется для хранения скрипта с инструкциями по реструктуризации домена.
ms.assetid: a9dd205d-f6c3-4eeb-95dc-491bfe30ab8b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-Упдатескрипт
- Схема AD атрибута msDS-Упдатескрипт
topic_type:
- apiref
api_name:
- ms-DS-UpdateScript
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7809bf6fdbaabb38976068d1998cacfb12bdaf3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655415"
---
# <a name="ms-ds-updatescript-attribute"></a><span data-ttu-id="c130c-105">Атрибут ms-DS-Упдатескрипт</span><span class="sxs-lookup"><span data-stu-id="c130c-105">ms-DS-UpdateScript attribute</span></span>

<span data-ttu-id="c130c-106">Он используется для хранения скрипта с инструкциями по реструктуризации домена.</span><span class="sxs-lookup"><span data-stu-id="c130c-106">This is used to hold the script with the domain restructure instructions.</span></span>



| <span data-ttu-id="c130c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c130c-107">Entry</span></span> | <span data-ttu-id="c130c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c130c-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c130c-109">CN</span><span class="sxs-lookup"><span data-stu-id="c130c-109">CN</span></span>                | <span data-ttu-id="c130c-110">MS-DS-Упдатескрипт</span><span class="sxs-lookup"><span data-stu-id="c130c-110">ms-DS-UpdateScript</span></span>                          |
| <span data-ttu-id="c130c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c130c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c130c-112">msDS-Упдатескрипт</span><span class="sxs-lookup"><span data-stu-id="c130c-112">msDS-UpdateScript</span></span>                           |
| <span data-ttu-id="c130c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c130c-113">Size</span></span>              | <span data-ttu-id="c130c-114">Максимальный размер в 10 000 байт.</span><span class="sxs-lookup"><span data-stu-id="c130c-114">Maximum size 10K bytes.</span></span>                     |
| <span data-ttu-id="c130c-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c130c-115">Update Privilege</span></span>  | <span data-ttu-id="c130c-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="c130c-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="c130c-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c130c-117">Update Frequency</span></span>  | <span data-ttu-id="c130c-118">Только во время реструктуризации домена.</span><span class="sxs-lookup"><span data-stu-id="c130c-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="c130c-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c130c-119">Attribute-Id</span></span>      | <span data-ttu-id="c130c-120">1.2.840.113556.1.4.1721</span><span class="sxs-lookup"><span data-stu-id="c130c-120">1.2.840.113556.1.4.1721</span></span>                     |
| <span data-ttu-id="c130c-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c130c-121">System-Id-Guid</span></span>    | <span data-ttu-id="c130c-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span><span class="sxs-lookup"><span data-stu-id="c130c-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span></span>        |
| <span data-ttu-id="c130c-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c130c-123">Syntax</span></span>            | [<span data-ttu-id="c130c-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="c130c-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c130c-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c130c-125">Implementations</span></span>

-   [<span data-ttu-id="c130c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c130c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c130c-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c130c-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c130c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c130c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c130c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c130c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c130c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c130c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c130c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c130c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c130c-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c130c-132">Windows Server 2003</span></span>



| <span data-ttu-id="c130c-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="c130c-133">Entry</span></span> | <span data-ttu-id="c130c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="c130c-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c130c-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c130c-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c130c-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c130c-137">System-Only</span></span>            | <span data-ttu-id="c130c-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-138">False</span></span>                                                         |
| <span data-ttu-id="c130c-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c130c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c130c-140">True</span><span class="sxs-lookup"><span data-stu-id="c130c-140">True</span></span>                                                          |
| <span data-ttu-id="c130c-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c130c-141">Is Indexed</span></span>             | <span data-ttu-id="c130c-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-142">False</span></span>                                                         |
| <span data-ttu-id="c130c-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c130c-143">In Global Catalog</span></span>      | <span data-ttu-id="c130c-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-144">False</span></span>                                                         |
| <span data-ttu-id="c130c-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c130c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c130c-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c130c-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c130c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c130c-147">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c130c-148">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-149">Search-Flags</span></span>           | <span data-ttu-id="c130c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c130c-150">0x00000000</span></span>                                                    |
| <span data-ttu-id="c130c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-151">System-Flags</span></span>           | <span data-ttu-id="c130c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c130c-152">0x00000010</span></span>                                                    |
| <span data-ttu-id="c130c-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c130c-153">Classes used in</span></span>        | [<span data-ttu-id="c130c-154">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c130c-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c130c-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="c130c-155">ADAM</span></span>



| <span data-ttu-id="c130c-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="c130c-156">Entry</span></span> | <span data-ttu-id="c130c-157">Значение</span><span class="sxs-lookup"><span data-stu-id="c130c-157">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c130c-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c130c-158">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c130c-159">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c130c-160">System-Only</span></span>            | <span data-ttu-id="c130c-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-161">False</span></span>                                                         |
| <span data-ttu-id="c130c-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c130c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c130c-163">True</span><span class="sxs-lookup"><span data-stu-id="c130c-163">True</span></span>                                                          |
| <span data-ttu-id="c130c-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c130c-164">Is Indexed</span></span>             | <span data-ttu-id="c130c-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-165">False</span></span>                                                         |
| <span data-ttu-id="c130c-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c130c-166">In Global Catalog</span></span>      | <span data-ttu-id="c130c-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-167">False</span></span>                                                         |
| <span data-ttu-id="c130c-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c130c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c130c-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c130c-169">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c130c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c130c-170">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c130c-171">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-172">Search-Flags</span></span>           | <span data-ttu-id="c130c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c130c-173">0x00000000</span></span>                                                    |
| <span data-ttu-id="c130c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-174">System-Flags</span></span>           | <span data-ttu-id="c130c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c130c-175">0x00000010</span></span>                                                    |
| <span data-ttu-id="c130c-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c130c-176">Classes used in</span></span>        | [<span data-ttu-id="c130c-177">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c130c-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c130c-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c130c-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c130c-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="c130c-179">Entry</span></span> | <span data-ttu-id="c130c-180">Значение</span><span class="sxs-lookup"><span data-stu-id="c130c-180">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c130c-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c130c-181">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c130c-182">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c130c-183">System-Only</span></span>            | <span data-ttu-id="c130c-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-184">False</span></span>                                                         |
| <span data-ttu-id="c130c-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c130c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c130c-186">True</span><span class="sxs-lookup"><span data-stu-id="c130c-186">True</span></span>                                                          |
| <span data-ttu-id="c130c-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c130c-187">Is Indexed</span></span>             | <span data-ttu-id="c130c-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-188">False</span></span>                                                         |
| <span data-ttu-id="c130c-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c130c-189">In Global Catalog</span></span>      | <span data-ttu-id="c130c-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-190">False</span></span>                                                         |
| <span data-ttu-id="c130c-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c130c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c130c-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c130c-192">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c130c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c130c-193">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c130c-194">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-195">Search-Flags</span></span>           | <span data-ttu-id="c130c-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c130c-196">0x00000000</span></span>                                                    |
| <span data-ttu-id="c130c-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-197">System-Flags</span></span>           | <span data-ttu-id="c130c-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c130c-198">0x00000010</span></span>                                                    |
| <span data-ttu-id="c130c-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c130c-199">Classes used in</span></span>        | [<span data-ttu-id="c130c-200">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c130c-200">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c130c-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c130c-201">Windows Server 2008</span></span>



| <span data-ttu-id="c130c-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="c130c-202">Entry</span></span> | <span data-ttu-id="c130c-203">Значение</span><span class="sxs-lookup"><span data-stu-id="c130c-203">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c130c-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c130c-204">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c130c-205">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c130c-206">System-Only</span></span>            | <span data-ttu-id="c130c-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-207">False</span></span>                                                         |
| <span data-ttu-id="c130c-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c130c-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c130c-209">True</span><span class="sxs-lookup"><span data-stu-id="c130c-209">True</span></span>                                                          |
| <span data-ttu-id="c130c-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c130c-210">Is Indexed</span></span>             | <span data-ttu-id="c130c-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-211">False</span></span>                                                         |
| <span data-ttu-id="c130c-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c130c-212">In Global Catalog</span></span>      | <span data-ttu-id="c130c-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-213">False</span></span>                                                         |
| <span data-ttu-id="c130c-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c130c-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c130c-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c130c-215">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c130c-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c130c-216">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c130c-217">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-218">Search-Flags</span></span>           | <span data-ttu-id="c130c-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c130c-219">0x00000000</span></span>                                                    |
| <span data-ttu-id="c130c-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-220">System-Flags</span></span>           | <span data-ttu-id="c130c-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c130c-221">0x00000010</span></span>                                                    |
| <span data-ttu-id="c130c-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c130c-222">Classes used in</span></span>        | [<span data-ttu-id="c130c-223">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c130c-223">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c130c-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c130c-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c130c-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="c130c-225">Entry</span></span> | <span data-ttu-id="c130c-226">Значение</span><span class="sxs-lookup"><span data-stu-id="c130c-226">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c130c-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c130c-227">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c130c-228">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="c130c-229">System-Only</span></span>            | <span data-ttu-id="c130c-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-230">False</span></span>                                                         |
| <span data-ttu-id="c130c-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c130c-231">Is-Single-Valued</span></span>       | <span data-ttu-id="c130c-232">True</span><span class="sxs-lookup"><span data-stu-id="c130c-232">True</span></span>                                                          |
| <span data-ttu-id="c130c-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c130c-233">Is Indexed</span></span>             | <span data-ttu-id="c130c-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-234">False</span></span>                                                         |
| <span data-ttu-id="c130c-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c130c-235">In Global Catalog</span></span>      | <span data-ttu-id="c130c-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-236">False</span></span>                                                         |
| <span data-ttu-id="c130c-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c130c-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="c130c-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c130c-238">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c130c-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c130c-239">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c130c-240">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-241">Search-Flags</span></span>           | <span data-ttu-id="c130c-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c130c-242">0x00000000</span></span>                                                    |
| <span data-ttu-id="c130c-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-243">System-Flags</span></span>           | <span data-ttu-id="c130c-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c130c-244">0x00000010</span></span>                                                    |
| <span data-ttu-id="c130c-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c130c-245">Classes used in</span></span>        | [<span data-ttu-id="c130c-246">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c130c-246">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c130c-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c130c-247">Windows Server 2012</span></span>



| <span data-ttu-id="c130c-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="c130c-248">Entry</span></span> | <span data-ttu-id="c130c-249">Значение</span><span class="sxs-lookup"><span data-stu-id="c130c-249">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c130c-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c130c-250">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c130c-251">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="c130c-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="c130c-252">System-Only</span></span>            | <span data-ttu-id="c130c-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-253">False</span></span>                                                         |
| <span data-ttu-id="c130c-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c130c-254">Is-Single-Valued</span></span>       | <span data-ttu-id="c130c-255">True</span><span class="sxs-lookup"><span data-stu-id="c130c-255">True</span></span>                                                          |
| <span data-ttu-id="c130c-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c130c-256">Is Indexed</span></span>             | <span data-ttu-id="c130c-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-257">False</span></span>                                                         |
| <span data-ttu-id="c130c-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c130c-258">In Global Catalog</span></span>      | <span data-ttu-id="c130c-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="c130c-259">False</span></span>                                                         |
| <span data-ttu-id="c130c-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c130c-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="c130c-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c130c-261">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="c130c-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c130c-262">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c130c-263">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="c130c-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-264">Search-Flags</span></span>           | <span data-ttu-id="c130c-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c130c-265">0x00000000</span></span>                                                    |
| <span data-ttu-id="c130c-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c130c-266">System-Flags</span></span>           | <span data-ttu-id="c130c-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c130c-267">0x00000010</span></span>                                                    |
| <span data-ttu-id="c130c-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c130c-268">Classes used in</span></span>        | [<span data-ttu-id="c130c-269">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c130c-269">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





