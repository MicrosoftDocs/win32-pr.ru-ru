---
title: Атрибут DS-Heuristics
description: Содержит глобальные параметры для всего леса.
ms.assetid: d5fd990b-7bbf-4ede-a3af-7f3f7ac959b3
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута DS-Heuristics
- Схема AD атрибута Дшеуристикс
topic_type:
- apiref
api_name:
- DS-Heuristics
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65922b580975ec05877ae33d213ff3a3675ec72f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654862"
---
# <a name="ds-heuristics-attribute"></a><span data-ttu-id="d5c9b-105">Атрибут DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="d5c9b-105">DS-Heuristics attribute</span></span>

<span data-ttu-id="d5c9b-106">Содержит глобальные параметры для всего леса.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-106">Contains global settings for the entire forest.</span></span>

<span data-ttu-id="d5c9b-107">Сведения о битах исключения adminSDholder, доступных на веб-сайте справки и поддержки Майкрософт в статье номер [817433, делегированные разрешения недоступны, и наследование автоматически отключается](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span><span class="sxs-lookup"><span data-stu-id="d5c9b-107">There is information about adminSDholder exclusion bits available on the Microsoft Help and Support website in an article number [817433, Delegated permissions are not available and inheritance is automatically disabled](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span></span>



| <span data-ttu-id="d5c9b-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="d5c9b-108">Entry</span></span> | <span data-ttu-id="d5c9b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="d5c9b-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d5c9b-110">CN</span><span class="sxs-lookup"><span data-stu-id="d5c9b-110">CN</span></span>                | <span data-ttu-id="d5c9b-111">DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="d5c9b-111">DS-Heuristics</span></span>                               |
| <span data-ttu-id="d5c9b-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d5c9b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="d5c9b-113">дшеуристикс</span><span class="sxs-lookup"><span data-stu-id="d5c9b-113">dSHeuristics</span></span>                                |
| <span data-ttu-id="d5c9b-114">Размер</span><span class="sxs-lookup"><span data-stu-id="d5c9b-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="d5c9b-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d5c9b-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="d5c9b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d5c9b-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d5c9b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d5c9b-117">Attribute-Id</span></span>      | <span data-ttu-id="d5c9b-118">1.2.840.113556.1.2.212</span><span class="sxs-lookup"><span data-stu-id="d5c9b-118">1.2.840.113556.1.2.212</span></span>                      |
| <span data-ttu-id="d5c9b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d5c9b-119">System-Id-Guid</span></span>    | <span data-ttu-id="d5c9b-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="d5c9b-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="d5c9b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5c9b-121">Syntax</span></span>            | [<span data-ttu-id="d5c9b-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d5c9b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d5c9b-123">Implementations</span></span>

-   [<span data-ttu-id="d5c9b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d5c9b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d5c9b-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d5c9b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d5c9b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d5c9b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d5c9b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d5c9b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5c9b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="d5c9b-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="d5c9b-132">Entry</span></span> | <span data-ttu-id="d5c9b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d5c9b-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d5c9b-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d5c9b-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c9b-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c9b-136">System-Only</span></span>            | <span data-ttu-id="d5c9b-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-137">False</span></span>                                            |
| <span data-ttu-id="d5c9b-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d5c9b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c9b-139">True</span><span class="sxs-lookup"><span data-stu-id="d5c9b-139">True</span></span>                                             |
| <span data-ttu-id="d5c9b-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d5c9b-140">Is Indexed</span></span>             | <span data-ttu-id="d5c9b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-141">False</span></span>                                            |
| <span data-ttu-id="d5c9b-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d5c9b-142">In Global Catalog</span></span>      | <span data-ttu-id="d5c9b-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-143">False</span></span>                                            |
| <span data-ttu-id="d5c9b-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d5c9b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c9b-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c9b-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d5c9b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c9b-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c9b-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-148">Search-Flags</span></span>           | <span data-ttu-id="d5c9b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c9b-149">0x00000000</span></span>                                       |
| <span data-ttu-id="d5c9b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-150">System-Flags</span></span>           | <span data-ttu-id="d5c9b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c9b-151">0x00000010</span></span>                                       |
| <span data-ttu-id="d5c9b-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d5c9b-152">Classes used in</span></span>        | [<span data-ttu-id="d5c9b-153">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-153">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d5c9b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d5c9b-154">Windows Server 2003</span></span>



| <span data-ttu-id="d5c9b-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="d5c9b-155">Entry</span></span> | <span data-ttu-id="d5c9b-156">Значение</span><span class="sxs-lookup"><span data-stu-id="d5c9b-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d5c9b-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d5c9b-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c9b-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c9b-159">System-Only</span></span>            | <span data-ttu-id="d5c9b-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-160">False</span></span>                                            |
| <span data-ttu-id="d5c9b-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d5c9b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c9b-162">True</span><span class="sxs-lookup"><span data-stu-id="d5c9b-162">True</span></span>                                             |
| <span data-ttu-id="d5c9b-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d5c9b-163">Is Indexed</span></span>             | <span data-ttu-id="d5c9b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-164">False</span></span>                                            |
| <span data-ttu-id="d5c9b-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d5c9b-165">In Global Catalog</span></span>      | <span data-ttu-id="d5c9b-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-166">False</span></span>                                            |
| <span data-ttu-id="d5c9b-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d5c9b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c9b-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c9b-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d5c9b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c9b-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c9b-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-171">Search-Flags</span></span>           | <span data-ttu-id="d5c9b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c9b-172">0x00000000</span></span>                                       |
| <span data-ttu-id="d5c9b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-173">System-Flags</span></span>           | <span data-ttu-id="d5c9b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c9b-174">0x00000010</span></span>                                       |
| <span data-ttu-id="d5c9b-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d5c9b-175">Classes used in</span></span>        | [<span data-ttu-id="d5c9b-176">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-176">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d5c9b-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="d5c9b-177">ADAM</span></span>



| <span data-ttu-id="d5c9b-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="d5c9b-178">Entry</span></span> | <span data-ttu-id="d5c9b-179">Значение</span><span class="sxs-lookup"><span data-stu-id="d5c9b-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d5c9b-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d5c9b-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c9b-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c9b-182">System-Only</span></span>            | <span data-ttu-id="d5c9b-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-183">False</span></span>                                            |
| <span data-ttu-id="d5c9b-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d5c9b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c9b-185">True</span><span class="sxs-lookup"><span data-stu-id="d5c9b-185">True</span></span>                                             |
| <span data-ttu-id="d5c9b-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d5c9b-186">Is Indexed</span></span>             | <span data-ttu-id="d5c9b-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-187">False</span></span>                                            |
| <span data-ttu-id="d5c9b-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d5c9b-188">In Global Catalog</span></span>      | <span data-ttu-id="d5c9b-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-189">False</span></span>                                            |
| <span data-ttu-id="d5c9b-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d5c9b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c9b-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c9b-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d5c9b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c9b-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c9b-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-194">Search-Flags</span></span>           | <span data-ttu-id="d5c9b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c9b-195">0x00000000</span></span>                                       |
| <span data-ttu-id="d5c9b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-196">System-Flags</span></span>           | <span data-ttu-id="d5c9b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c9b-197">0x00000010</span></span>                                       |
| <span data-ttu-id="d5c9b-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d5c9b-198">Classes used in</span></span>        | [<span data-ttu-id="d5c9b-199">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-199">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d5c9b-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d5c9b-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d5c9b-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="d5c9b-201">Entry</span></span> | <span data-ttu-id="d5c9b-202">Значение</span><span class="sxs-lookup"><span data-stu-id="d5c9b-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d5c9b-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d5c9b-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c9b-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c9b-205">System-Only</span></span>            | <span data-ttu-id="d5c9b-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-206">False</span></span>                                            |
| <span data-ttu-id="d5c9b-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d5c9b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c9b-208">True</span><span class="sxs-lookup"><span data-stu-id="d5c9b-208">True</span></span>                                             |
| <span data-ttu-id="d5c9b-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d5c9b-209">Is Indexed</span></span>             | <span data-ttu-id="d5c9b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-210">False</span></span>                                            |
| <span data-ttu-id="d5c9b-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d5c9b-211">In Global Catalog</span></span>      | <span data-ttu-id="d5c9b-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-212">False</span></span>                                            |
| <span data-ttu-id="d5c9b-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d5c9b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c9b-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c9b-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d5c9b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c9b-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c9b-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-217">Search-Flags</span></span>           | <span data-ttu-id="d5c9b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c9b-218">0x00000000</span></span>                                       |
| <span data-ttu-id="d5c9b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-219">System-Flags</span></span>           | <span data-ttu-id="d5c9b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c9b-220">0x00000010</span></span>                                       |
| <span data-ttu-id="d5c9b-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d5c9b-221">Classes used in</span></span>        | [<span data-ttu-id="d5c9b-222">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-222">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d5c9b-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5c9b-223">Windows Server 2008</span></span>



| <span data-ttu-id="d5c9b-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="d5c9b-224">Entry</span></span> | <span data-ttu-id="d5c9b-225">Значение</span><span class="sxs-lookup"><span data-stu-id="d5c9b-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d5c9b-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d5c9b-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c9b-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c9b-228">System-Only</span></span>            | <span data-ttu-id="d5c9b-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-229">False</span></span>                                            |
| <span data-ttu-id="d5c9b-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d5c9b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c9b-231">True</span><span class="sxs-lookup"><span data-stu-id="d5c9b-231">True</span></span>                                             |
| <span data-ttu-id="d5c9b-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d5c9b-232">Is Indexed</span></span>             | <span data-ttu-id="d5c9b-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-233">False</span></span>                                            |
| <span data-ttu-id="d5c9b-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d5c9b-234">In Global Catalog</span></span>      | <span data-ttu-id="d5c9b-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-235">False</span></span>                                            |
| <span data-ttu-id="d5c9b-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d5c9b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c9b-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c9b-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d5c9b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c9b-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c9b-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-240">Search-Flags</span></span>           | <span data-ttu-id="d5c9b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c9b-241">0x00000000</span></span>                                       |
| <span data-ttu-id="d5c9b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-242">System-Flags</span></span>           | <span data-ttu-id="d5c9b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c9b-243">0x00000010</span></span>                                       |
| <span data-ttu-id="d5c9b-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d5c9b-244">Classes used in</span></span>        | [<span data-ttu-id="d5c9b-245">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-245">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d5c9b-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d5c9b-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d5c9b-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="d5c9b-247">Entry</span></span> | <span data-ttu-id="d5c9b-248">Значение</span><span class="sxs-lookup"><span data-stu-id="d5c9b-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d5c9b-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d5c9b-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c9b-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c9b-251">System-Only</span></span>            | <span data-ttu-id="d5c9b-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-252">False</span></span>                                            |
| <span data-ttu-id="d5c9b-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d5c9b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c9b-254">True</span><span class="sxs-lookup"><span data-stu-id="d5c9b-254">True</span></span>                                             |
| <span data-ttu-id="d5c9b-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d5c9b-255">Is Indexed</span></span>             | <span data-ttu-id="d5c9b-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-256">False</span></span>                                            |
| <span data-ttu-id="d5c9b-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d5c9b-257">In Global Catalog</span></span>      | <span data-ttu-id="d5c9b-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-258">False</span></span>                                            |
| <span data-ttu-id="d5c9b-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d5c9b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c9b-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c9b-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d5c9b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c9b-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c9b-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-263">Search-Flags</span></span>           | <span data-ttu-id="d5c9b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c9b-264">0x00000000</span></span>                                       |
| <span data-ttu-id="d5c9b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-265">System-Flags</span></span>           | <span data-ttu-id="d5c9b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c9b-266">0x00000010</span></span>                                       |
| <span data-ttu-id="d5c9b-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d5c9b-267">Classes used in</span></span>        | [<span data-ttu-id="d5c9b-268">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-268">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d5c9b-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5c9b-269">Windows Server 2012</span></span>



| <span data-ttu-id="d5c9b-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="d5c9b-270">Entry</span></span> | <span data-ttu-id="d5c9b-271">Значение</span><span class="sxs-lookup"><span data-stu-id="d5c9b-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="d5c9b-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d5c9b-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d5c9b-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="d5c9b-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="d5c9b-274">System-Only</span></span>            | <span data-ttu-id="d5c9b-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-275">False</span></span>                                            |
| <span data-ttu-id="d5c9b-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d5c9b-276">Is-Single-Valued</span></span>       | <span data-ttu-id="d5c9b-277">True</span><span class="sxs-lookup"><span data-stu-id="d5c9b-277">True</span></span>                                             |
| <span data-ttu-id="d5c9b-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d5c9b-278">Is Indexed</span></span>             | <span data-ttu-id="d5c9b-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-279">False</span></span>                                            |
| <span data-ttu-id="d5c9b-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d5c9b-280">In Global Catalog</span></span>      | <span data-ttu-id="d5c9b-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="d5c9b-281">False</span></span>                                            |
| <span data-ttu-id="d5c9b-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d5c9b-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="d5c9b-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d5c9b-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="d5c9b-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d5c9b-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d5c9b-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="d5c9b-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-286">Search-Flags</span></span>           | <span data-ttu-id="d5c9b-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5c9b-287">0x00000000</span></span>                                       |
| <span data-ttu-id="d5c9b-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d5c9b-288">System-Flags</span></span>           | <span data-ttu-id="d5c9b-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c9b-289">0x00000010</span></span>                                       |
| <span data-ttu-id="d5c9b-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d5c9b-290">Classes used in</span></span>        | [<span data-ttu-id="d5c9b-291">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="d5c9b-291">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d5c9b-292">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5c9b-292">Remarks</span></span>

<span data-ttu-id="d5c9b-293">Каждый лес Active Directory содержит атрибут DS-Heuristics, который содержит параметры для всего леса.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-293">Each Active Directory forest contains a DS-Heuristics attribute that contains settings for the entire forest.</span></span> <span data-ttu-id="d5c9b-294">Атрибут DS-Heuristics является атрибутом CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration, <Domain> Object.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-294">The DS-Heuristics attribute is an attribute of the "CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,<Domain>" object.</span></span>

<span data-ttu-id="d5c9b-295">DS-Heuristics — это строка в Юникоде, в которой каждый символ содержит значение для одного параметра на уровне домена.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-295">DS-Heuristics is a Unicode string in which each character contains a value for a single domain-wide setting.</span></span> <span data-ttu-id="d5c9b-296">Строка DS-Heuristics имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-296">The DS-Heuristics string takes the following format.</span></span>

``` syntax
|<1>|<2>|<3>|<4>|<5>|<6>|<7>|<8>|<9>|<10>|<11>|<12>|<13>|<14>|<15>|<16>|<17>|<18>|<19>|<20>|<21>|<22>|<23>|<24>|<25>|
```

<span data-ttu-id="d5c9b-297">Для обеспечения проверки данных каждому десятому символу присваивается номер символа, деленный на десять.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-297">To provide data validation, each tenth character is set to the character number divided by ten.</span></span> <span data-ttu-id="d5c9b-298">Например, десятым символом является "1"; двадцатым символом является "2" и т. д.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-298">For example, the tenth character is '1'; the twentieth character is '2', and so on.</span></span>

<span data-ttu-id="d5c9b-299">Любой символ, который не задан, считается "0".</span><span class="sxs-lookup"><span data-stu-id="d5c9b-299">Any character that is not set is assumed to be a '0'.</span></span> <span data-ttu-id="d5c9b-300">Если атрибут DS-Heuristics не задан, предполагается, что все значения равны "0".</span><span class="sxs-lookup"><span data-stu-id="d5c9b-300">If the DS-Heuristics attribute is not set, all values are assumed to be '0'.</span></span> <span data-ttu-id="d5c9b-301">В настоящее время используется 25 символов, и нет необходимости вставлять строку для заполнения всех 25 символов.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-301">There are currently 25 characters being used and it is not necessary to pad the string to fill all 25 characters.</span></span> <span data-ttu-id="d5c9b-302">Например, если используется наибольший символ, то строка «0000002» приемлема.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-302">For example, if the highest character being used is 7, then the string "0000002" is acceptable.</span></span>

<span data-ttu-id="d5c9b-303">Дополнительные сведения о каждом символе см. [в разделе дшеуристикс in \[ MS-ADTS \] Active Directory Техническая спецификация](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span><span class="sxs-lookup"><span data-stu-id="d5c9b-303">For details about each character, see [dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span></span>

### <a name="anr-search-filters"></a><span data-ttu-id="d5c9b-304">Фильтры поиска ANR</span><span class="sxs-lookup"><span data-stu-id="d5c9b-304">ANR Search Filters</span></span>

<span data-ttu-id="d5c9b-305">Для изменения поведения фильтров поиска ANR используются символы 1, 2 и 4.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-305">Characters 1, 2, and 4 are used to modify the behavior of ANR search filters.</span></span> <span data-ttu-id="d5c9b-306">Если для символа 1 задано значение ' 1 ', расширение фильтра ANR для включения **givenName**  -  **Фамилия** (если место найдено) отключено.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-306">If character 1 is set to '1', then the expansion of the ANR filter to include **GivenName** - **Surname** (when space is found) is disabled.</span></span> <span data-ttu-id="d5c9b-307">Если для символа 2 задано значение ' 1 ', расширение фильтра ANR для включения **фамилии**  -  **givenName** отключается.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-307">If character 2 is set to '1', the expansion of the ANR filter to include **Surname** - **GivenName** is disabled.</span></span> <span data-ttu-id="d5c9b-308">Если в строке поиска содержится внедренное пространство, то строка поиска обычно делится на две строки, которые сравниваются по отношению к атрибутам **givenName** и **Фамилия** .</span><span class="sxs-lookup"><span data-stu-id="d5c9b-308">If an embedded space is present in the search string, the search string will normally be divided into two strings, which are compared pair-wise against the **GivenName** and **Surname** attributes.</span></span> <span data-ttu-id="d5c9b-309">Установка символов 1 и 2 в значение "1" предотвратит попытки этих совпадений.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-309">Setting characters 1 and 2 to '1' will prevent those matches from being attempted.</span></span> <span data-ttu-id="d5c9b-310">Такое сопоставление может быть отключено, если администратор уверен, что Поиск "Джеффа Иванов" всегда будет предоставляться как "Джефф Иванов", а не "Иванов, Иван".</span><span class="sxs-lookup"><span data-stu-id="d5c9b-310">This matching might be disabled if the administrator is confident that searches for "Jeff Smith" would always be provided as "jeff smith" and not "smith, jeff".</span></span> <span data-ttu-id="d5c9b-311">Обычно только одно или другое совпадение будет подавлено в соответствии с местным соглашением.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-311">Normally only one or the other match would be suppressed, according to local convention.</span></span>

<span data-ttu-id="d5c9b-312">Если для символа 4 задано значение ' 1 ', Active Directory будет выполнять разрешение псевдонимов, предшествующих упреждающее.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-312">If the character 4 is set to '1' then Active Directory will perform "pre-emptive nickname resolution".</span></span> <span data-ttu-id="d5c9b-313">То есть, если строка поиска точно совпадает с псевдонимом ровно одного объекта в области поиска, один объект возвращается в результате поиска, а остальная часть класса ANR пропускается.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-313">That is, if the search string exactly matches the nickname of exactly one object in the search scope, that one object is returned as the result of the search, and the rest of ANR is skipped.</span></span> <span data-ttu-id="d5c9b-314">Обратите внимание, что хотя остальная часть поиска ANR доступна по протоколу LDAP, упреждающее разрешение псевдонимов (также называемое «привязкой псевдонима») доступно только через MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5c9b-314">Note that while the rest of ANR searching is available through LDAP, pre-emptive nickname resolution (also known as "nickname snap") is available only through MAPI.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5c9b-315">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5c9b-315">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5c9b-316">[\[Техническая спецификация дшеуристикс в MS-ADTS \] Active Directory](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span><span class="sxs-lookup"><span data-stu-id="d5c9b-316">[dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span></span>
</dt> </dl>

 

