---
title: атрибут Митингстарттиме
description: Дата и время начала собрания.
ms.assetid: ac13a3c9-20c0-48de-b3d2-9034af9dbde8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Митингстарттиме
topic_type:
- apiref
api_name:
- meetingStartTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a612680ec6c137274d7b29c0fffe6059dbc9a0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655235"
---
# <a name="meetingstarttime-attribute"></a><span data-ttu-id="2c3fe-104">атрибут Митингстарттиме</span><span class="sxs-lookup"><span data-stu-id="2c3fe-104">meetingStartTime attribute</span></span>

<span data-ttu-id="2c3fe-105">Дата и время начала собрания.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-105">The date and time that the meeting starts.</span></span>



| <span data-ttu-id="2c3fe-106">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c3fe-106">Entry</span></span> | <span data-ttu-id="2c3fe-107">Значение</span><span class="sxs-lookup"><span data-stu-id="2c3fe-107">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c3fe-108">CN</span><span class="sxs-lookup"><span data-stu-id="2c3fe-108">CN</span></span>                | <span data-ttu-id="2c3fe-109">митингстарттиме</span><span class="sxs-lookup"><span data-stu-id="2c3fe-109">meetingStartTime</span></span>                                                                 |
| <span data-ttu-id="2c3fe-110">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2c3fe-110">Ldap-Display-Name</span></span> | <span data-ttu-id="2c3fe-111">митингстарттиме</span><span class="sxs-lookup"><span data-stu-id="2c3fe-111">meetingStartTime</span></span>                                                                 |
| <span data-ttu-id="2c3fe-112">Размер</span><span class="sxs-lookup"><span data-stu-id="2c3fe-112">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="2c3fe-113">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2c3fe-113">Update Privilege</span></span>  | <span data-ttu-id="2c3fe-114">Любой пользователь может обновить этот объект на основе безопасности создаваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="2c3fe-114">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="2c3fe-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2c3fe-115">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="2c3fe-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2c3fe-116">Attribute-Id</span></span>      | <span data-ttu-id="2c3fe-117">1.2.840.113556.1.4.587</span><span class="sxs-lookup"><span data-stu-id="2c3fe-117">1.2.840.113556.1.4.587</span></span>                                                           |
| <span data-ttu-id="2c3fe-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2c3fe-118">System-Id-Guid</span></span>    | <span data-ttu-id="2c3fe-119">11b6cc90-48c4-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2c3fe-119">11b6cc90-48c4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="2c3fe-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c3fe-120">Syntax</span></span>            | [<span data-ttu-id="2c3fe-121">**String(обобщенное_время)**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-121">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md)                    |



## <a name="implementations"></a><span data-ttu-id="2c3fe-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2c3fe-122">Implementations</span></span>

