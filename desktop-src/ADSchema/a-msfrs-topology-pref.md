---
title: атрибут MS-FRS-Topology-преф
description: Атрибут MS-FRS-Topology-преф используется для записи предпочтительных параметров топологии NTFRS.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-FRS-Topology-преф
- Мсфрс-Topology-схема AD атрибута преф
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804649"
---
# <a name="ms-frs-topology-pref-attribute"></a><span data-ttu-id="419c6-105">атрибут MS-FRS-Topology-преф</span><span class="sxs-lookup"><span data-stu-id="419c6-105">ms-FRS-Topology-Pref attribute</span></span>

<span data-ttu-id="419c6-106">Атрибут **MS-FRS-Topology-преф** используется для записи предпочтительных параметров топологии NTFRS.</span><span class="sxs-lookup"><span data-stu-id="419c6-106">The **ms-FRS-Topology-Pref** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="419c6-107">Когда член FRS добавляется в набор реплик или удаляется из него, эти атрибуты называются и вносятся изменения в соединения между остальными членами FRS в наборе реплик.</span><span class="sxs-lookup"><span data-stu-id="419c6-107">When an FRS member gets added or deleted to the replica set, these attributes are referred, and adjustments made to the connections between the rest of the FRS members in the replica set.</span></span>

<span data-ttu-id="419c6-108">Допустимые значения для этого атрибута:</span><span class="sxs-lookup"><span data-stu-id="419c6-108">Valid values for this attribute are as follows.</span></span>

| <span data-ttu-id="419c6-109">Значение</span><span class="sxs-lookup"><span data-stu-id="419c6-109">Value</span></span> | <span data-ttu-id="419c6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="419c6-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="419c6-111">1</span><span class="sxs-lookup"><span data-stu-id="419c6-111">1</span></span>     | <span data-ttu-id="419c6-112">\_рстопологипреф \_ кольца FRS</span><span class="sxs-lookup"><span data-stu-id="419c6-112">FRS\_RSTOPOLOGYPREF\_RING</span></span><br/>     |
| <span data-ttu-id="419c6-113">2</span><span class="sxs-lookup"><span data-stu-id="419c6-113">2</span></span>     | <span data-ttu-id="419c6-114">FRS \_ рстопологипреф \_ хубспоке</span><span class="sxs-lookup"><span data-stu-id="419c6-114">FRS\_RSTOPOLOGYPREF\_HUBSPOKE</span></span><br/> |
| <span data-ttu-id="419c6-115">3</span><span class="sxs-lookup"><span data-stu-id="419c6-115">3</span></span>     | <span data-ttu-id="419c6-116">FRS \_ рстопологипреф \_ фуллмеш</span><span class="sxs-lookup"><span data-stu-id="419c6-116">FRS\_RSTOPOLOGYPREF\_FULLMESH</span></span><br/> |
| <span data-ttu-id="419c6-117">4</span><span class="sxs-lookup"><span data-stu-id="419c6-117">4</span></span>     | <span data-ttu-id="419c6-118">\_РСТОПОЛОГИПРЕФ FRS \_</span><span class="sxs-lookup"><span data-stu-id="419c6-118">FRS\_RSTOPOLOGYPREF\_CUSTOM</span></span><br/>   |



 



| <span data-ttu-id="419c6-119">Ввод</span><span class="sxs-lookup"><span data-stu-id="419c6-119">Entry</span></span> | <span data-ttu-id="419c6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="419c6-120">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="419c6-121">CN</span><span class="sxs-lookup"><span data-stu-id="419c6-121">CN</span></span>                | <span data-ttu-id="419c6-122">MS-FRS-Topology-преф</span><span class="sxs-lookup"><span data-stu-id="419c6-122">ms-FRS-Topology-Pref</span></span>                                               |
| <span data-ttu-id="419c6-123">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="419c6-123">Ldap-Display-Name</span></span> | <span data-ttu-id="419c6-124">Мсфрс-Topology-преф</span><span class="sxs-lookup"><span data-stu-id="419c6-124">msFRS-Topology-Pref</span></span>                                                |
| <span data-ttu-id="419c6-125">Размер</span><span class="sxs-lookup"><span data-stu-id="419c6-125">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="419c6-126">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="419c6-126">Update Privilege</span></span>  | <span data-ttu-id="419c6-127">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="419c6-127">Domain administrator</span></span>                                               |
| <span data-ttu-id="419c6-128">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="419c6-128">Update Frequency</span></span>  | <span data-ttu-id="419c6-129">При создании набора реплик или изменении предпочтительной топологии.</span><span class="sxs-lookup"><span data-stu-id="419c6-129">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="419c6-130">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="419c6-130">Attribute-Id</span></span>      | <span data-ttu-id="419c6-131">1.2.840.113556.1.4.1692</span><span class="sxs-lookup"><span data-stu-id="419c6-131">1.2.840.113556.1.4.1692</span></span>                                            |
| <span data-ttu-id="419c6-132">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="419c6-132">System-Id-Guid</span></span>    | <span data-ttu-id="419c6-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span><span class="sxs-lookup"><span data-stu-id="419c6-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span></span>                               |
| <span data-ttu-id="419c6-134">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="419c6-134">Syntax</span></span>            | [<span data-ttu-id="419c6-135">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="419c6-135">**String(Unicode)**</span></span>](s-string-unicode.md)                        |



