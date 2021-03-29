---
title: Атрибут SID-History
description: Содержит предыдущие идентификаторы безопасности, используемые для объекта, если объект был перемещен из другого домена.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута SID-History
- Схема AD атрибута sIDHistory
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493692"
---
# <a name="sid-history-attribute"></a><span data-ttu-id="9bb58-105">Атрибут SID-History</span><span class="sxs-lookup"><span data-stu-id="9bb58-105">SID-History attribute</span></span>

<span data-ttu-id="9bb58-106">Содержит предыдущие идентификаторы безопасности, используемые для объекта, если объект был перемещен из другого домена.</span><span class="sxs-lookup"><span data-stu-id="9bb58-106">Contains previous SIDs used for the object if the object was moved from another domain.</span></span> <span data-ttu-id="9bb58-107">Каждый раз, когда объект перемещается из одного домена в другой, создается новый идентификатор безопасности, а новый идентификатор SID становится objectSID.</span><span class="sxs-lookup"><span data-stu-id="9bb58-107">Whenever an object is moved from one domain to another, a new SID is created and that new SID becomes the objectSID.</span></span> <span data-ttu-id="9bb58-108">Предыдущий идентификатор безопасности добавляется в свойство sIDHistory.</span><span class="sxs-lookup"><span data-stu-id="9bb58-108">The previous SID is added to the sIDHistory property.</span></span>



| <span data-ttu-id="9bb58-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="9bb58-109">Entry</span></span> | <span data-ttu-id="9bb58-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9bb58-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="9bb58-111">CN</span><span class="sxs-lookup"><span data-stu-id="9bb58-111">CN</span></span>                | <span data-ttu-id="9bb58-112">SID-History</span><span class="sxs-lookup"><span data-stu-id="9bb58-112">SID-History</span></span>                                    |
| <span data-ttu-id="9bb58-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9bb58-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9bb58-114">Лесами</span><span class="sxs-lookup"><span data-stu-id="9bb58-114">sIDHistory</span></span>                                     |
| <span data-ttu-id="9bb58-115">Размер</span><span class="sxs-lookup"><span data-stu-id="9bb58-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="9bb58-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9bb58-116">Update Privilege</span></span>  | <span data-ttu-id="9bb58-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="9bb58-117">This value is set by the system.</span></span>               |
| <span data-ttu-id="9bb58-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9bb58-118">Update Frequency</span></span>  | <span data-ttu-id="9bb58-119">Каждый раз при перемещении объекта в новый домен.</span><span class="sxs-lookup"><span data-stu-id="9bb58-119">Each time the object is moved to a new domain.</span></span> |
| <span data-ttu-id="9bb58-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9bb58-120">Attribute-Id</span></span>      | <span data-ttu-id="9bb58-121">1.2.840.113556.1.4.609</span><span class="sxs-lookup"><span data-stu-id="9bb58-121">1.2.840.113556.1.4.609</span></span>                         |
| <span data-ttu-id="9bb58-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9bb58-122">System-Id-Guid</span></span>    | <span data-ttu-id="9bb58-123">17eb4278-d167-11d0-b002-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9bb58-123">17eb4278-d167-11d0-b002-0000f80367c1</span></span>           |
| <span data-ttu-id="9bb58-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bb58-124">Syntax</span></span>            | [<span data-ttu-id="9bb58-125">**Строка (SID)**</span><span class="sxs-lookup"><span data-stu-id="9bb58-125">**String(Sid)**</span></span>](s-string-sid.md)            |



## <a name="implementations"></a><span data-ttu-id="9bb58-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9bb58-126">Implementations</span></span>

