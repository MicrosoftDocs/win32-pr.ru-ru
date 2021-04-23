---
title: Атрибут ms-DS-с экземпляром-NC
description: Сведения о состоянии репликации DS, аналогичные (и надмножество) существующих атрибутов Хасмастернкс и Хаспартиалрепликанкс. Используется в KCC при настройке партнеров репликации.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута NC для MS-DS-с созданным экземпляром
- Схема AD атрибута msDS-Хасинстантиатеднкс
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493821"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a><span data-ttu-id="060c9-106">Атрибут ms-DS-с экземпляром-NC</span><span class="sxs-lookup"><span data-stu-id="060c9-106">ms-DS-Has-Instantiated-NCs attribute</span></span>

<span data-ttu-id="060c9-107">Сведения о состоянии репликации DS, аналогичные (и надмножество) существующих атрибутов Хасмастернкс и Хаспартиалрепликанкс.</span><span class="sxs-lookup"><span data-stu-id="060c9-107">DS replication state information, analogous to (and a superset of) the existing attributes hasMasterNCs and hasPartialReplicaNCs.</span></span> <span data-ttu-id="060c9-108">Используется в KCC при настройке партнеров репликации.</span><span class="sxs-lookup"><span data-stu-id="060c9-108">To be used by the KCC when setting up replication partners.</span></span>



| <span data-ttu-id="060c9-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="060c9-109">Entry</span></span> | <span data-ttu-id="060c9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="060c9-110">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="060c9-111">CN</span><span class="sxs-lookup"><span data-stu-id="060c9-111">CN</span></span>                | <span data-ttu-id="060c9-112">MS-DS-создан экземпляр — NC</span><span class="sxs-lookup"><span data-stu-id="060c9-112">ms-DS-Has-Instantiated-NCs</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="060c9-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="060c9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="060c9-114">msDS-Хасинстантиатеднкс</span><span class="sxs-lookup"><span data-stu-id="060c9-114">msDS-HasInstantiatedNCs</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="060c9-115">Размер</span><span class="sxs-lookup"><span data-stu-id="060c9-115">Size</span></span>              | <span data-ttu-id="060c9-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="060c9-116">4 bytes</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="060c9-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="060c9-117">Update Privilege</span></span>  | <span data-ttu-id="060c9-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="060c9-118">This value is set by the system.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="060c9-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="060c9-119">Update Frequency</span></span>  | <span data-ttu-id="060c9-120">Примерно вдвое чаще, чем Хасмастернкс/Хаспартиалрепликанкс.</span><span class="sxs-lookup"><span data-stu-id="060c9-120">Roughly twice as often as hasMasterNCs / hasPartialReplicaNCs.</span></span> <span data-ttu-id="060c9-121">Эти существующие атрибуты обновляются только в том случае, если контроллер домена добавляет или удаляет секцию (например, при переходе с контроллера домена на GC или наоборот).</span><span class="sxs-lookup"><span data-stu-id="060c9-121">These existing attributes are updated only when the DC adds or removes a partition (For example, when changing from DC to GC or vice versa).</span></span> |
| <span data-ttu-id="060c9-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="060c9-122">Attribute-Id</span></span>      | <span data-ttu-id="060c9-123">1.2.840.113556.1.4.1709</span><span class="sxs-lookup"><span data-stu-id="060c9-123">1.2.840.113556.1.4.1709</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="060c9-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="060c9-124">System-Id-Guid</span></span>    | <span data-ttu-id="060c9-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span><span class="sxs-lookup"><span data-stu-id="060c9-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span></span>                                                                                                                                                                        |
| <span data-ttu-id="060c9-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="060c9-126">Syntax</span></span>            | [<span data-ttu-id="060c9-127">**Object(двоичный_DN)**</span><span class="sxs-lookup"><span data-stu-id="060c9-127">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a><span data-ttu-id="060c9-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="060c9-128">Implementations</span></span>

