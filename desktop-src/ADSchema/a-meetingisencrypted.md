---
title: атрибут Митингисенкриптед
description: Это справедливо, если собрание должно быть зашифровано.
ms.assetid: bf8c1344-9f7e-4e4f-aac7-52cb0b65b9f0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Митингисенкриптед
topic_type:
- apiref
api_name:
- meetingIsEncrypted
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e645624ff9167da7e8a6278e10bf57420cd152
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989721"
---
# <a name="meetingisencrypted-attribute"></a><span data-ttu-id="1478e-104">атрибут Митингисенкриптед</span><span class="sxs-lookup"><span data-stu-id="1478e-104">meetingIsEncrypted attribute</span></span>

<span data-ttu-id="1478e-105">Это **справедливо** , если собрание должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="1478e-105">This is **TRUE** if the meeting is to be encrypted.</span></span>



| <span data-ttu-id="1478e-106">Ввод</span><span class="sxs-lookup"><span data-stu-id="1478e-106">Entry</span></span> | <span data-ttu-id="1478e-107">Значение</span><span class="sxs-lookup"><span data-stu-id="1478e-107">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1478e-108">CN</span><span class="sxs-lookup"><span data-stu-id="1478e-108">CN</span></span>                | <span data-ttu-id="1478e-109">митингисенкриптед</span><span class="sxs-lookup"><span data-stu-id="1478e-109">meetingIsEncrypted</span></span>                                                               |
| <span data-ttu-id="1478e-110">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1478e-110">Ldap-Display-Name</span></span> | <span data-ttu-id="1478e-111">митингисенкриптед</span><span class="sxs-lookup"><span data-stu-id="1478e-111">meetingIsEncrypted</span></span>                                                               |
| <span data-ttu-id="1478e-112">Размер</span><span class="sxs-lookup"><span data-stu-id="1478e-112">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="1478e-113">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1478e-113">Update Privilege</span></span>  | <span data-ttu-id="1478e-114">Любой пользователь может обновить этот объект на основе безопасности создаваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="1478e-114">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="1478e-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1478e-115">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="1478e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1478e-116">Attribute-Id</span></span>      | <span data-ttu-id="1478e-117">1.2.840.113556.1.4.585</span><span class="sxs-lookup"><span data-stu-id="1478e-117">1.2.840.113556.1.4.585</span></span>                                                           |
| <span data-ttu-id="1478e-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1478e-118">System-Id-Guid</span></span>    | <span data-ttu-id="1478e-119">11b6cc8e-48c4-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1478e-119">11b6cc8e-48c4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="1478e-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1478e-120">Syntax</span></span>            | [<span data-ttu-id="1478e-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="1478e-121">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="1478e-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1478e-122">Implementations</span></span>

