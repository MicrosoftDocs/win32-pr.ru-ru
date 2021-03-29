---
title: Атрибут Help-Data32
description: Этот атрибут использовался для формата файла справки Win32 для Exchange 4,0. Он не используется для других версий Exchange.
ms.assetid: 33e64ff9-7cb4-43a6-8d7b-1c5e925b783c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Help-Data32
- Схема AD атрибута helpData32
topic_type:
- apiref
api_name:
- Help-Data32
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32debc8c72c95313b8da6288e0d31f5713a4205a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654823"
---
# <a name="help-data32-attribute"></a><span data-ttu-id="82f0d-106">Атрибут Help-Data32</span><span class="sxs-lookup"><span data-stu-id="82f0d-106">Help-Data32 attribute</span></span>

<span data-ttu-id="82f0d-107">Этот атрибут использовался для формата файла справки Win32 для Exchange 4,0.</span><span class="sxs-lookup"><span data-stu-id="82f0d-107">This attribute was used for the Win32 help file format for Exchange 4.0.</span></span> <span data-ttu-id="82f0d-108">Он не используется для других версий Exchange.</span><span class="sxs-lookup"><span data-stu-id="82f0d-108">It is not used for any other versions of Exchange.</span></span>



| <span data-ttu-id="82f0d-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="82f0d-109">Entry</span></span> | <span data-ttu-id="82f0d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="82f0d-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="82f0d-111">CN</span><span class="sxs-lookup"><span data-stu-id="82f0d-111">CN</span></span>                | <span data-ttu-id="82f0d-112">Help-Data32</span><span class="sxs-lookup"><span data-stu-id="82f0d-112">Help-Data32</span></span>                                           |
| <span data-ttu-id="82f0d-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="82f0d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="82f0d-114">helpData32</span><span class="sxs-lookup"><span data-stu-id="82f0d-114">helpData32</span></span>                                            |
| <span data-ttu-id="82f0d-115">Размер</span><span class="sxs-lookup"><span data-stu-id="82f0d-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="82f0d-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="82f0d-116">Update Privilege</span></span>  | <span data-ttu-id="82f0d-117">Используется системой.</span><span class="sxs-lookup"><span data-stu-id="82f0d-117">This is used by the system.</span></span>                           |
| <span data-ttu-id="82f0d-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="82f0d-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="82f0d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="82f0d-119">Attribute-Id</span></span>      | <span data-ttu-id="82f0d-120">1.2.840.113556.1.2.9</span><span class="sxs-lookup"><span data-stu-id="82f0d-120">1.2.840.113556.1.2.9</span></span>                                  |
| <span data-ttu-id="82f0d-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="82f0d-121">System-Id-Guid</span></span>    | <span data-ttu-id="82f0d-122">5fd424a8-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="82f0d-122">5fd424a8-1262-11d0-a060-00aa006c33ed</span></span>                  |
| <span data-ttu-id="82f0d-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82f0d-123">Syntax</span></span>            | [<span data-ttu-id="82f0d-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="82f0d-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="82f0d-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="82f0d-125">Implementations</span></span>

-   [<span data-ttu-id="82f0d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="82f0d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="82f0d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="82f0d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="82f0d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="82f0d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="82f0d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="82f0d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="82f0d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="82f0d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="82f0d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="82f0d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="82f0d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82f0d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="82f0d-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="82f0d-133">Entry</span></span> | <span data-ttu-id="82f0d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="82f0d-134">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="82f0d-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82f0d-135">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="82f0d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82f0d-136">MAPI-Id</span></span>                | <span data-ttu-id="82f0d-137">0x8010</span><span class="sxs-lookup"><span data-stu-id="82f0d-137">0x8010</span></span>                                                   |
| <span data-ttu-id="82f0d-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="82f0d-138">System-Only</span></span>            | <span data-ttu-id="82f0d-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-139">False</span></span>                                                    |
| <span data-ttu-id="82f0d-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82f0d-140">Is-Single-Valued</span></span>       | <span data-ttu-id="82f0d-141">True</span><span class="sxs-lookup"><span data-stu-id="82f0d-141">True</span></span>                                                     |
| <span data-ttu-id="82f0d-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82f0d-142">Is Indexed</span></span>             | <span data-ttu-id="82f0d-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-143">False</span></span>                                                    |
| <span data-ttu-id="82f0d-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82f0d-144">In Global Catalog</span></span>      | <span data-ttu-id="82f0d-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-145">False</span></span>                                                    |
| <span data-ttu-id="82f0d-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82f0d-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="82f0d-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82f0d-147">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="82f0d-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82f0d-148">Range-Lower</span></span>            | <span data-ttu-id="82f0d-149">1</span><span class="sxs-lookup"><span data-stu-id="82f0d-149">1</span></span>                                                        |
| <span data-ttu-id="82f0d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82f0d-150">Range-Upper</span></span>            | <span data-ttu-id="82f0d-151">32768</span><span class="sxs-lookup"><span data-stu-id="82f0d-151">32768</span></span>                                                    |
| <span data-ttu-id="82f0d-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-152">Search-Flags</span></span>           | <span data-ttu-id="82f0d-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82f0d-153">0x00000000</span></span>                                               |
| <span data-ttu-id="82f0d-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-154">System-Flags</span></span>           | <span data-ttu-id="82f0d-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82f0d-155">0x00000010</span></span>                                               |
| <span data-ttu-id="82f0d-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82f0d-156">Classes used in</span></span>        | [<span data-ttu-id="82f0d-157">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="82f0d-157">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="82f0d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="82f0d-158">Windows Server 2003</span></span>



| <span data-ttu-id="82f0d-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="82f0d-159">Entry</span></span> | <span data-ttu-id="82f0d-160">Значение</span><span class="sxs-lookup"><span data-stu-id="82f0d-160">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="82f0d-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82f0d-161">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="82f0d-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82f0d-162">MAPI-Id</span></span>                | <span data-ttu-id="82f0d-163">0x8010</span><span class="sxs-lookup"><span data-stu-id="82f0d-163">0x8010</span></span>                                                   |
| <span data-ttu-id="82f0d-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="82f0d-164">System-Only</span></span>            | <span data-ttu-id="82f0d-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-165">False</span></span>                                                    |
| <span data-ttu-id="82f0d-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82f0d-166">Is-Single-Valued</span></span>       | <span data-ttu-id="82f0d-167">True</span><span class="sxs-lookup"><span data-stu-id="82f0d-167">True</span></span>                                                     |
| <span data-ttu-id="82f0d-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82f0d-168">Is Indexed</span></span>             | <span data-ttu-id="82f0d-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-169">False</span></span>                                                    |
| <span data-ttu-id="82f0d-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82f0d-170">In Global Catalog</span></span>      | <span data-ttu-id="82f0d-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-171">False</span></span>                                                    |
| <span data-ttu-id="82f0d-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82f0d-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="82f0d-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82f0d-173">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="82f0d-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82f0d-174">Range-Lower</span></span>            | <span data-ttu-id="82f0d-175">1</span><span class="sxs-lookup"><span data-stu-id="82f0d-175">1</span></span>                                                        |
| <span data-ttu-id="82f0d-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82f0d-176">Range-Upper</span></span>            | <span data-ttu-id="82f0d-177">32768</span><span class="sxs-lookup"><span data-stu-id="82f0d-177">32768</span></span>                                                    |
| <span data-ttu-id="82f0d-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-178">Search-Flags</span></span>           | <span data-ttu-id="82f0d-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82f0d-179">0x00000000</span></span>                                               |
| <span data-ttu-id="82f0d-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-180">System-Flags</span></span>           | <span data-ttu-id="82f0d-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82f0d-181">0x00000010</span></span>                                               |
| <span data-ttu-id="82f0d-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82f0d-182">Classes used in</span></span>        | [<span data-ttu-id="82f0d-183">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="82f0d-183">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="82f0d-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="82f0d-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="82f0d-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="82f0d-185">Entry</span></span> | <span data-ttu-id="82f0d-186">Значение</span><span class="sxs-lookup"><span data-stu-id="82f0d-186">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="82f0d-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82f0d-187">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="82f0d-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82f0d-188">MAPI-Id</span></span>                | <span data-ttu-id="82f0d-189">0x8010</span><span class="sxs-lookup"><span data-stu-id="82f0d-189">0x8010</span></span>                                                   |
| <span data-ttu-id="82f0d-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="82f0d-190">System-Only</span></span>            | <span data-ttu-id="82f0d-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-191">False</span></span>                                                    |
| <span data-ttu-id="82f0d-192">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82f0d-192">Is-Single-Valued</span></span>       | <span data-ttu-id="82f0d-193">True</span><span class="sxs-lookup"><span data-stu-id="82f0d-193">True</span></span>                                                     |
| <span data-ttu-id="82f0d-194">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82f0d-194">Is Indexed</span></span>             | <span data-ttu-id="82f0d-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-195">False</span></span>                                                    |
| <span data-ttu-id="82f0d-196">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82f0d-196">In Global Catalog</span></span>      | <span data-ttu-id="82f0d-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-197">False</span></span>                                                    |
| <span data-ttu-id="82f0d-198">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82f0d-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="82f0d-199">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82f0d-199">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="82f0d-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82f0d-200">Range-Lower</span></span>            | <span data-ttu-id="82f0d-201">1</span><span class="sxs-lookup"><span data-stu-id="82f0d-201">1</span></span>                                                        |
| <span data-ttu-id="82f0d-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82f0d-202">Range-Upper</span></span>            | <span data-ttu-id="82f0d-203">32768</span><span class="sxs-lookup"><span data-stu-id="82f0d-203">32768</span></span>                                                    |
| <span data-ttu-id="82f0d-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-204">Search-Flags</span></span>           | <span data-ttu-id="82f0d-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82f0d-205">0x00000000</span></span>                                               |
| <span data-ttu-id="82f0d-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-206">System-Flags</span></span>           | <span data-ttu-id="82f0d-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82f0d-207">0x00000010</span></span>                                               |
| <span data-ttu-id="82f0d-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82f0d-208">Classes used in</span></span>        | [<span data-ttu-id="82f0d-209">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="82f0d-209">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="82f0d-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82f0d-210">Windows Server 2008</span></span>



| <span data-ttu-id="82f0d-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="82f0d-211">Entry</span></span> | <span data-ttu-id="82f0d-212">Значение</span><span class="sxs-lookup"><span data-stu-id="82f0d-212">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="82f0d-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82f0d-213">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="82f0d-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82f0d-214">MAPI-Id</span></span>                | <span data-ttu-id="82f0d-215">0x8010</span><span class="sxs-lookup"><span data-stu-id="82f0d-215">0x8010</span></span>                                                   |
| <span data-ttu-id="82f0d-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="82f0d-216">System-Only</span></span>            | <span data-ttu-id="82f0d-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-217">False</span></span>                                                    |
| <span data-ttu-id="82f0d-218">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82f0d-218">Is-Single-Valued</span></span>       | <span data-ttu-id="82f0d-219">True</span><span class="sxs-lookup"><span data-stu-id="82f0d-219">True</span></span>                                                     |
| <span data-ttu-id="82f0d-220">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82f0d-220">Is Indexed</span></span>             | <span data-ttu-id="82f0d-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-221">False</span></span>                                                    |
| <span data-ttu-id="82f0d-222">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82f0d-222">In Global Catalog</span></span>      | <span data-ttu-id="82f0d-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-223">False</span></span>                                                    |
| <span data-ttu-id="82f0d-224">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82f0d-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="82f0d-225">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82f0d-225">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="82f0d-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82f0d-226">Range-Lower</span></span>            | <span data-ttu-id="82f0d-227">1</span><span class="sxs-lookup"><span data-stu-id="82f0d-227">1</span></span>                                                        |
| <span data-ttu-id="82f0d-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82f0d-228">Range-Upper</span></span>            | <span data-ttu-id="82f0d-229">32768</span><span class="sxs-lookup"><span data-stu-id="82f0d-229">32768</span></span>                                                    |
| <span data-ttu-id="82f0d-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-230">Search-Flags</span></span>           | <span data-ttu-id="82f0d-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82f0d-231">0x00000000</span></span>                                               |
| <span data-ttu-id="82f0d-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-232">System-Flags</span></span>           | <span data-ttu-id="82f0d-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82f0d-233">0x00000010</span></span>                                               |
| <span data-ttu-id="82f0d-234">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82f0d-234">Classes used in</span></span>        | [<span data-ttu-id="82f0d-235">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="82f0d-235">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="82f0d-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="82f0d-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="82f0d-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="82f0d-237">Entry</span></span> | <span data-ttu-id="82f0d-238">Значение</span><span class="sxs-lookup"><span data-stu-id="82f0d-238">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="82f0d-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82f0d-239">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="82f0d-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82f0d-240">MAPI-Id</span></span>                | <span data-ttu-id="82f0d-241">0x8010</span><span class="sxs-lookup"><span data-stu-id="82f0d-241">0x8010</span></span>                                                   |
| <span data-ttu-id="82f0d-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="82f0d-242">System-Only</span></span>            | <span data-ttu-id="82f0d-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-243">False</span></span>                                                    |
| <span data-ttu-id="82f0d-244">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82f0d-244">Is-Single-Valued</span></span>       | <span data-ttu-id="82f0d-245">True</span><span class="sxs-lookup"><span data-stu-id="82f0d-245">True</span></span>                                                     |
| <span data-ttu-id="82f0d-246">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82f0d-246">Is Indexed</span></span>             | <span data-ttu-id="82f0d-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-247">False</span></span>                                                    |
| <span data-ttu-id="82f0d-248">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82f0d-248">In Global Catalog</span></span>      | <span data-ttu-id="82f0d-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-249">False</span></span>                                                    |
| <span data-ttu-id="82f0d-250">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82f0d-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="82f0d-251">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82f0d-251">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="82f0d-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82f0d-252">Range-Lower</span></span>            | <span data-ttu-id="82f0d-253">1</span><span class="sxs-lookup"><span data-stu-id="82f0d-253">1</span></span>                                                        |
| <span data-ttu-id="82f0d-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82f0d-254">Range-Upper</span></span>            | <span data-ttu-id="82f0d-255">32768</span><span class="sxs-lookup"><span data-stu-id="82f0d-255">32768</span></span>                                                    |
| <span data-ttu-id="82f0d-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-256">Search-Flags</span></span>           | <span data-ttu-id="82f0d-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82f0d-257">0x00000000</span></span>                                               |
| <span data-ttu-id="82f0d-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-258">System-Flags</span></span>           | <span data-ttu-id="82f0d-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82f0d-259">0x00000010</span></span>                                               |
| <span data-ttu-id="82f0d-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82f0d-260">Classes used in</span></span>        | [<span data-ttu-id="82f0d-261">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="82f0d-261">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="82f0d-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="82f0d-262">Windows Server 2012</span></span>



| <span data-ttu-id="82f0d-263">Ввод</span><span class="sxs-lookup"><span data-stu-id="82f0d-263">Entry</span></span> | <span data-ttu-id="82f0d-264">Значение</span><span class="sxs-lookup"><span data-stu-id="82f0d-264">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="82f0d-265">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="82f0d-265">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="82f0d-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="82f0d-266">MAPI-Id</span></span>                | <span data-ttu-id="82f0d-267">0x8010</span><span class="sxs-lookup"><span data-stu-id="82f0d-267">0x8010</span></span>                                                   |
| <span data-ttu-id="82f0d-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="82f0d-268">System-Only</span></span>            | <span data-ttu-id="82f0d-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-269">False</span></span>                                                    |
| <span data-ttu-id="82f0d-270">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="82f0d-270">Is-Single-Valued</span></span>       | <span data-ttu-id="82f0d-271">True</span><span class="sxs-lookup"><span data-stu-id="82f0d-271">True</span></span>                                                     |
| <span data-ttu-id="82f0d-272">Индексируется</span><span class="sxs-lookup"><span data-stu-id="82f0d-272">Is Indexed</span></span>             | <span data-ttu-id="82f0d-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-273">False</span></span>                                                    |
| <span data-ttu-id="82f0d-274">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="82f0d-274">In Global Catalog</span></span>      | <span data-ttu-id="82f0d-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="82f0d-275">False</span></span>                                                    |
| <span data-ttu-id="82f0d-276">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="82f0d-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="82f0d-277">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="82f0d-277">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="82f0d-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="82f0d-278">Range-Lower</span></span>            | <span data-ttu-id="82f0d-279">1</span><span class="sxs-lookup"><span data-stu-id="82f0d-279">1</span></span>                                                        |
| <span data-ttu-id="82f0d-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="82f0d-280">Range-Upper</span></span>            | <span data-ttu-id="82f0d-281">32768</span><span class="sxs-lookup"><span data-stu-id="82f0d-281">32768</span></span>                                                    |
| <span data-ttu-id="82f0d-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-282">Search-Flags</span></span>           | <span data-ttu-id="82f0d-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="82f0d-283">0x00000000</span></span>                                               |
| <span data-ttu-id="82f0d-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="82f0d-284">System-Flags</span></span>           | <span data-ttu-id="82f0d-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="82f0d-285">0x00000010</span></span>                                               |
| <span data-ttu-id="82f0d-286">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="82f0d-286">Classes used in</span></span>        | [<span data-ttu-id="82f0d-287">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="82f0d-287">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



 

 