-   [<span data-ttu-id="060c9-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="060c9-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="060c9-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="060c9-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="060c9-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="060c9-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="060c9-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="060c9-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="060c9-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="060c9-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="060c9-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="060c9-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="060c9-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="060c9-135">Windows Server 2003</span></span>



| <span data-ttu-id="060c9-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="060c9-136">Entry</span></span> | <span data-ttu-id="060c9-137">Значение</span><span class="sxs-lookup"><span data-stu-id="060c9-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="060c9-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="060c9-138">Link-Id</span></span>                | <span data-ttu-id="060c9-139">2002</span><span class="sxs-lookup"><span data-stu-id="060c9-139">2002</span></span>                                     |
| <span data-ttu-id="060c9-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="060c9-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="060c9-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="060c9-141">System-Only</span></span>            | <span data-ttu-id="060c9-142">True</span><span class="sxs-lookup"><span data-stu-id="060c9-142">True</span></span>                                     |
| <span data-ttu-id="060c9-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="060c9-143">Is-Single-Valued</span></span>       | <span data-ttu-id="060c9-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-144">False</span></span>                                    |
| <span data-ttu-id="060c9-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="060c9-145">Is Indexed</span></span>             | <span data-ttu-id="060c9-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-146">False</span></span>                                    |
| <span data-ttu-id="060c9-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="060c9-147">In Global Catalog</span></span>      | <span data-ttu-id="060c9-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-148">False</span></span>                                    |
| <span data-ttu-id="060c9-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="060c9-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="060c9-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="060c9-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="060c9-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="060c9-151">Range-Lower</span></span>            | <span data-ttu-id="060c9-152">4</span><span class="sxs-lookup"><span data-stu-id="060c9-152">4</span></span>                                        |
| <span data-ttu-id="060c9-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="060c9-153">Range-Upper</span></span>            | <span data-ttu-id="060c9-154">4</span><span class="sxs-lookup"><span data-stu-id="060c9-154">4</span></span>                                        |
| <span data-ttu-id="060c9-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-155">Search-Flags</span></span>           | <span data-ttu-id="060c9-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="060c9-156">0x00000000</span></span>                               |
| <span data-ttu-id="060c9-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-157">System-Flags</span></span>           | <span data-ttu-id="060c9-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="060c9-158">0x00000010</span></span>                               |
| <span data-ttu-id="060c9-159">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="060c9-159">Classes used in</span></span>        | [<span data-ttu-id="060c9-160">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="060c9-160">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="060c9-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="060c9-161">ADAM</span></span>



| <span data-ttu-id="060c9-162">Ввод</span><span class="sxs-lookup"><span data-stu-id="060c9-162">Entry</span></span> | <span data-ttu-id="060c9-163">Значение</span><span class="sxs-lookup"><span data-stu-id="060c9-163">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="060c9-164">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="060c9-164">Link-Id</span></span>                | <span data-ttu-id="060c9-165">2002</span><span class="sxs-lookup"><span data-stu-id="060c9-165">2002</span></span>                                     |
| <span data-ttu-id="060c9-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="060c9-166">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="060c9-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="060c9-167">System-Only</span></span>            | <span data-ttu-id="060c9-168">True</span><span class="sxs-lookup"><span data-stu-id="060c9-168">True</span></span>                                     |
| <span data-ttu-id="060c9-169">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="060c9-169">Is-Single-Valued</span></span>       | <span data-ttu-id="060c9-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-170">False</span></span>                                    |
| <span data-ttu-id="060c9-171">Индексируется</span><span class="sxs-lookup"><span data-stu-id="060c9-171">Is Indexed</span></span>             | <span data-ttu-id="060c9-172">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-172">False</span></span>                                    |
| <span data-ttu-id="060c9-173">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="060c9-173">In Global Catalog</span></span>      | <span data-ttu-id="060c9-174">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-174">False</span></span>                                    |
| <span data-ttu-id="060c9-175">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="060c9-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="060c9-176">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="060c9-176">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="060c9-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="060c9-177">Range-Lower</span></span>            | <span data-ttu-id="060c9-178">4</span><span class="sxs-lookup"><span data-stu-id="060c9-178">4</span></span>                                        |
| <span data-ttu-id="060c9-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="060c9-179">Range-Upper</span></span>            | <span data-ttu-id="060c9-180">4</span><span class="sxs-lookup"><span data-stu-id="060c9-180">4</span></span>                                        |
| <span data-ttu-id="060c9-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-181">Search-Flags</span></span>           | <span data-ttu-id="060c9-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="060c9-182">0x00000000</span></span>                               |
| <span data-ttu-id="060c9-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-183">System-Flags</span></span>           | <span data-ttu-id="060c9-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="060c9-184">0x00000010</span></span>                               |
| <span data-ttu-id="060c9-185">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="060c9-185">Classes used in</span></span>        | [<span data-ttu-id="060c9-186">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="060c9-186">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="060c9-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="060c9-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="060c9-188">Ввод</span><span class="sxs-lookup"><span data-stu-id="060c9-188">Entry</span></span> | <span data-ttu-id="060c9-189">Значение</span><span class="sxs-lookup"><span data-stu-id="060c9-189">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="060c9-190">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="060c9-190">Link-Id</span></span>                | <span data-ttu-id="060c9-191">2002</span><span class="sxs-lookup"><span data-stu-id="060c9-191">2002</span></span>                                     |
| <span data-ttu-id="060c9-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="060c9-192">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="060c9-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="060c9-193">System-Only</span></span>            | <span data-ttu-id="060c9-194">True</span><span class="sxs-lookup"><span data-stu-id="060c9-194">True</span></span>                                     |
| <span data-ttu-id="060c9-195">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="060c9-195">Is-Single-Valued</span></span>       | <span data-ttu-id="060c9-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-196">False</span></span>                                    |
| <span data-ttu-id="060c9-197">Индексируется</span><span class="sxs-lookup"><span data-stu-id="060c9-197">Is Indexed</span></span>             | <span data-ttu-id="060c9-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-198">False</span></span>                                    |
| <span data-ttu-id="060c9-199">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="060c9-199">In Global Catalog</span></span>      | <span data-ttu-id="060c9-200">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-200">False</span></span>                                    |
| <span data-ttu-id="060c9-201">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="060c9-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="060c9-202">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="060c9-202">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="060c9-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="060c9-203">Range-Lower</span></span>            | <span data-ttu-id="060c9-204">4</span><span class="sxs-lookup"><span data-stu-id="060c9-204">4</span></span>                                        |
| <span data-ttu-id="060c9-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="060c9-205">Range-Upper</span></span>            | <span data-ttu-id="060c9-206">4</span><span class="sxs-lookup"><span data-stu-id="060c9-206">4</span></span>                                        |
| <span data-ttu-id="060c9-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-207">Search-Flags</span></span>           | <span data-ttu-id="060c9-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="060c9-208">0x00000000</span></span>                               |
| <span data-ttu-id="060c9-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-209">System-Flags</span></span>           | <span data-ttu-id="060c9-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="060c9-210">0x00000010</span></span>                               |
| <span data-ttu-id="060c9-211">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="060c9-211">Classes used in</span></span>        | [<span data-ttu-id="060c9-212">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="060c9-212">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="060c9-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="060c9-213">Windows Server 2008</span></span>



| <span data-ttu-id="060c9-214">Ввод</span><span class="sxs-lookup"><span data-stu-id="060c9-214">Entry</span></span> | <span data-ttu-id="060c9-215">Значение</span><span class="sxs-lookup"><span data-stu-id="060c9-215">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="060c9-216">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="060c9-216">Link-Id</span></span>                | <span data-ttu-id="060c9-217">2002</span><span class="sxs-lookup"><span data-stu-id="060c9-217">2002</span></span>                                     |
| <span data-ttu-id="060c9-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="060c9-218">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="060c9-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="060c9-219">System-Only</span></span>            | <span data-ttu-id="060c9-220">True</span><span class="sxs-lookup"><span data-stu-id="060c9-220">True</span></span>                                     |
| <span data-ttu-id="060c9-221">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="060c9-221">Is-Single-Valued</span></span>       | <span data-ttu-id="060c9-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-222">False</span></span>                                    |
| <span data-ttu-id="060c9-223">Индексируется</span><span class="sxs-lookup"><span data-stu-id="060c9-223">Is Indexed</span></span>             | <span data-ttu-id="060c9-224">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-224">False</span></span>                                    |
| <span data-ttu-id="060c9-225">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="060c9-225">In Global Catalog</span></span>      | <span data-ttu-id="060c9-226">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-226">False</span></span>                                    |
| <span data-ttu-id="060c9-227">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="060c9-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="060c9-228">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="060c9-228">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="060c9-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="060c9-229">Range-Lower</span></span>            | <span data-ttu-id="060c9-230">4</span><span class="sxs-lookup"><span data-stu-id="060c9-230">4</span></span>                                        |
| <span data-ttu-id="060c9-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="060c9-231">Range-Upper</span></span>            | <span data-ttu-id="060c9-232">4</span><span class="sxs-lookup"><span data-stu-id="060c9-232">4</span></span>                                        |
| <span data-ttu-id="060c9-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-233">Search-Flags</span></span>           | <span data-ttu-id="060c9-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="060c9-234">0x00000000</span></span>                               |
| <span data-ttu-id="060c9-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-235">System-Flags</span></span>           | <span data-ttu-id="060c9-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="060c9-236">0x00000010</span></span>                               |
| <span data-ttu-id="060c9-237">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="060c9-237">Classes used in</span></span>        | [<span data-ttu-id="060c9-238">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="060c9-238">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="060c9-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="060c9-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="060c9-240">Ввод</span><span class="sxs-lookup"><span data-stu-id="060c9-240">Entry</span></span> | <span data-ttu-id="060c9-241">Значение</span><span class="sxs-lookup"><span data-stu-id="060c9-241">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="060c9-242">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="060c9-242">Link-Id</span></span>                | <span data-ttu-id="060c9-243">2002</span><span class="sxs-lookup"><span data-stu-id="060c9-243">2002</span></span>                                     |
| <span data-ttu-id="060c9-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="060c9-244">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="060c9-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="060c9-245">System-Only</span></span>            | <span data-ttu-id="060c9-246">True</span><span class="sxs-lookup"><span data-stu-id="060c9-246">True</span></span>                                     |
| <span data-ttu-id="060c9-247">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="060c9-247">Is-Single-Valued</span></span>       | <span data-ttu-id="060c9-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-248">False</span></span>                                    |
| <span data-ttu-id="060c9-249">Индексируется</span><span class="sxs-lookup"><span data-stu-id="060c9-249">Is Indexed</span></span>             | <span data-ttu-id="060c9-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-250">False</span></span>                                    |
| <span data-ttu-id="060c9-251">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="060c9-251">In Global Catalog</span></span>      | <span data-ttu-id="060c9-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-252">False</span></span>                                    |
| <span data-ttu-id="060c9-253">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="060c9-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="060c9-254">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="060c9-254">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="060c9-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="060c9-255">Range-Lower</span></span>            | <span data-ttu-id="060c9-256">4</span><span class="sxs-lookup"><span data-stu-id="060c9-256">4</span></span>                                        |
| <span data-ttu-id="060c9-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="060c9-257">Range-Upper</span></span>            | <span data-ttu-id="060c9-258">4</span><span class="sxs-lookup"><span data-stu-id="060c9-258">4</span></span>                                        |
| <span data-ttu-id="060c9-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-259">Search-Flags</span></span>           | <span data-ttu-id="060c9-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="060c9-260">0x00000000</span></span>                               |
| <span data-ttu-id="060c9-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-261">System-Flags</span></span>           | <span data-ttu-id="060c9-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="060c9-262">0x00000010</span></span>                               |
| <span data-ttu-id="060c9-263">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="060c9-263">Classes used in</span></span>        | [<span data-ttu-id="060c9-264">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="060c9-264">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="060c9-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="060c9-265">Windows Server 2012</span></span>



| <span data-ttu-id="060c9-266">Ввод</span><span class="sxs-lookup"><span data-stu-id="060c9-266">Entry</span></span> | <span data-ttu-id="060c9-267">Значение</span><span class="sxs-lookup"><span data-stu-id="060c9-267">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="060c9-268">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="060c9-268">Link-Id</span></span>                | <span data-ttu-id="060c9-269">2002</span><span class="sxs-lookup"><span data-stu-id="060c9-269">2002</span></span>                                     |
| <span data-ttu-id="060c9-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="060c9-270">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="060c9-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="060c9-271">System-Only</span></span>            | <span data-ttu-id="060c9-272">True</span><span class="sxs-lookup"><span data-stu-id="060c9-272">True</span></span>                                     |
| <span data-ttu-id="060c9-273">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="060c9-273">Is-Single-Valued</span></span>       | <span data-ttu-id="060c9-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-274">False</span></span>                                    |
| <span data-ttu-id="060c9-275">Индексируется</span><span class="sxs-lookup"><span data-stu-id="060c9-275">Is Indexed</span></span>             | <span data-ttu-id="060c9-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-276">False</span></span>                                    |
| <span data-ttu-id="060c9-277">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="060c9-277">In Global Catalog</span></span>      | <span data-ttu-id="060c9-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="060c9-278">False</span></span>                                    |
| <span data-ttu-id="060c9-279">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="060c9-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="060c9-280">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="060c9-280">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="060c9-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="060c9-281">Range-Lower</span></span>            | <span data-ttu-id="060c9-282">4</span><span class="sxs-lookup"><span data-stu-id="060c9-282">4</span></span>                                        |
| <span data-ttu-id="060c9-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="060c9-283">Range-Upper</span></span>            | <span data-ttu-id="060c9-284">4</span><span class="sxs-lookup"><span data-stu-id="060c9-284">4</span></span>                                        |
| <span data-ttu-id="060c9-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-285">Search-Flags</span></span>           | <span data-ttu-id="060c9-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="060c9-286">0x00000000</span></span>                               |
| <span data-ttu-id="060c9-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="060c9-287">System-Flags</span></span>           | <span data-ttu-id="060c9-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="060c9-288">0x00000010</span></span>                               |
| <span data-ttu-id="060c9-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="060c9-289">Classes used in</span></span>        | [<span data-ttu-id="060c9-290">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="060c9-290">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