-   [<span data-ttu-id="2c3fe-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2c3fe-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2c3fe-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2c3fe-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2c3fe-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2c3fe-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2c3fe-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c3fe-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2c3fe-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c3fe-130">Entry</span></span> | <span data-ttu-id="2c3fe-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2c3fe-131">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="2c3fe-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c3fe-132">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c3fe-133">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c3fe-134">System-Only</span></span>            | <span data-ttu-id="2c3fe-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-135">False</span></span>                                   |
| <span data-ttu-id="2c3fe-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c3fe-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2c3fe-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-137">False</span></span>                                   |
| <span data-ttu-id="2c3fe-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c3fe-138">Is Indexed</span></span>             | <span data-ttu-id="2c3fe-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-139">False</span></span>                                   |
| <span data-ttu-id="2c3fe-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c3fe-140">In Global Catalog</span></span>      | <span data-ttu-id="2c3fe-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-141">False</span></span>                                   |
| <span data-ttu-id="2c3fe-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c3fe-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c3fe-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c3fe-143">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="2c3fe-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c3fe-144">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c3fe-145">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-146">Search-Flags</span></span>           | <span data-ttu-id="2c3fe-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c3fe-147">0x00000000</span></span>                              |
| <span data-ttu-id="2c3fe-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-148">System-Flags</span></span>           | <span data-ttu-id="2c3fe-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c3fe-149">0x00000010</span></span>                              |
| <span data-ttu-id="2c3fe-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c3fe-150">Classes used in</span></span>        | [<span data-ttu-id="2c3fe-151">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-151">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2c3fe-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c3fe-152">Windows Server 2003</span></span>



| <span data-ttu-id="2c3fe-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c3fe-153">Entry</span></span> | <span data-ttu-id="2c3fe-154">Значение</span><span class="sxs-lookup"><span data-stu-id="2c3fe-154">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="2c3fe-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c3fe-155">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c3fe-156">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c3fe-157">System-Only</span></span>            | <span data-ttu-id="2c3fe-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-158">False</span></span>                                   |
| <span data-ttu-id="2c3fe-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c3fe-159">Is-Single-Valued</span></span>       | <span data-ttu-id="2c3fe-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-160">False</span></span>                                   |
| <span data-ttu-id="2c3fe-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c3fe-161">Is Indexed</span></span>             | <span data-ttu-id="2c3fe-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-162">False</span></span>                                   |
| <span data-ttu-id="2c3fe-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c3fe-163">In Global Catalog</span></span>      | <span data-ttu-id="2c3fe-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-164">False</span></span>                                   |
| <span data-ttu-id="2c3fe-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c3fe-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c3fe-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c3fe-166">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="2c3fe-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c3fe-167">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c3fe-168">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-169">Search-Flags</span></span>           | <span data-ttu-id="2c3fe-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c3fe-170">0x00000000</span></span>                              |
| <span data-ttu-id="2c3fe-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-171">System-Flags</span></span>           | <span data-ttu-id="2c3fe-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c3fe-172">0x00000010</span></span>                              |
| <span data-ttu-id="2c3fe-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c3fe-173">Classes used in</span></span>        | [<span data-ttu-id="2c3fe-174">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-174">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2c3fe-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2c3fe-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2c3fe-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c3fe-176">Entry</span></span> | <span data-ttu-id="2c3fe-177">Значение</span><span class="sxs-lookup"><span data-stu-id="2c3fe-177">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="2c3fe-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c3fe-178">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c3fe-179">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c3fe-180">System-Only</span></span>            | <span data-ttu-id="2c3fe-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-181">False</span></span>                                   |
| <span data-ttu-id="2c3fe-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c3fe-182">Is-Single-Valued</span></span>       | <span data-ttu-id="2c3fe-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-183">False</span></span>                                   |
| <span data-ttu-id="2c3fe-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c3fe-184">Is Indexed</span></span>             | <span data-ttu-id="2c3fe-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-185">False</span></span>                                   |
| <span data-ttu-id="2c3fe-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c3fe-186">In Global Catalog</span></span>      | <span data-ttu-id="2c3fe-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-187">False</span></span>                                   |
| <span data-ttu-id="2c3fe-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c3fe-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c3fe-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c3fe-189">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="2c3fe-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c3fe-190">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c3fe-191">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-192">Search-Flags</span></span>           | <span data-ttu-id="2c3fe-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c3fe-193">0x00000000</span></span>                              |
| <span data-ttu-id="2c3fe-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-194">System-Flags</span></span>           | <span data-ttu-id="2c3fe-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c3fe-195">0x00000010</span></span>                              |
| <span data-ttu-id="2c3fe-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c3fe-196">Classes used in</span></span>        | [<span data-ttu-id="2c3fe-197">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-197">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2c3fe-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c3fe-198">Windows Server 2008</span></span>



| <span data-ttu-id="2c3fe-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c3fe-199">Entry</span></span> | <span data-ttu-id="2c3fe-200">Значение</span><span class="sxs-lookup"><span data-stu-id="2c3fe-200">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="2c3fe-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c3fe-201">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c3fe-202">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c3fe-203">System-Only</span></span>            | <span data-ttu-id="2c3fe-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-204">False</span></span>                                   |
| <span data-ttu-id="2c3fe-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c3fe-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2c3fe-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-206">False</span></span>                                   |
| <span data-ttu-id="2c3fe-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c3fe-207">Is Indexed</span></span>             | <span data-ttu-id="2c3fe-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-208">False</span></span>                                   |
| <span data-ttu-id="2c3fe-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c3fe-209">In Global Catalog</span></span>      | <span data-ttu-id="2c3fe-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-210">False</span></span>                                   |
| <span data-ttu-id="2c3fe-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c3fe-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c3fe-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c3fe-212">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="2c3fe-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c3fe-213">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c3fe-214">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-215">Search-Flags</span></span>           | <span data-ttu-id="2c3fe-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c3fe-216">0x00000000</span></span>                              |
| <span data-ttu-id="2c3fe-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-217">System-Flags</span></span>           | <span data-ttu-id="2c3fe-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c3fe-218">0x00000010</span></span>                              |
| <span data-ttu-id="2c3fe-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c3fe-219">Classes used in</span></span>        | [<span data-ttu-id="2c3fe-220">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-220">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2c3fe-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2c3fe-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2c3fe-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c3fe-222">Entry</span></span> | <span data-ttu-id="2c3fe-223">Значение</span><span class="sxs-lookup"><span data-stu-id="2c3fe-223">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="2c3fe-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c3fe-224">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c3fe-225">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c3fe-226">System-Only</span></span>            | <span data-ttu-id="2c3fe-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-227">False</span></span>                                   |
| <span data-ttu-id="2c3fe-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c3fe-228">Is-Single-Valued</span></span>       | <span data-ttu-id="2c3fe-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-229">False</span></span>                                   |
| <span data-ttu-id="2c3fe-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c3fe-230">Is Indexed</span></span>             | <span data-ttu-id="2c3fe-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-231">False</span></span>                                   |
| <span data-ttu-id="2c3fe-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c3fe-232">In Global Catalog</span></span>      | <span data-ttu-id="2c3fe-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-233">False</span></span>                                   |
| <span data-ttu-id="2c3fe-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c3fe-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c3fe-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c3fe-235">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="2c3fe-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c3fe-236">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c3fe-237">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-238">Search-Flags</span></span>           | <span data-ttu-id="2c3fe-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c3fe-239">0x00000000</span></span>                              |
| <span data-ttu-id="2c3fe-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-240">System-Flags</span></span>           | <span data-ttu-id="2c3fe-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c3fe-241">0x00000010</span></span>                              |
| <span data-ttu-id="2c3fe-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c3fe-242">Classes used in</span></span>        | [<span data-ttu-id="2c3fe-243">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-243">**Meeting**</span></span>](c-meeting.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2c3fe-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c3fe-244">Windows Server 2012</span></span>



| <span data-ttu-id="2c3fe-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c3fe-245">Entry</span></span> | <span data-ttu-id="2c3fe-246">Значение</span><span class="sxs-lookup"><span data-stu-id="2c3fe-246">Value</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="2c3fe-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c3fe-247">Link-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c3fe-248">MAPI-Id</span></span>                | \-                                      |
| <span data-ttu-id="2c3fe-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c3fe-249">System-Only</span></span>            | <span data-ttu-id="2c3fe-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-250">False</span></span>                                   |
| <span data-ttu-id="2c3fe-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c3fe-251">Is-Single-Valued</span></span>       | <span data-ttu-id="2c3fe-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-252">False</span></span>                                   |
| <span data-ttu-id="2c3fe-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c3fe-253">Is Indexed</span></span>             | <span data-ttu-id="2c3fe-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-254">False</span></span>                                   |
| <span data-ttu-id="2c3fe-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c3fe-255">In Global Catalog</span></span>      | <span data-ttu-id="2c3fe-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c3fe-256">False</span></span>                                   |
| <span data-ttu-id="2c3fe-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c3fe-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c3fe-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c3fe-258">O:BAG:BAD:S:</span></span>                            |
| <span data-ttu-id="2c3fe-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c3fe-259">Range-Lower</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c3fe-260">Range-Upper</span></span>            | \-                                      |
| <span data-ttu-id="2c3fe-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-261">Search-Flags</span></span>           | <span data-ttu-id="2c3fe-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c3fe-262">0x00000000</span></span>                              |
| <span data-ttu-id="2c3fe-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c3fe-263">System-Flags</span></span>           | <span data-ttu-id="2c3fe-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c3fe-264">0x00000010</span></span>                              |
| <span data-ttu-id="2c3fe-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c3fe-265">Classes used in</span></span>        | [<span data-ttu-id="2c3fe-266">**Собрание**</span><span class="sxs-lookup"><span data-stu-id="2c3fe-266">**Meeting**</span></span>](c-meeting.md)<br/> |



 

 