-   [<span data-ttu-id="1478e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1478e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1478e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1478e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1478e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1478e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1478e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1478e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1478e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1478e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1478e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1478e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1478e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1478e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1478e-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="1478e-130">Entry</span></span> | <span data-ttu-id="1478e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1478e-131">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="1478e-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1478e-132">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1478e-133">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1478e-134">System-Only</span></span>            | <span data-ttu-id="1478e-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-135">False</span></span>                                   |
| <span data-ttu-id="1478e-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1478e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1478e-137">True</span><span class="sxs-lookup"><span data-stu-id="1478e-137">True</span></span>                                    |
| <span data-ttu-id="1478e-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1478e-138">Is Indexed</span></span>             | <span data-ttu-id="1478e-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-139">False</span></span>                                   |
| <span data-ttu-id="1478e-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1478e-140">In Global Catalog</span></span>      | <span data-ttu-id="1478e-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-141">False</span></span>                                   |
| <span data-ttu-id="1478e-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1478e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1478e-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1478e-143">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="1478e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1478e-144">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="1478e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1478e-145">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="1478e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-146">Search-Flags</span></span>           | <span data-ttu-id="1478e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1478e-147">0x00000000</span></span>                              |
| <span data-ttu-id="1478e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-148">System-Flags</span></span>           | <span data-ttu-id="1478e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1478e-149">0x00000010</span></span>                              |
| <span data-ttu-id="1478e-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1478e-150">Classes used in</span></span>        | [<span data-ttu-id="1478e-151">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="1478e-151">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1478e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1478e-152">Windows Server 2003</span></span>



| <span data-ttu-id="1478e-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="1478e-153">Entry</span></span> | <span data-ttu-id="1478e-154">Значение</span><span class="sxs-lookup"><span data-stu-id="1478e-154">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="1478e-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1478e-155">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1478e-156">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="1478e-157">System-Only</span></span>            | <span data-ttu-id="1478e-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-158">False</span></span>                                   |
| <span data-ttu-id="1478e-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1478e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="1478e-160">True</span><span class="sxs-lookup"><span data-stu-id="1478e-160">True</span></span>                                    |
| <span data-ttu-id="1478e-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1478e-161">Is Indexed</span></span>             | <span data-ttu-id="1478e-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-162">False</span></span>                                   |
| <span data-ttu-id="1478e-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1478e-163">In Global Catalog</span></span>      | <span data-ttu-id="1478e-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-164">False</span></span>                                   |
| <span data-ttu-id="1478e-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1478e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="1478e-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1478e-166">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="1478e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1478e-167">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="1478e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1478e-168">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="1478e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-169">Search-Flags</span></span>           | <span data-ttu-id="1478e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1478e-170">0x00000000</span></span>                              |
| <span data-ttu-id="1478e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-171">System-Flags</span></span>           | <span data-ttu-id="1478e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1478e-172">0x00000010</span></span>                              |
| <span data-ttu-id="1478e-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1478e-173">Classes used in</span></span>        | [<span data-ttu-id="1478e-174">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="1478e-174">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1478e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1478e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1478e-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="1478e-176">Entry</span></span> | <span data-ttu-id="1478e-177">Значение</span><span class="sxs-lookup"><span data-stu-id="1478e-177">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="1478e-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1478e-178">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1478e-179">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="1478e-180">System-Only</span></span>            | <span data-ttu-id="1478e-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-181">False</span></span>                                   |
| <span data-ttu-id="1478e-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1478e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="1478e-183">True</span><span class="sxs-lookup"><span data-stu-id="1478e-183">True</span></span>                                    |
| <span data-ttu-id="1478e-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1478e-184">Is Indexed</span></span>             | <span data-ttu-id="1478e-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-185">False</span></span>                                   |
| <span data-ttu-id="1478e-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1478e-186">In Global Catalog</span></span>      | <span data-ttu-id="1478e-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-187">False</span></span>                                   |
| <span data-ttu-id="1478e-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1478e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="1478e-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1478e-189">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="1478e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1478e-190">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="1478e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1478e-191">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="1478e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-192">Search-Flags</span></span>           | <span data-ttu-id="1478e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1478e-193">0x00000000</span></span>                              |
| <span data-ttu-id="1478e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-194">System-Flags</span></span>           | <span data-ttu-id="1478e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1478e-195">0x00000010</span></span>                              |
| <span data-ttu-id="1478e-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1478e-196">Classes used in</span></span>        | [<span data-ttu-id="1478e-197">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="1478e-197">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1478e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1478e-198">Windows Server 2008</span></span>



| <span data-ttu-id="1478e-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="1478e-199">Entry</span></span> | <span data-ttu-id="1478e-200">Значение</span><span class="sxs-lookup"><span data-stu-id="1478e-200">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="1478e-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1478e-201">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1478e-202">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="1478e-203">System-Only</span></span>            | <span data-ttu-id="1478e-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-204">False</span></span>                                   |
| <span data-ttu-id="1478e-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1478e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="1478e-206">True</span><span class="sxs-lookup"><span data-stu-id="1478e-206">True</span></span>                                    |
| <span data-ttu-id="1478e-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1478e-207">Is Indexed</span></span>             | <span data-ttu-id="1478e-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-208">False</span></span>                                   |
| <span data-ttu-id="1478e-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1478e-209">In Global Catalog</span></span>      | <span data-ttu-id="1478e-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-210">False</span></span>                                   |
| <span data-ttu-id="1478e-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1478e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="1478e-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1478e-212">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="1478e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1478e-213">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="1478e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1478e-214">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="1478e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-215">Search-Flags</span></span>           | <span data-ttu-id="1478e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1478e-216">0x00000000</span></span>                              |
| <span data-ttu-id="1478e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-217">System-Flags</span></span>           | <span data-ttu-id="1478e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1478e-218">0x00000010</span></span>                              |
| <span data-ttu-id="1478e-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1478e-219">Classes used in</span></span>        | [<span data-ttu-id="1478e-220">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="1478e-220">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1478e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1478e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1478e-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="1478e-222">Entry</span></span> | <span data-ttu-id="1478e-223">Значение</span><span class="sxs-lookup"><span data-stu-id="1478e-223">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="1478e-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1478e-224">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1478e-225">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="1478e-226">System-Only</span></span>            | <span data-ttu-id="1478e-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-227">False</span></span>                                   |
| <span data-ttu-id="1478e-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1478e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="1478e-229">True</span><span class="sxs-lookup"><span data-stu-id="1478e-229">True</span></span>                                    |
| <span data-ttu-id="1478e-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1478e-230">Is Indexed</span></span>             | <span data-ttu-id="1478e-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-231">False</span></span>                                   |
| <span data-ttu-id="1478e-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1478e-232">In Global Catalog</span></span>      | <span data-ttu-id="1478e-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-233">False</span></span>                                   |
| <span data-ttu-id="1478e-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1478e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="1478e-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1478e-235">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="1478e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1478e-236">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="1478e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1478e-237">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="1478e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-238">Search-Flags</span></span>           | <span data-ttu-id="1478e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1478e-239">0x00000000</span></span>                              |
| <span data-ttu-id="1478e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-240">System-Flags</span></span>           | <span data-ttu-id="1478e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1478e-241">0x00000010</span></span>                              |
| <span data-ttu-id="1478e-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1478e-242">Classes used in</span></span>        | [<span data-ttu-id="1478e-243">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="1478e-243">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1478e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1478e-244">Windows Server 2012</span></span>



| <span data-ttu-id="1478e-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="1478e-245">Entry</span></span> | <span data-ttu-id="1478e-246">Значение</span><span class="sxs-lookup"><span data-stu-id="1478e-246">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="1478e-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1478e-247">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1478e-248">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="1478e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="1478e-249">System-Only</span></span>            | <span data-ttu-id="1478e-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-250">False</span></span>                                   |
| <span data-ttu-id="1478e-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1478e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="1478e-252">True</span><span class="sxs-lookup"><span data-stu-id="1478e-252">True</span></span>                                    |
| <span data-ttu-id="1478e-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1478e-253">Is Indexed</span></span>             | <span data-ttu-id="1478e-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-254">False</span></span>                                   |
| <span data-ttu-id="1478e-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1478e-255">In Global Catalog</span></span>      | <span data-ttu-id="1478e-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="1478e-256">False</span></span>                                   |
| <span data-ttu-id="1478e-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1478e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="1478e-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1478e-258">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="1478e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1478e-259">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="1478e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1478e-260">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="1478e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-261">Search-Flags</span></span>           | <span data-ttu-id="1478e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1478e-262">0x00000000</span></span>                              |
| <span data-ttu-id="1478e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1478e-263">System-Flags</span></span>           | <span data-ttu-id="1478e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1478e-264">0x00000010</span></span>                              |
| <span data-ttu-id="1478e-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1478e-265">Classes used in</span></span>        | [<span data-ttu-id="1478e-266">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="1478e-266">**Meeting**</span></span>](c-meeting.md)<br/> |



 

 





