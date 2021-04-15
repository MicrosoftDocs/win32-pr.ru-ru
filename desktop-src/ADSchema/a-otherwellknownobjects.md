---
title: Атрибут других известных объектов
description: Содержит список контейнеров по идентификатору GUID и различающееся имя. Это позволяет получить объект после перемещения с использованием только идентификатора GUID и имени домена. При перемещении объекта система автоматически обновляет различающееся имя.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- Схема AD других хорошо известных объектов
- Схема AD атрибута otherWellKnownObjects
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493953"
---
# <a name="other-well-known-objects-attribute"></a><span data-ttu-id="0d885-107">Атрибут других известных объектов</span><span class="sxs-lookup"><span data-stu-id="0d885-107">Other-Well-Known-Objects attribute</span></span>

<span data-ttu-id="0d885-108">Содержит список контейнеров по идентификатору GUID и различающееся имя.</span><span class="sxs-lookup"><span data-stu-id="0d885-108">Contains a list of containers by GUID and Distinguished Name.</span></span> <span data-ttu-id="0d885-109">Это позволяет получить объект после перемещения с использованием только идентификатора GUID и имени домена.</span><span class="sxs-lookup"><span data-stu-id="0d885-109">This permits retrieving an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="0d885-110">При перемещении объекта система автоматически обновляет различающееся имя.</span><span class="sxs-lookup"><span data-stu-id="0d885-110">Whenever the object is moved, the system automatically updates the Distinguished Name.</span></span>



| <span data-ttu-id="0d885-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d885-111">Entry</span></span> | <span data-ttu-id="0d885-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0d885-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d885-113">CN</span><span class="sxs-lookup"><span data-stu-id="0d885-113">CN</span></span>                | <span data-ttu-id="0d885-114">Другие хорошо известные объекты</span><span class="sxs-lookup"><span data-stu-id="0d885-114">Other-Well-Known-Objects</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="0d885-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0d885-115">Ldap-Display-Name</span></span> | <span data-ttu-id="0d885-116">otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="0d885-116">otherWellKnownObjects</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="0d885-117">Размер</span><span class="sxs-lookup"><span data-stu-id="0d885-117">Size</span></span>              | <span data-ttu-id="0d885-118">Пример получения контейнера "Пользователи" в домене Майкрософт: LDAP://(ВКГУИД = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com).</span><span class="sxs-lookup"><span data-stu-id="0d885-118">Sample for retrieving the Users container in the microsoft domain: LDAP://(WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=microsoft,dc=com).</span></span> <span data-ttu-id="0d885-119">Примечание. угловые скобки, которые заменяются круглыми скобками, чтобы избежать конфликтов XML.</span><span class="sxs-lookup"><span data-stu-id="0d885-119">NOTE: Angle brackets replaced by parentheses to avoid XML conflicts.</span></span> |
| <span data-ttu-id="0d885-120">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0d885-120">Update Privilege</span></span>  | <span data-ttu-id="0d885-121">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="0d885-121">Schema administrator</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="0d885-122">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0d885-122">Update Frequency</span></span>  | <span data-ttu-id="0d885-123">При перемещении объекта.</span><span class="sxs-lookup"><span data-stu-id="0d885-123">Whenever the object is moved.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="0d885-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0d885-124">Attribute-Id</span></span>      | <span data-ttu-id="0d885-125">1.2.840.113556.1.4.1359</span><span class="sxs-lookup"><span data-stu-id="0d885-125">1.2.840.113556.1.4.1359</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="0d885-126">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0d885-126">System-Id-Guid</span></span>    | <span data-ttu-id="0d885-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="0d885-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span></span>                                                                                                                                                                          |
| <span data-ttu-id="0d885-128">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d885-128">Syntax</span></span>            | [<span data-ttu-id="0d885-129">**Object(двоичный_DN)**</span><span class="sxs-lookup"><span data-stu-id="0d885-129">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                               |



## <a name="implementations"></a><span data-ttu-id="0d885-130">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0d885-130">Implementations</span></span>

