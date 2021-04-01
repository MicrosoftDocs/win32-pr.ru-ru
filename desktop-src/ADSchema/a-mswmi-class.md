---
title: атрибут класса MS-WMI-Class
description: Имя объекта класса WMI в связанной кодировке (например, Win32 \_ ComputerSystem). В качестве кодировки может использоваться экземпляр или объект класса.
ms.assetid: a0a4284e-3b52-4597-8656-df2f3297060d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута класса MS-WMI-Class
- Схема AD атрибута Мсвми-Class
topic_type:
- apiref
api_name:
- ms-WMI-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e69cd36fa4242203f0b36b8598d22bf96783b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138570"
---
# <a name="ms-wmi-class-attribute"></a><span data-ttu-id="5a043-106">атрибут класса MS-WMI-Class</span><span class="sxs-lookup"><span data-stu-id="5a043-106">ms-WMI-Class attribute</span></span>

<span data-ttu-id="5a043-107">Имя объекта класса WMI в связанной кодировке (например, Win32 \_ ComputerSystem).</span><span class="sxs-lookup"><span data-stu-id="5a043-107">The name of a WMI Class object in an associated encoding (for example, Win32\_ComputerSystem).</span></span> <span data-ttu-id="5a043-108">В качестве кодировки может использоваться экземпляр или объект класса.</span><span class="sxs-lookup"><span data-stu-id="5a043-108">The encoding can be either an instance or class object.</span></span>