## <a name="implementations"></a><span data-ttu-id="419c6-136">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="419c6-136">Implementations</span></span>

-   [<span data-ttu-id="419c6-137">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="419c6-137">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="419c6-138">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="419c6-138">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="419c6-139">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="419c6-139">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="419c6-140">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="419c6-140">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="419c6-141">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="419c6-141">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="419c6-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="419c6-142">Windows Server 2003</span></span>



| <span data-ttu-id="419c6-143">Ввод</span><span class="sxs-lookup"><span data-stu-id="419c6-143">Entry</span></span> | <span data-ttu-id="419c6-144">Значение</span><span class="sxs-lookup"><span data-stu-id="419c6-144">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="419c6-145">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="419c6-145">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-146">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="419c6-146">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-147">System-Only</span><span class="sxs-lookup"><span data-stu-id="419c6-147">System-Only</span></span>            | <span data-ttu-id="419c6-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-148">False</span></span>                                                     |
| <span data-ttu-id="419c6-149">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="419c6-149">Is-Single-Valued</span></span>       | <span data-ttu-id="419c6-150">True</span><span class="sxs-lookup"><span data-stu-id="419c6-150">True</span></span>                                                      |
| <span data-ttu-id="419c6-151">Индексируется</span><span class="sxs-lookup"><span data-stu-id="419c6-151">Is Indexed</span></span>             | <span data-ttu-id="419c6-152">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-152">False</span></span>                                                     |
| <span data-ttu-id="419c6-153">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="419c6-153">In Global Catalog</span></span>      | <span data-ttu-id="419c6-154">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-154">False</span></span>                                                     |
| <span data-ttu-id="419c6-155">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="419c6-155">NT-Security-Descriptor</span></span> | <span data-ttu-id="419c6-156">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="419c6-156">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="419c6-157">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="419c6-157">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-158">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="419c6-158">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-159">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-159">Search-Flags</span></span>           | <span data-ttu-id="419c6-160">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-160">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-161">System-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-161">System-Flags</span></span>           | <span data-ttu-id="419c6-162">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-162">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-163">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="419c6-163">Classes used in</span></span>        | [<span data-ttu-id="419c6-164">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="419c6-164">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="419c6-165">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="419c6-165">Windows Server 2003 R2</span></span>



| <span data-ttu-id="419c6-166">Ввод</span><span class="sxs-lookup"><span data-stu-id="419c6-166">Entry</span></span> | <span data-ttu-id="419c6-167">Значение</span><span class="sxs-lookup"><span data-stu-id="419c6-167">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="419c6-168">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="419c6-168">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-169">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="419c6-169">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="419c6-170">System-Only</span></span>            | <span data-ttu-id="419c6-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-171">False</span></span>                                                     |
| <span data-ttu-id="419c6-172">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="419c6-172">Is-Single-Valued</span></span>       | <span data-ttu-id="419c6-173">True</span><span class="sxs-lookup"><span data-stu-id="419c6-173">True</span></span>                                                      |
| <span data-ttu-id="419c6-174">Индексируется</span><span class="sxs-lookup"><span data-stu-id="419c6-174">Is Indexed</span></span>             | <span data-ttu-id="419c6-175">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-175">False</span></span>                                                     |
| <span data-ttu-id="419c6-176">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="419c6-176">In Global Catalog</span></span>      | <span data-ttu-id="419c6-177">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-177">False</span></span>                                                     |
| <span data-ttu-id="419c6-178">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="419c6-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="419c6-179">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="419c6-179">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="419c6-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="419c6-180">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-181">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="419c6-181">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-182">Search-Flags</span></span>           | <span data-ttu-id="419c6-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-183">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-184">System-Flags</span></span>           | <span data-ttu-id="419c6-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-185">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-186">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="419c6-186">Classes used in</span></span>        | [<span data-ttu-id="419c6-187">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="419c6-187">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="419c6-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="419c6-188">Windows Server 2008</span></span>



| <span data-ttu-id="419c6-189">Ввод</span><span class="sxs-lookup"><span data-stu-id="419c6-189">Entry</span></span> | <span data-ttu-id="419c6-190">Значение</span><span class="sxs-lookup"><span data-stu-id="419c6-190">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="419c6-191">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="419c6-191">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="419c6-192">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="419c6-193">System-Only</span></span>            | <span data-ttu-id="419c6-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-194">False</span></span>                                                     |
| <span data-ttu-id="419c6-195">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="419c6-195">Is-Single-Valued</span></span>       | <span data-ttu-id="419c6-196">True</span><span class="sxs-lookup"><span data-stu-id="419c6-196">True</span></span>                                                      |
| <span data-ttu-id="419c6-197">Индексируется</span><span class="sxs-lookup"><span data-stu-id="419c6-197">Is Indexed</span></span>             | <span data-ttu-id="419c6-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-198">False</span></span>                                                     |
| <span data-ttu-id="419c6-199">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="419c6-199">In Global Catalog</span></span>      | <span data-ttu-id="419c6-200">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-200">False</span></span>                                                     |
| <span data-ttu-id="419c6-201">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="419c6-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="419c6-202">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="419c6-202">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="419c6-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="419c6-203">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="419c6-204">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-205">Search-Flags</span></span>           | <span data-ttu-id="419c6-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-206">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-207">System-Flags</span></span>           | <span data-ttu-id="419c6-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-208">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-209">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="419c6-209">Classes used in</span></span>        | [<span data-ttu-id="419c6-210">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="419c6-210">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="419c6-211">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="419c6-211">Windows Server 2008 R2</span></span>



| <span data-ttu-id="419c6-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="419c6-212">Entry</span></span> | <span data-ttu-id="419c6-213">Значение</span><span class="sxs-lookup"><span data-stu-id="419c6-213">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="419c6-214">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="419c6-214">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="419c6-215">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="419c6-216">System-Only</span></span>            | <span data-ttu-id="419c6-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-217">False</span></span>                                                     |
| <span data-ttu-id="419c6-218">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="419c6-218">Is-Single-Valued</span></span>       | <span data-ttu-id="419c6-219">True</span><span class="sxs-lookup"><span data-stu-id="419c6-219">True</span></span>                                                      |
| <span data-ttu-id="419c6-220">Индексируется</span><span class="sxs-lookup"><span data-stu-id="419c6-220">Is Indexed</span></span>             | <span data-ttu-id="419c6-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-221">False</span></span>                                                     |
| <span data-ttu-id="419c6-222">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="419c6-222">In Global Catalog</span></span>      | <span data-ttu-id="419c6-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-223">False</span></span>                                                     |
| <span data-ttu-id="419c6-224">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="419c6-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="419c6-225">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="419c6-225">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="419c6-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="419c6-226">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="419c6-227">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-228">Search-Flags</span></span>           | <span data-ttu-id="419c6-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-229">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-230">System-Flags</span></span>           | <span data-ttu-id="419c6-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-231">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-232">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="419c6-232">Classes used in</span></span>        | [<span data-ttu-id="419c6-233">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="419c6-233">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="419c6-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="419c6-234">Windows Server 2012</span></span>



| <span data-ttu-id="419c6-235">Ввод</span><span class="sxs-lookup"><span data-stu-id="419c6-235">Entry</span></span> | <span data-ttu-id="419c6-236">Значение</span><span class="sxs-lookup"><span data-stu-id="419c6-236">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="419c6-237">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="419c6-237">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="419c6-238">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="419c6-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="419c6-239">System-Only</span></span>            | <span data-ttu-id="419c6-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-240">False</span></span>                                                     |
| <span data-ttu-id="419c6-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="419c6-241">Is-Single-Valued</span></span>       | <span data-ttu-id="419c6-242">True</span><span class="sxs-lookup"><span data-stu-id="419c6-242">True</span></span>                                                      |
| <span data-ttu-id="419c6-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="419c6-243">Is Indexed</span></span>             | <span data-ttu-id="419c6-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-244">False</span></span>                                                     |
| <span data-ttu-id="419c6-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="419c6-245">In Global Catalog</span></span>      | <span data-ttu-id="419c6-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="419c6-246">False</span></span>                                                     |
| <span data-ttu-id="419c6-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="419c6-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="419c6-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="419c6-248">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="419c6-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="419c6-249">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="419c6-250">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="419c6-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-251">Search-Flags</span></span>           | <span data-ttu-id="419c6-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-252">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="419c6-253">System-Flags</span></span>           | <span data-ttu-id="419c6-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="419c6-254">0x00000000</span></span>                                                |
| <span data-ttu-id="419c6-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="419c6-255">Classes used in</span></span>        | [<span data-ttu-id="419c6-256">**NTFRS-Set-реплика**</span><span class="sxs-lookup"><span data-stu-id="419c6-256">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





