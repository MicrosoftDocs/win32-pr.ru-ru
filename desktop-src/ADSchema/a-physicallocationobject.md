---
title: Атрибут физического расположения — объект
description: Используется для подключения устройства (например, принтера, компьютера и т. д.) к физическому расположению.
ms.assetid: 1055d278-a4fc-47a3-b59f-9d63be39a5e7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута физического расположения объекта
- Схема AD атрибута Фисикаллокатионобжект
topic_type:
- apiref
api_name:
- Physical-Location-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce247ec2a73d8644497ce152402f4ad08b8bb7f5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535918"
---
# <a name="physical-location-object-attribute"></a><span data-ttu-id="b45c8-105">Атрибут физического расположения — объект</span><span class="sxs-lookup"><span data-stu-id="b45c8-105">Physical-Location-Object attribute</span></span>

<span data-ttu-id="b45c8-106">Используется для подключения устройства (например, принтера, компьютера и т. д.) к физическому расположению.</span><span class="sxs-lookup"><span data-stu-id="b45c8-106">Used to map a device (for example, a printer, computer, and so on) to a physical location.</span></span>



| <span data-ttu-id="b45c8-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b45c8-107">Entry</span></span> | <span data-ttu-id="b45c8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b45c8-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b45c8-109">CN</span><span class="sxs-lookup"><span data-stu-id="b45c8-109">CN</span></span>                | <span data-ttu-id="b45c8-110">Физическое расположение — объект</span><span class="sxs-lookup"><span data-stu-id="b45c8-110">Physical-Location-Object</span></span>                |
| <span data-ttu-id="b45c8-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b45c8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b45c8-112">physicalLocationObject</span><span class="sxs-lookup"><span data-stu-id="b45c8-112">physicalLocationObject</span></span>                  |
| <span data-ttu-id="b45c8-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b45c8-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="b45c8-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b45c8-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="b45c8-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b45c8-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="b45c8-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b45c8-116">Attribute-Id</span></span>      | <span data-ttu-id="b45c8-117">1.2.840.113556.1.4.514</span><span class="sxs-lookup"><span data-stu-id="b45c8-117">1.2.840.113556.1.4.514</span></span>                  |
| <span data-ttu-id="b45c8-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b45c8-118">System-Id-Guid</span></span>    | <span data-ttu-id="b45c8-119">b7b13119-b82e-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b45c8-119">b7b13119-b82e-11d0-afee-0000f80367c1</span></span>    |
| <span data-ttu-id="b45c8-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b45c8-120">Syntax</span></span>            | [<span data-ttu-id="b45c8-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b45c8-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="b45c8-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b45c8-122">Implementations</span></span>

-   [<span data-ttu-id="b45c8-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b45c8-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b45c8-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b45c8-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b45c8-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b45c8-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b45c8-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b45c8-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b45c8-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b45c8-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b45c8-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b45c8-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b45c8-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b45c8-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b45c8-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="b45c8-130">Entry</span></span> | <span data-ttu-id="b45c8-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b45c8-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45c8-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b45c8-132">Link-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b45c8-133">MAPI-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b45c8-134">System-Only</span></span>            | <span data-ttu-id="b45c8-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-135">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b45c8-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b45c8-137">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-137">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b45c8-138">Is Indexed</span></span>             | <span data-ttu-id="b45c8-139">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-139">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b45c8-140">In Global Catalog</span></span>      | <span data-ttu-id="b45c8-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-141">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b45c8-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b45c8-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b45c8-143">O:BAG:BAD:S:</span></span>                                                                                                                   |
| <span data-ttu-id="b45c8-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b45c8-144">Range-Lower</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b45c8-145">Range-Upper</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-146">Search-Flags</span></span>           | <span data-ttu-id="b45c8-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b45c8-147">0x00000001</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-148">System-Flags</span></span>           | <span data-ttu-id="b45c8-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b45c8-149">0x00000010</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b45c8-150">Classes used in</span></span>        | [<span data-ttu-id="b45c8-151">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="b45c8-151">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b45c8-152">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b45c8-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> [<span data-ttu-id="b45c8-153">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="b45c8-153">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b45c8-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b45c8-154">Windows Server 2003</span></span>



| <span data-ttu-id="b45c8-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="b45c8-155">Entry</span></span> | <span data-ttu-id="b45c8-156">Значение</span><span class="sxs-lookup"><span data-stu-id="b45c8-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45c8-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b45c8-157">Link-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b45c8-158">MAPI-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b45c8-159">System-Only</span></span>            | <span data-ttu-id="b45c8-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-160">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b45c8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b45c8-162">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-162">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b45c8-163">Is Indexed</span></span>             | <span data-ttu-id="b45c8-164">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-164">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b45c8-165">In Global Catalog</span></span>      | <span data-ttu-id="b45c8-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-166">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b45c8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b45c8-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b45c8-168">O:BAG:BAD:S:</span></span>                                                                                                                   |
| <span data-ttu-id="b45c8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b45c8-169">Range-Lower</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b45c8-170">Range-Upper</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-171">Search-Flags</span></span>           | <span data-ttu-id="b45c8-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b45c8-172">0x00000001</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-173">System-Flags</span></span>           | <span data-ttu-id="b45c8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b45c8-174">0x00000010</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b45c8-175">Classes used in</span></span>        | [<span data-ttu-id="b45c8-176">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="b45c8-176">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b45c8-177">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b45c8-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> [<span data-ttu-id="b45c8-178">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="b45c8-178">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b45c8-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b45c8-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b45c8-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="b45c8-180">Entry</span></span> | <span data-ttu-id="b45c8-181">Значение</span><span class="sxs-lookup"><span data-stu-id="b45c8-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45c8-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b45c8-182">Link-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b45c8-183">MAPI-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b45c8-184">System-Only</span></span>            | <span data-ttu-id="b45c8-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-185">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b45c8-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b45c8-187">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-187">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b45c8-188">Is Indexed</span></span>             | <span data-ttu-id="b45c8-189">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-189">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b45c8-190">In Global Catalog</span></span>      | <span data-ttu-id="b45c8-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-191">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b45c8-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b45c8-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b45c8-193">O:BAG:BAD:S:</span></span>                                                                                                                   |
| <span data-ttu-id="b45c8-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b45c8-194">Range-Lower</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b45c8-195">Range-Upper</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-196">Search-Flags</span></span>           | <span data-ttu-id="b45c8-197">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b45c8-197">0x00000001</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-198">System-Flags</span></span>           | <span data-ttu-id="b45c8-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b45c8-199">0x00000010</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b45c8-200">Classes used in</span></span>        | [<span data-ttu-id="b45c8-201">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="b45c8-201">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b45c8-202">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b45c8-202">**Print-Queue**</span></span>](c-printqueue.md)<br/> [<span data-ttu-id="b45c8-203">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="b45c8-203">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b45c8-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b45c8-204">Windows Server 2008</span></span>



| <span data-ttu-id="b45c8-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="b45c8-205">Entry</span></span> | <span data-ttu-id="b45c8-206">Значение</span><span class="sxs-lookup"><span data-stu-id="b45c8-206">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45c8-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b45c8-207">Link-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b45c8-208">MAPI-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="b45c8-209">System-Only</span></span>            | <span data-ttu-id="b45c8-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-210">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b45c8-211">Is-Single-Valued</span></span>       | <span data-ttu-id="b45c8-212">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-212">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b45c8-213">Is Indexed</span></span>             | <span data-ttu-id="b45c8-214">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-214">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b45c8-215">In Global Catalog</span></span>      | <span data-ttu-id="b45c8-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-216">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b45c8-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="b45c8-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b45c8-218">O:BAG:BAD:S:</span></span>                                                                                                                   |
| <span data-ttu-id="b45c8-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b45c8-219">Range-Lower</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b45c8-220">Range-Upper</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-221">Search-Flags</span></span>           | <span data-ttu-id="b45c8-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b45c8-222">0x00000001</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-223">System-Flags</span></span>           | <span data-ttu-id="b45c8-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b45c8-224">0x00000010</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b45c8-225">Classes used in</span></span>        | [<span data-ttu-id="b45c8-226">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="b45c8-226">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b45c8-227">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b45c8-227">**Print-Queue**</span></span>](c-printqueue.md)<br/> [<span data-ttu-id="b45c8-228">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="b45c8-228">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b45c8-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b45c8-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b45c8-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="b45c8-230">Entry</span></span> | <span data-ttu-id="b45c8-231">Значение</span><span class="sxs-lookup"><span data-stu-id="b45c8-231">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45c8-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b45c8-232">Link-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b45c8-233">MAPI-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="b45c8-234">System-Only</span></span>            | <span data-ttu-id="b45c8-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-235">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b45c8-236">Is-Single-Valued</span></span>       | <span data-ttu-id="b45c8-237">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-237">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b45c8-238">Is Indexed</span></span>             | <span data-ttu-id="b45c8-239">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-239">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b45c8-240">In Global Catalog</span></span>      | <span data-ttu-id="b45c8-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-241">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b45c8-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="b45c8-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b45c8-243">O:BAG:BAD:S:</span></span>                                                                                                                   |
| <span data-ttu-id="b45c8-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b45c8-244">Range-Lower</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b45c8-245">Range-Upper</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-246">Search-Flags</span></span>           | <span data-ttu-id="b45c8-247">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b45c8-247">0x00000001</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-248">System-Flags</span></span>           | <span data-ttu-id="b45c8-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b45c8-249">0x00000010</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b45c8-250">Classes used in</span></span>        | [<span data-ttu-id="b45c8-251">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="b45c8-251">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b45c8-252">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b45c8-252">**Print-Queue**</span></span>](c-printqueue.md)<br/> [<span data-ttu-id="b45c8-253">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="b45c8-253">**Subnet**</span></span>](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b45c8-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b45c8-254">Windows Server 2012</span></span>



| <span data-ttu-id="b45c8-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="b45c8-255">Entry</span></span> | <span data-ttu-id="b45c8-256">Значение</span><span class="sxs-lookup"><span data-stu-id="b45c8-256">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45c8-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b45c8-257">Link-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b45c8-258">MAPI-Id</span></span>                | \-                                                                                                                             |
| <span data-ttu-id="b45c8-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b45c8-259">System-Only</span></span>            | <span data-ttu-id="b45c8-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-260">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b45c8-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b45c8-262">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-262">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b45c8-263">Is Indexed</span></span>             | <span data-ttu-id="b45c8-264">True</span><span class="sxs-lookup"><span data-stu-id="b45c8-264">True</span></span>                                                                                                                           |
| <span data-ttu-id="b45c8-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b45c8-265">In Global Catalog</span></span>      | <span data-ttu-id="b45c8-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="b45c8-266">False</span></span>                                                                                                                          |
| <span data-ttu-id="b45c8-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b45c8-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b45c8-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b45c8-268">O:BAG:BAD:S:</span></span>                                                                                                                   |
| <span data-ttu-id="b45c8-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b45c8-269">Range-Lower</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b45c8-270">Range-Upper</span></span>            | \-                                                                                                                             |
| <span data-ttu-id="b45c8-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-271">Search-Flags</span></span>           | <span data-ttu-id="b45c8-272">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b45c8-272">0x00000001</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b45c8-273">System-Flags</span></span>           | <span data-ttu-id="b45c8-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b45c8-274">0x00000010</span></span>                                                                                                                     |
| <span data-ttu-id="b45c8-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b45c8-275">Classes used in</span></span>        | [<span data-ttu-id="b45c8-276">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="b45c8-276">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="b45c8-277">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="b45c8-277">**Print-Queue**</span></span>](c-printqueue.md)<br/> [<span data-ttu-id="b45c8-278">**Подсеть**</span><span class="sxs-lookup"><span data-stu-id="b45c8-278">**Subnet**</span></span>](c-subnet.md)<br/> |



 

 