| <span data-ttu-id="5a043-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="5a043-109">Entry</span></span> | <span data-ttu-id="5a043-110">Значение</span><span class="sxs-lookup"><span data-stu-id="5a043-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5a043-111">CN</span><span class="sxs-lookup"><span data-stu-id="5a043-111">CN</span></span>                | <span data-ttu-id="5a043-112">Класс MS-WMI-</span><span class="sxs-lookup"><span data-stu-id="5a043-112">ms-WMI-Class</span></span>                                                    |
| <span data-ttu-id="5a043-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5a043-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5a043-114">Класс Мсвми</span><span class="sxs-lookup"><span data-stu-id="5a043-114">msWMI-Class</span></span>                                                     |
| <span data-ttu-id="5a043-115">Размер</span><span class="sxs-lookup"><span data-stu-id="5a043-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="5a043-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5a043-116">Update Privilege</span></span>  | <span data-ttu-id="5a043-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="5a043-117">Domain administrator</span></span>                                            |
| <span data-ttu-id="5a043-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5a043-118">Update Frequency</span></span>  | <span data-ttu-id="5a043-119">Каждый раз при добавлении или изменении класса, содержащего атрибут.</span><span class="sxs-lookup"><span data-stu-id="5a043-119">Whenever a class containing the attribute is added or modified.</span></span> |
| <span data-ttu-id="5a043-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5a043-120">Attribute-Id</span></span>      | <span data-ttu-id="5a043-121">1.2.840.113556.1.4.1676</span><span class="sxs-lookup"><span data-stu-id="5a043-121">1.2.840.113556.1.4.1676</span></span>                                         |
| <span data-ttu-id="5a043-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5a043-122">System-Id-Guid</span></span>    | <span data-ttu-id="5a043-123">90c1925f-4a24-4b07-b202-be32eb3c8b74</span><span class="sxs-lookup"><span data-stu-id="5a043-123">90c1925f-4a24-4b07-b202-be32eb3c8b74</span></span>                            |
| <span data-ttu-id="5a043-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a043-124">Syntax</span></span>            | [<span data-ttu-id="5a043-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="5a043-125">**String(Unicode)**</span></span>](s-string-unicode.md)                     |



## <a name="implementations"></a><span data-ttu-id="5a043-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5a043-126">Implementations</span></span>

-   [<span data-ttu-id="5a043-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5a043-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5a043-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5a043-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5a043-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5a043-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5a043-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5a043-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5a043-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5a043-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5a043-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a043-132">Windows Server 2003</span></span>



| <span data-ttu-id="5a043-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="5a043-133">Entry</span></span> | <span data-ttu-id="5a043-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5a043-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5a043-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5a043-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a043-136">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a043-137">System-Only</span></span>            | <span data-ttu-id="5a043-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-138">False</span></span>                                                              |
| <span data-ttu-id="5a043-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5a043-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5a043-140">True</span><span class="sxs-lookup"><span data-stu-id="5a043-140">True</span></span>                                                               |
| <span data-ttu-id="5a043-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5a043-141">Is Indexed</span></span>             | <span data-ttu-id="5a043-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-142">False</span></span>                                                              |
| <span data-ttu-id="5a043-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5a043-143">In Global Catalog</span></span>      | <span data-ttu-id="5a043-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-144">False</span></span>                                                              |
| <span data-ttu-id="5a043-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5a043-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a043-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a043-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5a043-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a043-147">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a043-148">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-149">Search-Flags</span></span>           | <span data-ttu-id="5a043-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a043-150">0x00000000</span></span>                                                         |
| <span data-ttu-id="5a043-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-151">System-Flags</span></span>           | <span data-ttu-id="5a043-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a043-152">0x00000010</span></span>                                                         |
| <span data-ttu-id="5a043-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5a043-153">Classes used in</span></span>        | [<span data-ttu-id="5a043-154">**MS-WMI-Обжектенкодинг**</span><span class="sxs-lookup"><span data-stu-id="5a043-154">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5a043-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5a043-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5a043-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="5a043-156">Entry</span></span> | <span data-ttu-id="5a043-157">Значение</span><span class="sxs-lookup"><span data-stu-id="5a043-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5a043-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5a043-158">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a043-159">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a043-160">System-Only</span></span>            | <span data-ttu-id="5a043-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-161">False</span></span>                                                              |
| <span data-ttu-id="5a043-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5a043-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5a043-163">True</span><span class="sxs-lookup"><span data-stu-id="5a043-163">True</span></span>                                                               |
| <span data-ttu-id="5a043-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5a043-164">Is Indexed</span></span>             | <span data-ttu-id="5a043-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-165">False</span></span>                                                              |
| <span data-ttu-id="5a043-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5a043-166">In Global Catalog</span></span>      | <span data-ttu-id="5a043-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-167">False</span></span>                                                              |
| <span data-ttu-id="5a043-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5a043-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a043-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a043-169">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5a043-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a043-170">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a043-171">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-172">Search-Flags</span></span>           | <span data-ttu-id="5a043-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a043-173">0x00000000</span></span>                                                         |
| <span data-ttu-id="5a043-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-174">System-Flags</span></span>           | <span data-ttu-id="5a043-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a043-175">0x00000010</span></span>                                                         |
| <span data-ttu-id="5a043-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5a043-176">Classes used in</span></span>        | [<span data-ttu-id="5a043-177">**MS-WMI-Обжектенкодинг**</span><span class="sxs-lookup"><span data-stu-id="5a043-177">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5a043-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a043-178">Windows Server 2008</span></span>



| <span data-ttu-id="5a043-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="5a043-179">Entry</span></span> | <span data-ttu-id="5a043-180">Значение</span><span class="sxs-lookup"><span data-stu-id="5a043-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5a043-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5a043-181">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a043-182">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a043-183">System-Only</span></span>            | <span data-ttu-id="5a043-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-184">False</span></span>                                                              |
| <span data-ttu-id="5a043-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5a043-185">Is-Single-Valued</span></span>       | <span data-ttu-id="5a043-186">True</span><span class="sxs-lookup"><span data-stu-id="5a043-186">True</span></span>                                                               |
| <span data-ttu-id="5a043-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5a043-187">Is Indexed</span></span>             | <span data-ttu-id="5a043-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-188">False</span></span>                                                              |
| <span data-ttu-id="5a043-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5a043-189">In Global Catalog</span></span>      | <span data-ttu-id="5a043-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-190">False</span></span>                                                              |
| <span data-ttu-id="5a043-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5a043-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a043-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a043-192">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5a043-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a043-193">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a043-194">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-195">Search-Flags</span></span>           | <span data-ttu-id="5a043-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a043-196">0x00000000</span></span>                                                         |
| <span data-ttu-id="5a043-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-197">System-Flags</span></span>           | <span data-ttu-id="5a043-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a043-198">0x00000010</span></span>                                                         |
| <span data-ttu-id="5a043-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5a043-199">Classes used in</span></span>        | [<span data-ttu-id="5a043-200">**MS-WMI-Обжектенкодинг**</span><span class="sxs-lookup"><span data-stu-id="5a043-200">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5a043-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5a043-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5a043-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="5a043-202">Entry</span></span> | <span data-ttu-id="5a043-203">Значение</span><span class="sxs-lookup"><span data-stu-id="5a043-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5a043-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5a043-204">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a043-205">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a043-206">System-Only</span></span>            | <span data-ttu-id="5a043-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-207">False</span></span>                                                              |
| <span data-ttu-id="5a043-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5a043-208">Is-Single-Valued</span></span>       | <span data-ttu-id="5a043-209">True</span><span class="sxs-lookup"><span data-stu-id="5a043-209">True</span></span>                                                               |
| <span data-ttu-id="5a043-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5a043-210">Is Indexed</span></span>             | <span data-ttu-id="5a043-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-211">False</span></span>                                                              |
| <span data-ttu-id="5a043-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5a043-212">In Global Catalog</span></span>      | <span data-ttu-id="5a043-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-213">False</span></span>                                                              |
| <span data-ttu-id="5a043-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5a043-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a043-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a043-215">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5a043-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a043-216">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a043-217">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-218">Search-Flags</span></span>           | <span data-ttu-id="5a043-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a043-219">0x00000000</span></span>                                                         |
| <span data-ttu-id="5a043-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-220">System-Flags</span></span>           | <span data-ttu-id="5a043-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a043-221">0x00000010</span></span>                                                         |
| <span data-ttu-id="5a043-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5a043-222">Classes used in</span></span>        | [<span data-ttu-id="5a043-223">**MS-WMI-Обжектенкодинг**</span><span class="sxs-lookup"><span data-stu-id="5a043-223">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5a043-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a043-224">Windows Server 2012</span></span>



| <span data-ttu-id="5a043-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="5a043-225">Entry</span></span> | <span data-ttu-id="5a043-226">Значение</span><span class="sxs-lookup"><span data-stu-id="5a043-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="5a043-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5a043-227">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5a043-228">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="5a043-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="5a043-229">System-Only</span></span>            | <span data-ttu-id="5a043-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-230">False</span></span>                                                              |
| <span data-ttu-id="5a043-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5a043-231">Is-Single-Valued</span></span>       | <span data-ttu-id="5a043-232">True</span><span class="sxs-lookup"><span data-stu-id="5a043-232">True</span></span>                                                               |
| <span data-ttu-id="5a043-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5a043-233">Is Indexed</span></span>             | <span data-ttu-id="5a043-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-234">False</span></span>                                                              |
| <span data-ttu-id="5a043-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5a043-235">In Global Catalog</span></span>      | <span data-ttu-id="5a043-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="5a043-236">False</span></span>                                                              |
| <span data-ttu-id="5a043-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5a043-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="5a043-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5a043-238">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="5a043-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5a043-239">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5a043-240">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="5a043-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-241">Search-Flags</span></span>           | <span data-ttu-id="5a043-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5a043-242">0x00000000</span></span>                                                         |
| <span data-ttu-id="5a043-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5a043-243">System-Flags</span></span>           | <span data-ttu-id="5a043-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5a043-244">0x00000010</span></span>                                                         |
| <span data-ttu-id="5a043-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5a043-245">Classes used in</span></span>        | [<span data-ttu-id="5a043-246">**MS-WMI-Обжектенкодинг**</span><span class="sxs-lookup"><span data-stu-id="5a043-246">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



 

 





