---
title: Атрибут Sequence последнего обновления
description: Этот атрибут содержит порядковый номер обновления для последнего элемента в хранилище классов, который был изменен.
ms.assetid: fd434b8d-31b4-45f7-8d8f-048f61cabb92
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "Последняя обновление — последовательность"
- Схема AD атрибута Ластупдатесекуенце
topic_type:
- apiref
api_name:
- Last-Update-Sequence
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e670c6784ded96a1e81d98f5f1c9bfb859efaa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654943"
---
# <a name="last-update-sequence-attribute"></a><span data-ttu-id="c110f-105">Атрибут Sequence последнего обновления</span><span class="sxs-lookup"><span data-stu-id="c110f-105">Last-Update-Sequence attribute</span></span>

<span data-ttu-id="c110f-106">Этот атрибут содержит порядковый номер обновления для последнего элемента в хранилище классов, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="c110f-106">This attribute contains the update sequence number for the last item in the class store that was changed.</span></span>



| <span data-ttu-id="c110f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c110f-107">Entry</span></span> | <span data-ttu-id="c110f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c110f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c110f-109">CN</span><span class="sxs-lookup"><span data-stu-id="c110f-109">CN</span></span>                | <span data-ttu-id="c110f-110">Последняя-обновление — последовательность</span><span class="sxs-lookup"><span data-stu-id="c110f-110">Last-Update-Sequence</span></span>                        |
| <span data-ttu-id="c110f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c110f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c110f-112">ластупдатесекуенце</span><span class="sxs-lookup"><span data-stu-id="c110f-112">lastUpdateSequence</span></span>                          |
| <span data-ttu-id="c110f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c110f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c110f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c110f-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="c110f-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c110f-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c110f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c110f-116">Attribute-Id</span></span>      | <span data-ttu-id="c110f-117">1.2.840.113556.1.4.330</span><span class="sxs-lookup"><span data-stu-id="c110f-117">1.2.840.113556.1.4.330</span></span>                      |
| <span data-ttu-id="c110f-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c110f-118">System-Id-Guid</span></span>    | <span data-ttu-id="c110f-119">7d6c0e9c-7e20-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c110f-119">7d6c0e9c-7e20-11d0-afd6-00c04fd930c9</span></span>        |
| <span data-ttu-id="c110f-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c110f-120">Syntax</span></span>            | [<span data-ttu-id="c110f-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="c110f-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c110f-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c110f-122">Implementations</span></span>

-   [<span data-ttu-id="c110f-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c110f-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c110f-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c110f-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c110f-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c110f-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c110f-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c110f-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c110f-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c110f-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c110f-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c110f-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c110f-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c110f-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c110f-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="c110f-130">Entry</span></span> | <span data-ttu-id="c110f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c110f-131">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c110f-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c110f-132">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c110f-133">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c110f-134">System-Only</span></span>            | <span data-ttu-id="c110f-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-135">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c110f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c110f-137">True</span><span class="sxs-lookup"><span data-stu-id="c110f-137">True</span></span>                                                                                                            |
| <span data-ttu-id="c110f-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c110f-138">Is Indexed</span></span>             | <span data-ttu-id="c110f-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-139">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c110f-140">In Global Catalog</span></span>      | <span data-ttu-id="c110f-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-141">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c110f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c110f-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c110f-143">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="c110f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c110f-144">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c110f-145">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-146">Search-Flags</span></span>           | <span data-ttu-id="c110f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c110f-147">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="c110f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-148">System-Flags</span></span>           | <span data-ttu-id="c110f-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c110f-149">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="c110f-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c110f-150">Classes used in</span></span>        | [<span data-ttu-id="c110f-151">**Хранилище классов**</span><span class="sxs-lookup"><span data-stu-id="c110f-151">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="c110f-152">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="c110f-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c110f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c110f-153">Windows Server 2003</span></span>



| <span data-ttu-id="c110f-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="c110f-154">Entry</span></span> | <span data-ttu-id="c110f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="c110f-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c110f-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c110f-156">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c110f-157">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c110f-158">System-Only</span></span>            | <span data-ttu-id="c110f-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-159">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c110f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c110f-161">True</span><span class="sxs-lookup"><span data-stu-id="c110f-161">True</span></span>                                                                                                            |
| <span data-ttu-id="c110f-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c110f-162">Is Indexed</span></span>             | <span data-ttu-id="c110f-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-163">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c110f-164">In Global Catalog</span></span>      | <span data-ttu-id="c110f-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-165">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c110f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c110f-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c110f-167">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="c110f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c110f-168">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c110f-169">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-170">Search-Flags</span></span>           | <span data-ttu-id="c110f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c110f-171">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="c110f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-172">System-Flags</span></span>           | <span data-ttu-id="c110f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c110f-173">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="c110f-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c110f-174">Classes used in</span></span>        | [<span data-ttu-id="c110f-175">**Хранилище классов**</span><span class="sxs-lookup"><span data-stu-id="c110f-175">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="c110f-176">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="c110f-176">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c110f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c110f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c110f-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="c110f-178">Entry</span></span> | <span data-ttu-id="c110f-179">Значение</span><span class="sxs-lookup"><span data-stu-id="c110f-179">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c110f-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c110f-180">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c110f-181">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c110f-182">System-Only</span></span>            | <span data-ttu-id="c110f-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-183">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c110f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c110f-185">True</span><span class="sxs-lookup"><span data-stu-id="c110f-185">True</span></span>                                                                                                            |
| <span data-ttu-id="c110f-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c110f-186">Is Indexed</span></span>             | <span data-ttu-id="c110f-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-187">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c110f-188">In Global Catalog</span></span>      | <span data-ttu-id="c110f-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-189">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c110f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c110f-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c110f-191">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="c110f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c110f-192">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c110f-193">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-194">Search-Flags</span></span>           | <span data-ttu-id="c110f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c110f-195">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="c110f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-196">System-Flags</span></span>           | <span data-ttu-id="c110f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c110f-197">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="c110f-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c110f-198">Classes used in</span></span>        | [<span data-ttu-id="c110f-199">**Хранилище классов**</span><span class="sxs-lookup"><span data-stu-id="c110f-199">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="c110f-200">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="c110f-200">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c110f-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c110f-201">Windows Server 2008</span></span>



| <span data-ttu-id="c110f-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="c110f-202">Entry</span></span> | <span data-ttu-id="c110f-203">Значение</span><span class="sxs-lookup"><span data-stu-id="c110f-203">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c110f-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c110f-204">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c110f-205">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c110f-206">System-Only</span></span>            | <span data-ttu-id="c110f-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-207">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c110f-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c110f-209">True</span><span class="sxs-lookup"><span data-stu-id="c110f-209">True</span></span>                                                                                                            |
| <span data-ttu-id="c110f-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c110f-210">Is Indexed</span></span>             | <span data-ttu-id="c110f-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-211">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c110f-212">In Global Catalog</span></span>      | <span data-ttu-id="c110f-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-213">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c110f-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c110f-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c110f-215">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="c110f-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c110f-216">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c110f-217">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-218">Search-Flags</span></span>           | <span data-ttu-id="c110f-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c110f-219">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="c110f-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-220">System-Flags</span></span>           | <span data-ttu-id="c110f-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c110f-221">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="c110f-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c110f-222">Classes used in</span></span>        | [<span data-ttu-id="c110f-223">**Хранилище классов**</span><span class="sxs-lookup"><span data-stu-id="c110f-223">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="c110f-224">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="c110f-224">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c110f-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c110f-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c110f-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="c110f-226">Entry</span></span> | <span data-ttu-id="c110f-227">Значение</span><span class="sxs-lookup"><span data-stu-id="c110f-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c110f-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c110f-228">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c110f-229">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="c110f-230">System-Only</span></span>            | <span data-ttu-id="c110f-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-231">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c110f-232">Is-Single-Valued</span></span>       | <span data-ttu-id="c110f-233">True</span><span class="sxs-lookup"><span data-stu-id="c110f-233">True</span></span>                                                                                                            |
| <span data-ttu-id="c110f-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c110f-234">Is Indexed</span></span>             | <span data-ttu-id="c110f-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-235">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c110f-236">In Global Catalog</span></span>      | <span data-ttu-id="c110f-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-237">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c110f-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="c110f-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c110f-239">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="c110f-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c110f-240">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c110f-241">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-242">Search-Flags</span></span>           | <span data-ttu-id="c110f-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c110f-243">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="c110f-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-244">System-Flags</span></span>           | <span data-ttu-id="c110f-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c110f-245">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="c110f-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c110f-246">Classes used in</span></span>        | [<span data-ttu-id="c110f-247">**Хранилище классов**</span><span class="sxs-lookup"><span data-stu-id="c110f-247">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="c110f-248">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="c110f-248">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c110f-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c110f-249">Windows Server 2012</span></span>



| <span data-ttu-id="c110f-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="c110f-250">Entry</span></span> | <span data-ttu-id="c110f-251">Значение</span><span class="sxs-lookup"><span data-stu-id="c110f-251">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c110f-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c110f-252">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c110f-253">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="c110f-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c110f-254">System-Only</span></span>            | <span data-ttu-id="c110f-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-255">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c110f-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c110f-257">True</span><span class="sxs-lookup"><span data-stu-id="c110f-257">True</span></span>                                                                                                            |
| <span data-ttu-id="c110f-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c110f-258">Is Indexed</span></span>             | <span data-ttu-id="c110f-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-259">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c110f-260">In Global Catalog</span></span>      | <span data-ttu-id="c110f-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="c110f-261">False</span></span>                                                                                                           |
| <span data-ttu-id="c110f-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c110f-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c110f-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c110f-263">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="c110f-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c110f-264">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c110f-265">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="c110f-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-266">Search-Flags</span></span>           | <span data-ttu-id="c110f-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c110f-267">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="c110f-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c110f-268">System-Flags</span></span>           | <span data-ttu-id="c110f-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c110f-269">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="c110f-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c110f-270">Classes used in</span></span>        | [<span data-ttu-id="c110f-271">**Хранилище классов**</span><span class="sxs-lookup"><span data-stu-id="c110f-271">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="c110f-272">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="c110f-272">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





