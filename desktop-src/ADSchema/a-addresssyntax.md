---
title: Атрибут Address-Syntax
description: Грамматика для кодирования свойств отображаемой таблицы в виде строки.
ms.assetid: 809981da-8572-4a9f-a4c3-06cff95c8bdc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Address-Syntax
- Схема AD атрибута Аддресссинтакс
topic_type:
- apiref
api_name:
- Address-Syntax
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db7ae0a0d5a4672168329b546dd53c19697eec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654990"
---
# <a name="address-syntax-attribute"></a><span data-ttu-id="ef0d2-105">Атрибут Address-Syntax</span><span class="sxs-lookup"><span data-stu-id="ef0d2-105">Address-Syntax attribute</span></span>

<span data-ttu-id="ef0d2-106">Грамматика для кодирования свойств отображаемой таблицы в виде строки.</span><span class="sxs-lookup"><span data-stu-id="ef0d2-106">A grammar for encoding the display table properties as a string.</span></span>



| <span data-ttu-id="ef0d2-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ef0d2-107">Entry</span></span> | <span data-ttu-id="ef0d2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ef0d2-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ef0d2-109">CN</span><span class="sxs-lookup"><span data-stu-id="ef0d2-109">CN</span></span>                | <span data-ttu-id="ef0d2-110">Address-Syntax</span><span class="sxs-lookup"><span data-stu-id="ef0d2-110">Address-Syntax</span></span>                                        |
| <span data-ttu-id="ef0d2-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ef0d2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ef0d2-112">аддресссинтакс</span><span class="sxs-lookup"><span data-stu-id="ef0d2-112">addressSyntax</span></span>                                         |
| <span data-ttu-id="ef0d2-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ef0d2-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ef0d2-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ef0d2-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ef0d2-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ef0d2-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ef0d2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ef0d2-116">Attribute-Id</span></span>      | <span data-ttu-id="ef0d2-117">1.2.840.113556.1.2.255</span><span class="sxs-lookup"><span data-stu-id="ef0d2-117">1.2.840.113556.1.2.255</span></span>                                |
| <span data-ttu-id="ef0d2-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ef0d2-118">System-Id-Guid</span></span>    | <span data-ttu-id="ef0d2-119">5fd42463-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="ef0d2-119">5fd42463-1262-11d0-a060-00aa006c33ed</span></span>                  |
| <span data-ttu-id="ef0d2-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef0d2-120">Syntax</span></span>            | [<span data-ttu-id="ef0d2-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ef0d2-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ef0d2-122">Implementations</span></span>

-   [<span data-ttu-id="ef0d2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ef0d2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ef0d2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ef0d2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ef0d2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ef0d2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ef0d2-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef0d2-129">Windows 2000 Server</span></span>



| <span data-ttu-id="ef0d2-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="ef0d2-130">Entry</span></span> | <span data-ttu-id="ef0d2-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ef0d2-131">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef0d2-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ef0d2-132">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef0d2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef0d2-133">MAPI-Id</span></span>                | <span data-ttu-id="ef0d2-134">0x8018</span><span class="sxs-lookup"><span data-stu-id="ef0d2-134">0x8018</span></span>                                                   |
| <span data-ttu-id="ef0d2-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef0d2-135">System-Only</span></span>            | <span data-ttu-id="ef0d2-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-136">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ef0d2-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ef0d2-138">True</span><span class="sxs-lookup"><span data-stu-id="ef0d2-138">True</span></span>                                                     |
| <span data-ttu-id="ef0d2-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ef0d2-139">Is Indexed</span></span>             | <span data-ttu-id="ef0d2-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-140">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ef0d2-141">In Global Catalog</span></span>      | <span data-ttu-id="ef0d2-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-142">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ef0d2-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef0d2-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ef0d2-144">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef0d2-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef0d2-145">Range-Lower</span></span>            | <span data-ttu-id="ef0d2-146">1</span><span class="sxs-lookup"><span data-stu-id="ef0d2-146">1</span></span>                                                        |
| <span data-ttu-id="ef0d2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef0d2-147">Range-Upper</span></span>            | <span data-ttu-id="ef0d2-148">4096</span><span class="sxs-lookup"><span data-stu-id="ef0d2-148">4096</span></span>                                                     |
| <span data-ttu-id="ef0d2-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-149">Search-Flags</span></span>           | <span data-ttu-id="ef0d2-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef0d2-150">0x00000000</span></span>                                               |
| <span data-ttu-id="ef0d2-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-151">System-Flags</span></span>           | <span data-ttu-id="ef0d2-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef0d2-152">0x00000010</span></span>                                               |
| <span data-ttu-id="ef0d2-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ef0d2-153">Classes used in</span></span>        | [<span data-ttu-id="ef0d2-154">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-154">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ef0d2-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef0d2-155">Windows Server 2003</span></span>



| <span data-ttu-id="ef0d2-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="ef0d2-156">Entry</span></span> | <span data-ttu-id="ef0d2-157">Значение</span><span class="sxs-lookup"><span data-stu-id="ef0d2-157">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef0d2-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ef0d2-158">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef0d2-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef0d2-159">MAPI-Id</span></span>                | <span data-ttu-id="ef0d2-160">0x8018</span><span class="sxs-lookup"><span data-stu-id="ef0d2-160">0x8018</span></span>                                                   |
| <span data-ttu-id="ef0d2-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef0d2-161">System-Only</span></span>            | <span data-ttu-id="ef0d2-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-162">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ef0d2-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ef0d2-164">True</span><span class="sxs-lookup"><span data-stu-id="ef0d2-164">True</span></span>                                                     |
| <span data-ttu-id="ef0d2-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ef0d2-165">Is Indexed</span></span>             | <span data-ttu-id="ef0d2-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-166">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ef0d2-167">In Global Catalog</span></span>      | <span data-ttu-id="ef0d2-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-168">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ef0d2-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef0d2-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ef0d2-170">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef0d2-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef0d2-171">Range-Lower</span></span>            | <span data-ttu-id="ef0d2-172">1</span><span class="sxs-lookup"><span data-stu-id="ef0d2-172">1</span></span>                                                        |
| <span data-ttu-id="ef0d2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef0d2-173">Range-Upper</span></span>            | <span data-ttu-id="ef0d2-174">4096</span><span class="sxs-lookup"><span data-stu-id="ef0d2-174">4096</span></span>                                                     |
| <span data-ttu-id="ef0d2-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-175">Search-Flags</span></span>           | <span data-ttu-id="ef0d2-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef0d2-176">0x00000000</span></span>                                               |
| <span data-ttu-id="ef0d2-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-177">System-Flags</span></span>           | <span data-ttu-id="ef0d2-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef0d2-178">0x00000010</span></span>                                               |
| <span data-ttu-id="ef0d2-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ef0d2-179">Classes used in</span></span>        | [<span data-ttu-id="ef0d2-180">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-180">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ef0d2-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ef0d2-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ef0d2-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="ef0d2-182">Entry</span></span> | <span data-ttu-id="ef0d2-183">Значение</span><span class="sxs-lookup"><span data-stu-id="ef0d2-183">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef0d2-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ef0d2-184">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef0d2-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef0d2-185">MAPI-Id</span></span>                | <span data-ttu-id="ef0d2-186">0x8018</span><span class="sxs-lookup"><span data-stu-id="ef0d2-186">0x8018</span></span>                                                   |
| <span data-ttu-id="ef0d2-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef0d2-187">System-Only</span></span>            | <span data-ttu-id="ef0d2-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-188">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ef0d2-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ef0d2-190">True</span><span class="sxs-lookup"><span data-stu-id="ef0d2-190">True</span></span>                                                     |
| <span data-ttu-id="ef0d2-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ef0d2-191">Is Indexed</span></span>             | <span data-ttu-id="ef0d2-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-192">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ef0d2-193">In Global Catalog</span></span>      | <span data-ttu-id="ef0d2-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-194">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ef0d2-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef0d2-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ef0d2-196">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef0d2-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef0d2-197">Range-Lower</span></span>            | <span data-ttu-id="ef0d2-198">1</span><span class="sxs-lookup"><span data-stu-id="ef0d2-198">1</span></span>                                                        |
| <span data-ttu-id="ef0d2-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef0d2-199">Range-Upper</span></span>            | <span data-ttu-id="ef0d2-200">4096</span><span class="sxs-lookup"><span data-stu-id="ef0d2-200">4096</span></span>                                                     |
| <span data-ttu-id="ef0d2-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-201">Search-Flags</span></span>           | <span data-ttu-id="ef0d2-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef0d2-202">0x00000000</span></span>                                               |
| <span data-ttu-id="ef0d2-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-203">System-Flags</span></span>           | <span data-ttu-id="ef0d2-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef0d2-204">0x00000010</span></span>                                               |
| <span data-ttu-id="ef0d2-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ef0d2-205">Classes used in</span></span>        | [<span data-ttu-id="ef0d2-206">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-206">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ef0d2-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef0d2-207">Windows Server 2008</span></span>



| <span data-ttu-id="ef0d2-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="ef0d2-208">Entry</span></span> | <span data-ttu-id="ef0d2-209">Значение</span><span class="sxs-lookup"><span data-stu-id="ef0d2-209">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef0d2-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ef0d2-210">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef0d2-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef0d2-211">MAPI-Id</span></span>                | <span data-ttu-id="ef0d2-212">0x8018</span><span class="sxs-lookup"><span data-stu-id="ef0d2-212">0x8018</span></span>                                                   |
| <span data-ttu-id="ef0d2-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef0d2-213">System-Only</span></span>            | <span data-ttu-id="ef0d2-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-214">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ef0d2-215">Is-Single-Valued</span></span>       | <span data-ttu-id="ef0d2-216">True</span><span class="sxs-lookup"><span data-stu-id="ef0d2-216">True</span></span>                                                     |
| <span data-ttu-id="ef0d2-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ef0d2-217">Is Indexed</span></span>             | <span data-ttu-id="ef0d2-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-218">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ef0d2-219">In Global Catalog</span></span>      | <span data-ttu-id="ef0d2-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-220">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ef0d2-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef0d2-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ef0d2-222">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef0d2-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef0d2-223">Range-Lower</span></span>            | <span data-ttu-id="ef0d2-224">1</span><span class="sxs-lookup"><span data-stu-id="ef0d2-224">1</span></span>                                                        |
| <span data-ttu-id="ef0d2-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef0d2-225">Range-Upper</span></span>            | <span data-ttu-id="ef0d2-226">4096</span><span class="sxs-lookup"><span data-stu-id="ef0d2-226">4096</span></span>                                                     |
| <span data-ttu-id="ef0d2-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-227">Search-Flags</span></span>           | <span data-ttu-id="ef0d2-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef0d2-228">0x00000000</span></span>                                               |
| <span data-ttu-id="ef0d2-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-229">System-Flags</span></span>           | <span data-ttu-id="ef0d2-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef0d2-230">0x00000010</span></span>                                               |
| <span data-ttu-id="ef0d2-231">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ef0d2-231">Classes used in</span></span>        | [<span data-ttu-id="ef0d2-232">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-232">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ef0d2-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef0d2-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ef0d2-234">Ввод</span><span class="sxs-lookup"><span data-stu-id="ef0d2-234">Entry</span></span> | <span data-ttu-id="ef0d2-235">Значение</span><span class="sxs-lookup"><span data-stu-id="ef0d2-235">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef0d2-236">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ef0d2-236">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef0d2-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef0d2-237">MAPI-Id</span></span>                | <span data-ttu-id="ef0d2-238">0x8018</span><span class="sxs-lookup"><span data-stu-id="ef0d2-238">0x8018</span></span>                                                   |
| <span data-ttu-id="ef0d2-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef0d2-239">System-Only</span></span>            | <span data-ttu-id="ef0d2-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-240">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ef0d2-241">Is-Single-Valued</span></span>       | <span data-ttu-id="ef0d2-242">True</span><span class="sxs-lookup"><span data-stu-id="ef0d2-242">True</span></span>                                                     |
| <span data-ttu-id="ef0d2-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ef0d2-243">Is Indexed</span></span>             | <span data-ttu-id="ef0d2-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-244">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ef0d2-245">In Global Catalog</span></span>      | <span data-ttu-id="ef0d2-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-246">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ef0d2-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef0d2-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ef0d2-248">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef0d2-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef0d2-249">Range-Lower</span></span>            | <span data-ttu-id="ef0d2-250">1</span><span class="sxs-lookup"><span data-stu-id="ef0d2-250">1</span></span>                                                        |
| <span data-ttu-id="ef0d2-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef0d2-251">Range-Upper</span></span>            | <span data-ttu-id="ef0d2-252">4096</span><span class="sxs-lookup"><span data-stu-id="ef0d2-252">4096</span></span>                                                     |
| <span data-ttu-id="ef0d2-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-253">Search-Flags</span></span>           | <span data-ttu-id="ef0d2-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef0d2-254">0x00000000</span></span>                                               |
| <span data-ttu-id="ef0d2-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-255">System-Flags</span></span>           | <span data-ttu-id="ef0d2-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef0d2-256">0x00000010</span></span>                                               |
| <span data-ttu-id="ef0d2-257">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ef0d2-257">Classes used in</span></span>        | [<span data-ttu-id="ef0d2-258">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-258">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ef0d2-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ef0d2-259">Windows Server 2012</span></span>



| <span data-ttu-id="ef0d2-260">Ввод</span><span class="sxs-lookup"><span data-stu-id="ef0d2-260">Entry</span></span> | <span data-ttu-id="ef0d2-261">Значение</span><span class="sxs-lookup"><span data-stu-id="ef0d2-261">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="ef0d2-262">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ef0d2-262">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="ef0d2-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ef0d2-263">MAPI-Id</span></span>                | <span data-ttu-id="ef0d2-264">0x8018</span><span class="sxs-lookup"><span data-stu-id="ef0d2-264">0x8018</span></span>                                                   |
| <span data-ttu-id="ef0d2-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="ef0d2-265">System-Only</span></span>            | <span data-ttu-id="ef0d2-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-266">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-267">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ef0d2-267">Is-Single-Valued</span></span>       | <span data-ttu-id="ef0d2-268">True</span><span class="sxs-lookup"><span data-stu-id="ef0d2-268">True</span></span>                                                     |
| <span data-ttu-id="ef0d2-269">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ef0d2-269">Is Indexed</span></span>             | <span data-ttu-id="ef0d2-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-270">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-271">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ef0d2-271">In Global Catalog</span></span>      | <span data-ttu-id="ef0d2-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="ef0d2-272">False</span></span>                                                    |
| <span data-ttu-id="ef0d2-273">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ef0d2-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="ef0d2-274">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ef0d2-274">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="ef0d2-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ef0d2-275">Range-Lower</span></span>            | <span data-ttu-id="ef0d2-276">1</span><span class="sxs-lookup"><span data-stu-id="ef0d2-276">1</span></span>                                                        |
| <span data-ttu-id="ef0d2-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ef0d2-277">Range-Upper</span></span>            | <span data-ttu-id="ef0d2-278">4096</span><span class="sxs-lookup"><span data-stu-id="ef0d2-278">4096</span></span>                                                     |
| <span data-ttu-id="ef0d2-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-279">Search-Flags</span></span>           | <span data-ttu-id="ef0d2-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ef0d2-280">0x00000000</span></span>                                               |
| <span data-ttu-id="ef0d2-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ef0d2-281">System-Flags</span></span>           | <span data-ttu-id="ef0d2-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ef0d2-282">0x00000010</span></span>                                               |
| <span data-ttu-id="ef0d2-283">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ef0d2-283">Classes used in</span></span>        | [<span data-ttu-id="ef0d2-284">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="ef0d2-284">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



 

 