-   [<span data-ttu-id="0d885-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0d885-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0d885-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0d885-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0d885-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="0d885-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="0d885-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0d885-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0d885-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0d885-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0d885-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0d885-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0d885-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0d885-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0d885-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0d885-138">Windows 2000 Server</span></span>



| <span data-ttu-id="0d885-139">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d885-139">Entry</span></span> | <span data-ttu-id="0d885-140">Значение</span><span class="sxs-lookup"><span data-stu-id="0d885-140">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d885-141">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d885-141">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d885-142">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d885-143">System-Only</span></span>            | <span data-ttu-id="0d885-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-144">False</span></span>                           |
| <span data-ttu-id="0d885-145">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d885-145">Is-Single-Valued</span></span>       | <span data-ttu-id="0d885-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-146">False</span></span>                           |
| <span data-ttu-id="0d885-147">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d885-147">Is Indexed</span></span>             | <span data-ttu-id="0d885-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-148">False</span></span>                           |
| <span data-ttu-id="0d885-149">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d885-149">In Global Catalog</span></span>      | <span data-ttu-id="0d885-150">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-150">False</span></span>                           |
| <span data-ttu-id="0d885-151">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d885-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d885-152">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d885-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d885-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d885-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="0d885-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d885-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="0d885-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-155">Search-Flags</span></span>           | <span data-ttu-id="0d885-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d885-156">0x00000000</span></span>                      |
| <span data-ttu-id="0d885-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-157">System-Flags</span></span>           | <span data-ttu-id="0d885-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d885-158">0x00000010</span></span>                      |
| <span data-ttu-id="0d885-159">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d885-159">Classes used in</span></span>        | [<span data-ttu-id="0d885-160">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="0d885-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0d885-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d885-161">Windows Server 2003</span></span>



| <span data-ttu-id="0d885-162">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d885-162">Entry</span></span> | <span data-ttu-id="0d885-163">Значение</span><span class="sxs-lookup"><span data-stu-id="0d885-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d885-164">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d885-164">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d885-165">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d885-166">System-Only</span></span>            | <span data-ttu-id="0d885-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-167">False</span></span>                           |
| <span data-ttu-id="0d885-168">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d885-168">Is-Single-Valued</span></span>       | <span data-ttu-id="0d885-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-169">False</span></span>                           |
| <span data-ttu-id="0d885-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d885-170">Is Indexed</span></span>             | <span data-ttu-id="0d885-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-171">False</span></span>                           |
| <span data-ttu-id="0d885-172">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d885-172">In Global Catalog</span></span>      | <span data-ttu-id="0d885-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-173">False</span></span>                           |
| <span data-ttu-id="0d885-174">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d885-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d885-175">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d885-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d885-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d885-176">Range-Lower</span></span>            | <span data-ttu-id="0d885-177">16</span><span class="sxs-lookup"><span data-stu-id="0d885-177">16</span></span>                              |
| <span data-ttu-id="0d885-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d885-178">Range-Upper</span></span>            | <span data-ttu-id="0d885-179">16</span><span class="sxs-lookup"><span data-stu-id="0d885-179">16</span></span>                              |
| <span data-ttu-id="0d885-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-180">Search-Flags</span></span>           | <span data-ttu-id="0d885-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d885-181">0x00000000</span></span>                      |
| <span data-ttu-id="0d885-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-182">System-Flags</span></span>           | <span data-ttu-id="0d885-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d885-183">0x00000010</span></span>                      |
| <span data-ttu-id="0d885-184">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d885-184">Classes used in</span></span>        | [<span data-ttu-id="0d885-185">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="0d885-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="0d885-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="0d885-186">ADAM</span></span>



| <span data-ttu-id="0d885-187">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d885-187">Entry</span></span> | <span data-ttu-id="0d885-188">Значение</span><span class="sxs-lookup"><span data-stu-id="0d885-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d885-189">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d885-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d885-190">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d885-191">System-Only</span></span>            | <span data-ttu-id="0d885-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-192">False</span></span>                           |
| <span data-ttu-id="0d885-193">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d885-193">Is-Single-Valued</span></span>       | <span data-ttu-id="0d885-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-194">False</span></span>                           |
| <span data-ttu-id="0d885-195">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d885-195">Is Indexed</span></span>             | <span data-ttu-id="0d885-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-196">False</span></span>                           |
| <span data-ttu-id="0d885-197">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d885-197">In Global Catalog</span></span>      | <span data-ttu-id="0d885-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-198">False</span></span>                           |
| <span data-ttu-id="0d885-199">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d885-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d885-200">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d885-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d885-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d885-201">Range-Lower</span></span>            | <span data-ttu-id="0d885-202">16</span><span class="sxs-lookup"><span data-stu-id="0d885-202">16</span></span>                              |
| <span data-ttu-id="0d885-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d885-203">Range-Upper</span></span>            | <span data-ttu-id="0d885-204">16</span><span class="sxs-lookup"><span data-stu-id="0d885-204">16</span></span>                              |
| <span data-ttu-id="0d885-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-205">Search-Flags</span></span>           | <span data-ttu-id="0d885-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d885-206">0x00000000</span></span>                      |
| <span data-ttu-id="0d885-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-207">System-Flags</span></span>           | <span data-ttu-id="0d885-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d885-208">0x00000010</span></span>                      |
| <span data-ttu-id="0d885-209">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d885-209">Classes used in</span></span>        | [<span data-ttu-id="0d885-210">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="0d885-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0d885-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0d885-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0d885-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d885-212">Entry</span></span> | <span data-ttu-id="0d885-213">Значение</span><span class="sxs-lookup"><span data-stu-id="0d885-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d885-214">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d885-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d885-215">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d885-216">System-Only</span></span>            | <span data-ttu-id="0d885-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-217">False</span></span>                           |
| <span data-ttu-id="0d885-218">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d885-218">Is-Single-Valued</span></span>       | <span data-ttu-id="0d885-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-219">False</span></span>                           |
| <span data-ttu-id="0d885-220">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d885-220">Is Indexed</span></span>             | <span data-ttu-id="0d885-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-221">False</span></span>                           |
| <span data-ttu-id="0d885-222">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d885-222">In Global Catalog</span></span>      | <span data-ttu-id="0d885-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-223">False</span></span>                           |
| <span data-ttu-id="0d885-224">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d885-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d885-225">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d885-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d885-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d885-226">Range-Lower</span></span>            | <span data-ttu-id="0d885-227">16</span><span class="sxs-lookup"><span data-stu-id="0d885-227">16</span></span>                              |
| <span data-ttu-id="0d885-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d885-228">Range-Upper</span></span>            | <span data-ttu-id="0d885-229">16</span><span class="sxs-lookup"><span data-stu-id="0d885-229">16</span></span>                              |
| <span data-ttu-id="0d885-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-230">Search-Flags</span></span>           | <span data-ttu-id="0d885-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d885-231">0x00000000</span></span>                      |
| <span data-ttu-id="0d885-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-232">System-Flags</span></span>           | <span data-ttu-id="0d885-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d885-233">0x00000010</span></span>                      |
| <span data-ttu-id="0d885-234">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d885-234">Classes used in</span></span>        | [<span data-ttu-id="0d885-235">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="0d885-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0d885-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d885-236">Windows Server 2008</span></span>



| <span data-ttu-id="0d885-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d885-237">Entry</span></span> | <span data-ttu-id="0d885-238">Значение</span><span class="sxs-lookup"><span data-stu-id="0d885-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d885-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d885-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d885-240">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d885-241">System-Only</span></span>            | <span data-ttu-id="0d885-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-242">False</span></span>                           |
| <span data-ttu-id="0d885-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d885-243">Is-Single-Valued</span></span>       | <span data-ttu-id="0d885-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-244">False</span></span>                           |
| <span data-ttu-id="0d885-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d885-245">Is Indexed</span></span>             | <span data-ttu-id="0d885-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-246">False</span></span>                           |
| <span data-ttu-id="0d885-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d885-247">In Global Catalog</span></span>      | <span data-ttu-id="0d885-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-248">False</span></span>                           |
| <span data-ttu-id="0d885-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d885-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d885-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d885-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d885-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d885-251">Range-Lower</span></span>            | <span data-ttu-id="0d885-252">16</span><span class="sxs-lookup"><span data-stu-id="0d885-252">16</span></span>                              |
| <span data-ttu-id="0d885-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d885-253">Range-Upper</span></span>            | <span data-ttu-id="0d885-254">16</span><span class="sxs-lookup"><span data-stu-id="0d885-254">16</span></span>                              |
| <span data-ttu-id="0d885-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-255">Search-Flags</span></span>           | <span data-ttu-id="0d885-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d885-256">0x00000000</span></span>                      |
| <span data-ttu-id="0d885-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-257">System-Flags</span></span>           | <span data-ttu-id="0d885-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d885-258">0x00000010</span></span>                      |
| <span data-ttu-id="0d885-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d885-259">Classes used in</span></span>        | [<span data-ttu-id="0d885-260">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="0d885-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0d885-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0d885-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0d885-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d885-262">Entry</span></span> | <span data-ttu-id="0d885-263">Значение</span><span class="sxs-lookup"><span data-stu-id="0d885-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d885-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d885-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d885-265">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d885-266">System-Only</span></span>            | <span data-ttu-id="0d885-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-267">False</span></span>                           |
| <span data-ttu-id="0d885-268">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d885-268">Is-Single-Valued</span></span>       | <span data-ttu-id="0d885-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-269">False</span></span>                           |
| <span data-ttu-id="0d885-270">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d885-270">Is Indexed</span></span>             | <span data-ttu-id="0d885-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-271">False</span></span>                           |
| <span data-ttu-id="0d885-272">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d885-272">In Global Catalog</span></span>      | <span data-ttu-id="0d885-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-273">False</span></span>                           |
| <span data-ttu-id="0d885-274">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d885-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d885-275">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d885-275">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d885-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d885-276">Range-Lower</span></span>            | <span data-ttu-id="0d885-277">16</span><span class="sxs-lookup"><span data-stu-id="0d885-277">16</span></span>                              |
| <span data-ttu-id="0d885-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d885-278">Range-Upper</span></span>            | <span data-ttu-id="0d885-279">16</span><span class="sxs-lookup"><span data-stu-id="0d885-279">16</span></span>                              |
| <span data-ttu-id="0d885-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-280">Search-Flags</span></span>           | <span data-ttu-id="0d885-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d885-281">0x00000000</span></span>                      |
| <span data-ttu-id="0d885-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-282">System-Flags</span></span>           | <span data-ttu-id="0d885-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d885-283">0x00000010</span></span>                      |
| <span data-ttu-id="0d885-284">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d885-284">Classes used in</span></span>        | [<span data-ttu-id="0d885-285">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="0d885-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0d885-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d885-286">Windows Server 2012</span></span>



| <span data-ttu-id="0d885-287">Ввод</span><span class="sxs-lookup"><span data-stu-id="0d885-287">Entry</span></span> | <span data-ttu-id="0d885-288">Значение</span><span class="sxs-lookup"><span data-stu-id="0d885-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="0d885-289">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0d885-289">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-290">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d885-290">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="0d885-291">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d885-291">System-Only</span></span>            | <span data-ttu-id="0d885-292">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-292">False</span></span>                           |
| <span data-ttu-id="0d885-293">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0d885-293">Is-Single-Valued</span></span>       | <span data-ttu-id="0d885-294">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-294">False</span></span>                           |
| <span data-ttu-id="0d885-295">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0d885-295">Is Indexed</span></span>             | <span data-ttu-id="0d885-296">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-296">False</span></span>                           |
| <span data-ttu-id="0d885-297">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0d885-297">In Global Catalog</span></span>      | <span data-ttu-id="0d885-298">Неверно</span><span class="sxs-lookup"><span data-stu-id="0d885-298">False</span></span>                           |
| <span data-ttu-id="0d885-299">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0d885-299">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d885-300">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0d885-300">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="0d885-301">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d885-301">Range-Lower</span></span>            | <span data-ttu-id="0d885-302">16</span><span class="sxs-lookup"><span data-stu-id="0d885-302">16</span></span>                              |
| <span data-ttu-id="0d885-303">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d885-303">Range-Upper</span></span>            | <span data-ttu-id="0d885-304">16</span><span class="sxs-lookup"><span data-stu-id="0d885-304">16</span></span>                              |
| <span data-ttu-id="0d885-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-305">Search-Flags</span></span>           | <span data-ttu-id="0d885-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d885-306">0x00000000</span></span>                      |
| <span data-ttu-id="0d885-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d885-307">System-Flags</span></span>           | <span data-ttu-id="0d885-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d885-308">0x00000010</span></span>                      |
| <span data-ttu-id="0d885-309">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0d885-309">Classes used in</span></span>        | [<span data-ttu-id="0d885-310">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="0d885-310">**Top**</span></span>](c-top.md)<br/> |



 

 