-   [<span data-ttu-id="9bb58-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9bb58-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9bb58-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9bb58-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9bb58-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9bb58-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9bb58-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9bb58-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9bb58-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9bb58-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9bb58-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9bb58-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9bb58-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9bb58-133">Windows 2000 Server</span></span>



| <span data-ttu-id="9bb58-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="9bb58-134">Entry</span></span> | <span data-ttu-id="9bb58-135">Значение</span><span class="sxs-lookup"><span data-stu-id="9bb58-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9bb58-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9bb58-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bb58-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bb58-138">System-Only</span></span>            | <span data-ttu-id="9bb58-139">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-139">True</span></span>                                                         |
| <span data-ttu-id="9bb58-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9bb58-140">Is-Single-Valued</span></span>       | <span data-ttu-id="9bb58-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-141">False</span></span>                                                        |
| <span data-ttu-id="9bb58-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9bb58-142">Is Indexed</span></span>             | <span data-ttu-id="9bb58-143">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-143">True</span></span>                                                         |
| <span data-ttu-id="9bb58-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9bb58-144">In Global Catalog</span></span>      | <span data-ttu-id="9bb58-145">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-145">True</span></span>                                                         |
| <span data-ttu-id="9bb58-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9bb58-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bb58-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9bb58-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9bb58-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bb58-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bb58-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-150">Search-Flags</span></span>           | <span data-ttu-id="9bb58-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bb58-151">0x00000001</span></span>                                                   |
| <span data-ttu-id="9bb58-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-152">System-Flags</span></span>           | <span data-ttu-id="9bb58-153">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9bb58-153">0x00000012</span></span>                                                   |
| <span data-ttu-id="9bb58-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9bb58-154">Classes used in</span></span>        | [<span data-ttu-id="9bb58-155">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="9bb58-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9bb58-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9bb58-156">Windows Server 2003</span></span>



| <span data-ttu-id="9bb58-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="9bb58-157">Entry</span></span> | <span data-ttu-id="9bb58-158">Значение</span><span class="sxs-lookup"><span data-stu-id="9bb58-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9bb58-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9bb58-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bb58-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bb58-161">System-Only</span></span>            | <span data-ttu-id="9bb58-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-162">False</span></span>                                                        |
| <span data-ttu-id="9bb58-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9bb58-163">Is-Single-Valued</span></span>       | <span data-ttu-id="9bb58-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-164">False</span></span>                                                        |
| <span data-ttu-id="9bb58-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9bb58-165">Is Indexed</span></span>             | <span data-ttu-id="9bb58-166">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-166">True</span></span>                                                         |
| <span data-ttu-id="9bb58-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9bb58-167">In Global Catalog</span></span>      | <span data-ttu-id="9bb58-168">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-168">True</span></span>                                                         |
| <span data-ttu-id="9bb58-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9bb58-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bb58-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9bb58-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9bb58-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bb58-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bb58-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-173">Search-Flags</span></span>           | <span data-ttu-id="9bb58-174">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bb58-174">0x00000001</span></span>                                                   |
| <span data-ttu-id="9bb58-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-175">System-Flags</span></span>           | <span data-ttu-id="9bb58-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9bb58-176">0x00000012</span></span>                                                   |
| <span data-ttu-id="9bb58-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9bb58-177">Classes used in</span></span>        | [<span data-ttu-id="9bb58-178">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="9bb58-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9bb58-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9bb58-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9bb58-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="9bb58-180">Entry</span></span> | <span data-ttu-id="9bb58-181">Значение</span><span class="sxs-lookup"><span data-stu-id="9bb58-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9bb58-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9bb58-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bb58-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bb58-184">System-Only</span></span>            | <span data-ttu-id="9bb58-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-185">False</span></span>                                                        |
| <span data-ttu-id="9bb58-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9bb58-186">Is-Single-Valued</span></span>       | <span data-ttu-id="9bb58-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-187">False</span></span>                                                        |
| <span data-ttu-id="9bb58-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9bb58-188">Is Indexed</span></span>             | <span data-ttu-id="9bb58-189">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-189">True</span></span>                                                         |
| <span data-ttu-id="9bb58-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9bb58-190">In Global Catalog</span></span>      | <span data-ttu-id="9bb58-191">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-191">True</span></span>                                                         |
| <span data-ttu-id="9bb58-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9bb58-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bb58-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9bb58-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9bb58-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bb58-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bb58-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-196">Search-Flags</span></span>           | <span data-ttu-id="9bb58-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bb58-197">0x00000001</span></span>                                                   |
| <span data-ttu-id="9bb58-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-198">System-Flags</span></span>           | <span data-ttu-id="9bb58-199">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9bb58-199">0x00000012</span></span>                                                   |
| <span data-ttu-id="9bb58-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9bb58-200">Classes used in</span></span>        | [<span data-ttu-id="9bb58-201">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="9bb58-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9bb58-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bb58-202">Windows Server 2008</span></span>



| <span data-ttu-id="9bb58-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="9bb58-203">Entry</span></span> | <span data-ttu-id="9bb58-204">Значение</span><span class="sxs-lookup"><span data-stu-id="9bb58-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9bb58-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9bb58-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bb58-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bb58-207">System-Only</span></span>            | <span data-ttu-id="9bb58-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-208">False</span></span>                                                        |
| <span data-ttu-id="9bb58-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9bb58-209">Is-Single-Valued</span></span>       | <span data-ttu-id="9bb58-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-210">False</span></span>                                                        |
| <span data-ttu-id="9bb58-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9bb58-211">Is Indexed</span></span>             | <span data-ttu-id="9bb58-212">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-212">True</span></span>                                                         |
| <span data-ttu-id="9bb58-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9bb58-213">In Global Catalog</span></span>      | <span data-ttu-id="9bb58-214">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-214">True</span></span>                                                         |
| <span data-ttu-id="9bb58-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9bb58-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bb58-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9bb58-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9bb58-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bb58-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bb58-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-219">Search-Flags</span></span>           | <span data-ttu-id="9bb58-220">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bb58-220">0x00000001</span></span>                                                   |
| <span data-ttu-id="9bb58-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-221">System-Flags</span></span>           | <span data-ttu-id="9bb58-222">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9bb58-222">0x00000012</span></span>                                                   |
| <span data-ttu-id="9bb58-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9bb58-223">Classes used in</span></span>        | [<span data-ttu-id="9bb58-224">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="9bb58-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9bb58-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9bb58-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9bb58-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="9bb58-226">Entry</span></span> | <span data-ttu-id="9bb58-227">Значение</span><span class="sxs-lookup"><span data-stu-id="9bb58-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9bb58-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9bb58-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bb58-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bb58-230">System-Only</span></span>            | <span data-ttu-id="9bb58-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-231">False</span></span>                                                        |
| <span data-ttu-id="9bb58-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9bb58-232">Is-Single-Valued</span></span>       | <span data-ttu-id="9bb58-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-233">False</span></span>                                                        |
| <span data-ttu-id="9bb58-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9bb58-234">Is Indexed</span></span>             | <span data-ttu-id="9bb58-235">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-235">True</span></span>                                                         |
| <span data-ttu-id="9bb58-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9bb58-236">In Global Catalog</span></span>      | <span data-ttu-id="9bb58-237">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-237">True</span></span>                                                         |
| <span data-ttu-id="9bb58-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9bb58-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bb58-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9bb58-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9bb58-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bb58-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bb58-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-242">Search-Flags</span></span>           | <span data-ttu-id="9bb58-243">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bb58-243">0x00000001</span></span>                                                   |
| <span data-ttu-id="9bb58-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-244">System-Flags</span></span>           | <span data-ttu-id="9bb58-245">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9bb58-245">0x00000012</span></span>                                                   |
| <span data-ttu-id="9bb58-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9bb58-246">Classes used in</span></span>        | [<span data-ttu-id="9bb58-247">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="9bb58-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9bb58-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9bb58-248">Windows Server 2012</span></span>



| <span data-ttu-id="9bb58-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="9bb58-249">Entry</span></span> | <span data-ttu-id="9bb58-250">Значение</span><span class="sxs-lookup"><span data-stu-id="9bb58-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9bb58-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9bb58-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9bb58-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="9bb58-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="9bb58-253">System-Only</span></span>            | <span data-ttu-id="9bb58-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-254">False</span></span>                                                        |
| <span data-ttu-id="9bb58-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9bb58-255">Is-Single-Valued</span></span>       | <span data-ttu-id="9bb58-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="9bb58-256">False</span></span>                                                        |
| <span data-ttu-id="9bb58-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9bb58-257">Is Indexed</span></span>             | <span data-ttu-id="9bb58-258">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-258">True</span></span>                                                         |
| <span data-ttu-id="9bb58-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9bb58-259">In Global Catalog</span></span>      | <span data-ttu-id="9bb58-260">True</span><span class="sxs-lookup"><span data-stu-id="9bb58-260">True</span></span>                                                         |
| <span data-ttu-id="9bb58-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9bb58-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="9bb58-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9bb58-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="9bb58-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9bb58-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9bb58-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="9bb58-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-265">Search-Flags</span></span>           | <span data-ttu-id="9bb58-266">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9bb58-266">0x00000001</span></span>                                                   |
| <span data-ttu-id="9bb58-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9bb58-267">System-Flags</span></span>           | <span data-ttu-id="9bb58-268">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9bb58-268">0x00000012</span></span>                                                   |
| <span data-ttu-id="9bb58-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9bb58-269">Classes used in</span></span>        | [<span data-ttu-id="9bb58-270">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="9bb58-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





