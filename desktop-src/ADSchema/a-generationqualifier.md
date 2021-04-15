---
title: Атрибут Generation-Qualifier
description: Указывает создание пользователя. Например, Jr. или II.
ms.assetid: 6b882114-3273-43ff-8df3-5b23c98a2dae
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Generation-Qualifier
- Схема AD атрибута Женератионкуалифиер
topic_type:
- apiref
api_name:
- Generation-Qualifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc29fdc6bc32273113c5daab2482465535dee145
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655274"
---
# <a name="generation-qualifier-attribute"></a><span data-ttu-id="2e3c5-106">Атрибут Generation-Qualifier</span><span class="sxs-lookup"><span data-stu-id="2e3c5-106">Generation-Qualifier attribute</span></span>

<span data-ttu-id="2e3c5-107">Указывает создание пользователя.</span><span class="sxs-lookup"><span data-stu-id="2e3c5-107">Indicates a person generation.</span></span> <span data-ttu-id="2e3c5-108">Например, Jr. или II.</span><span class="sxs-lookup"><span data-stu-id="2e3c5-108">For example, Jr. or II.</span></span>



| <span data-ttu-id="2e3c5-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e3c5-109">Entry</span></span> | <span data-ttu-id="2e3c5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2e3c5-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2e3c5-111">CN</span><span class="sxs-lookup"><span data-stu-id="2e3c5-111">CN</span></span>                | <span data-ttu-id="2e3c5-112">Generation-Qualifier</span><span class="sxs-lookup"><span data-stu-id="2e3c5-112">Generation-Qualifier</span></span>                        |
| <span data-ttu-id="2e3c5-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2e3c5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="2e3c5-114">женератионкуалифиер</span><span class="sxs-lookup"><span data-stu-id="2e3c5-114">generationQualifier</span></span>                         |
| <span data-ttu-id="2e3c5-115">Размер</span><span class="sxs-lookup"><span data-stu-id="2e3c5-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="2e3c5-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2e3c5-116">Update Privilege</span></span>  | <span data-ttu-id="2e3c5-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="2e3c5-117">Domain Administrator</span></span>                        |
| <span data-ttu-id="2e3c5-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2e3c5-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="2e3c5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2e3c5-119">Attribute-Id</span></span>      | <span data-ttu-id="2e3c5-120">2.5.4.44</span><span class="sxs-lookup"><span data-stu-id="2e3c5-120">2.5.4.44</span></span>                                    |
| <span data-ttu-id="2e3c5-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2e3c5-121">System-Id-Guid</span></span>    | <span data-ttu-id="2e3c5-122">16775804-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2e3c5-122">16775804-47f3-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="2e3c5-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e3c5-123">Syntax</span></span>            | [<span data-ttu-id="2e3c5-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2e3c5-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2e3c5-125">Implementations</span></span>

-   [<span data-ttu-id="2e3c5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2e3c5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2e3c5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2e3c5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2e3c5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2e3c5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2e3c5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e3c5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2e3c5-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e3c5-133">Entry</span></span> | <span data-ttu-id="2e3c5-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2e3c5-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2e3c5-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e3c5-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2e3c5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e3c5-136">MAPI-Id</span></span>                | <span data-ttu-id="2e3c5-137">0x8C53</span><span class="sxs-lookup"><span data-stu-id="2e3c5-137">0x8C53</span></span>                                                             |
| <span data-ttu-id="2e3c5-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e3c5-138">System-Only</span></span>            | <span data-ttu-id="2e3c5-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-139">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e3c5-140">Is-Single-Valued</span></span>       | <span data-ttu-id="2e3c5-141">True</span><span class="sxs-lookup"><span data-stu-id="2e3c5-141">True</span></span>                                                               |
| <span data-ttu-id="2e3c5-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e3c5-142">Is Indexed</span></span>             | <span data-ttu-id="2e3c5-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-143">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e3c5-144">In Global Catalog</span></span>      | <span data-ttu-id="2e3c5-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-145">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e3c5-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e3c5-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e3c5-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2e3c5-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e3c5-148">Range-Lower</span></span>            | <span data-ttu-id="2e3c5-149">1</span><span class="sxs-lookup"><span data-stu-id="2e3c5-149">1</span></span>                                                                  |
| <span data-ttu-id="2e3c5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e3c5-150">Range-Upper</span></span>            | <span data-ttu-id="2e3c5-151">64</span><span class="sxs-lookup"><span data-stu-id="2e3c5-151">64</span></span>                                                                 |
| <span data-ttu-id="2e3c5-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-152">Search-Flags</span></span>           | <span data-ttu-id="2e3c5-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e3c5-153">0x00000000</span></span>                                                         |
| <span data-ttu-id="2e3c5-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-154">System-Flags</span></span>           | <span data-ttu-id="2e3c5-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e3c5-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="2e3c5-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e3c5-156">Classes used in</span></span>        | [<span data-ttu-id="2e3c5-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2e3c5-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e3c5-158">Windows Server 2003</span></span>



| <span data-ttu-id="2e3c5-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e3c5-159">Entry</span></span> | <span data-ttu-id="2e3c5-160">Значение</span><span class="sxs-lookup"><span data-stu-id="2e3c5-160">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2e3c5-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e3c5-161">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2e3c5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e3c5-162">MAPI-Id</span></span>                | <span data-ttu-id="2e3c5-163">0x8C53</span><span class="sxs-lookup"><span data-stu-id="2e3c5-163">0x8C53</span></span>                                                             |
| <span data-ttu-id="2e3c5-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e3c5-164">System-Only</span></span>            | <span data-ttu-id="2e3c5-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-165">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e3c5-166">Is-Single-Valued</span></span>       | <span data-ttu-id="2e3c5-167">True</span><span class="sxs-lookup"><span data-stu-id="2e3c5-167">True</span></span>                                                               |
| <span data-ttu-id="2e3c5-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e3c5-168">Is Indexed</span></span>             | <span data-ttu-id="2e3c5-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-169">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e3c5-170">In Global Catalog</span></span>      | <span data-ttu-id="2e3c5-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-171">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e3c5-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e3c5-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e3c5-173">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2e3c5-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e3c5-174">Range-Lower</span></span>            | <span data-ttu-id="2e3c5-175">1</span><span class="sxs-lookup"><span data-stu-id="2e3c5-175">1</span></span>                                                                  |
| <span data-ttu-id="2e3c5-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e3c5-176">Range-Upper</span></span>            | <span data-ttu-id="2e3c5-177">64</span><span class="sxs-lookup"><span data-stu-id="2e3c5-177">64</span></span>                                                                 |
| <span data-ttu-id="2e3c5-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-178">Search-Flags</span></span>           | <span data-ttu-id="2e3c5-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e3c5-179">0x00000000</span></span>                                                         |
| <span data-ttu-id="2e3c5-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-180">System-Flags</span></span>           | <span data-ttu-id="2e3c5-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e3c5-181">0x00000010</span></span>                                                         |
| <span data-ttu-id="2e3c5-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e3c5-182">Classes used in</span></span>        | [<span data-ttu-id="2e3c5-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2e3c5-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e3c5-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2e3c5-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e3c5-185">Entry</span></span> | <span data-ttu-id="2e3c5-186">Значение</span><span class="sxs-lookup"><span data-stu-id="2e3c5-186">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2e3c5-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e3c5-187">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2e3c5-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e3c5-188">MAPI-Id</span></span>                | <span data-ttu-id="2e3c5-189">0x8C53</span><span class="sxs-lookup"><span data-stu-id="2e3c5-189">0x8C53</span></span>                                                             |
| <span data-ttu-id="2e3c5-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e3c5-190">System-Only</span></span>            | <span data-ttu-id="2e3c5-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-191">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-192">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e3c5-192">Is-Single-Valued</span></span>       | <span data-ttu-id="2e3c5-193">True</span><span class="sxs-lookup"><span data-stu-id="2e3c5-193">True</span></span>                                                               |
| <span data-ttu-id="2e3c5-194">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e3c5-194">Is Indexed</span></span>             | <span data-ttu-id="2e3c5-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-195">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-196">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e3c5-196">In Global Catalog</span></span>      | <span data-ttu-id="2e3c5-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-197">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-198">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e3c5-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e3c5-199">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e3c5-199">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2e3c5-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e3c5-200">Range-Lower</span></span>            | <span data-ttu-id="2e3c5-201">1</span><span class="sxs-lookup"><span data-stu-id="2e3c5-201">1</span></span>                                                                  |
| <span data-ttu-id="2e3c5-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e3c5-202">Range-Upper</span></span>            | <span data-ttu-id="2e3c5-203">64</span><span class="sxs-lookup"><span data-stu-id="2e3c5-203">64</span></span>                                                                 |
| <span data-ttu-id="2e3c5-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-204">Search-Flags</span></span>           | <span data-ttu-id="2e3c5-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e3c5-205">0x00000000</span></span>                                                         |
| <span data-ttu-id="2e3c5-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-206">System-Flags</span></span>           | <span data-ttu-id="2e3c5-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e3c5-207">0x00000010</span></span>                                                         |
| <span data-ttu-id="2e3c5-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e3c5-208">Classes used in</span></span>        | [<span data-ttu-id="2e3c5-209">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2e3c5-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e3c5-210">Windows Server 2008</span></span>



| <span data-ttu-id="2e3c5-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e3c5-211">Entry</span></span> | <span data-ttu-id="2e3c5-212">Значение</span><span class="sxs-lookup"><span data-stu-id="2e3c5-212">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2e3c5-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e3c5-213">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2e3c5-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e3c5-214">MAPI-Id</span></span>                | <span data-ttu-id="2e3c5-215">0x8C53</span><span class="sxs-lookup"><span data-stu-id="2e3c5-215">0x8C53</span></span>                                                             |
| <span data-ttu-id="2e3c5-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e3c5-216">System-Only</span></span>            | <span data-ttu-id="2e3c5-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-217">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-218">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e3c5-218">Is-Single-Valued</span></span>       | <span data-ttu-id="2e3c5-219">True</span><span class="sxs-lookup"><span data-stu-id="2e3c5-219">True</span></span>                                                               |
| <span data-ttu-id="2e3c5-220">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e3c5-220">Is Indexed</span></span>             | <span data-ttu-id="2e3c5-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-221">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-222">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e3c5-222">In Global Catalog</span></span>      | <span data-ttu-id="2e3c5-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-223">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-224">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e3c5-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e3c5-225">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e3c5-225">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2e3c5-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e3c5-226">Range-Lower</span></span>            | <span data-ttu-id="2e3c5-227">1</span><span class="sxs-lookup"><span data-stu-id="2e3c5-227">1</span></span>                                                                  |
| <span data-ttu-id="2e3c5-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e3c5-228">Range-Upper</span></span>            | <span data-ttu-id="2e3c5-229">64</span><span class="sxs-lookup"><span data-stu-id="2e3c5-229">64</span></span>                                                                 |
| <span data-ttu-id="2e3c5-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-230">Search-Flags</span></span>           | <span data-ttu-id="2e3c5-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e3c5-231">0x00000000</span></span>                                                         |
| <span data-ttu-id="2e3c5-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-232">System-Flags</span></span>           | <span data-ttu-id="2e3c5-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e3c5-233">0x00000010</span></span>                                                         |
| <span data-ttu-id="2e3c5-234">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e3c5-234">Classes used in</span></span>        | [<span data-ttu-id="2e3c5-235">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2e3c5-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e3c5-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2e3c5-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e3c5-237">Entry</span></span> | <span data-ttu-id="2e3c5-238">Значение</span><span class="sxs-lookup"><span data-stu-id="2e3c5-238">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2e3c5-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e3c5-239">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2e3c5-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e3c5-240">MAPI-Id</span></span>                | <span data-ttu-id="2e3c5-241">0x8C53</span><span class="sxs-lookup"><span data-stu-id="2e3c5-241">0x8C53</span></span>                                                             |
| <span data-ttu-id="2e3c5-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e3c5-242">System-Only</span></span>            | <span data-ttu-id="2e3c5-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-243">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-244">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e3c5-244">Is-Single-Valued</span></span>       | <span data-ttu-id="2e3c5-245">True</span><span class="sxs-lookup"><span data-stu-id="2e3c5-245">True</span></span>                                                               |
| <span data-ttu-id="2e3c5-246">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e3c5-246">Is Indexed</span></span>             | <span data-ttu-id="2e3c5-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-247">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-248">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e3c5-248">In Global Catalog</span></span>      | <span data-ttu-id="2e3c5-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-249">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-250">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e3c5-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e3c5-251">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e3c5-251">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2e3c5-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e3c5-252">Range-Lower</span></span>            | <span data-ttu-id="2e3c5-253">1</span><span class="sxs-lookup"><span data-stu-id="2e3c5-253">1</span></span>                                                                  |
| <span data-ttu-id="2e3c5-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e3c5-254">Range-Upper</span></span>            | <span data-ttu-id="2e3c5-255">64</span><span class="sxs-lookup"><span data-stu-id="2e3c5-255">64</span></span>                                                                 |
| <span data-ttu-id="2e3c5-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-256">Search-Flags</span></span>           | <span data-ttu-id="2e3c5-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e3c5-257">0x00000000</span></span>                                                         |
| <span data-ttu-id="2e3c5-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-258">System-Flags</span></span>           | <span data-ttu-id="2e3c5-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e3c5-259">0x00000010</span></span>                                                         |
| <span data-ttu-id="2e3c5-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e3c5-260">Classes used in</span></span>        | [<span data-ttu-id="2e3c5-261">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2e3c5-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e3c5-262">Windows Server 2012</span></span>



| <span data-ttu-id="2e3c5-263">Ввод</span><span class="sxs-lookup"><span data-stu-id="2e3c5-263">Entry</span></span> | <span data-ttu-id="2e3c5-264">Значение</span><span class="sxs-lookup"><span data-stu-id="2e3c5-264">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2e3c5-265">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2e3c5-265">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="2e3c5-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2e3c5-266">MAPI-Id</span></span>                | <span data-ttu-id="2e3c5-267">0x8C53</span><span class="sxs-lookup"><span data-stu-id="2e3c5-267">0x8C53</span></span>                                                             |
| <span data-ttu-id="2e3c5-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="2e3c5-268">System-Only</span></span>            | <span data-ttu-id="2e3c5-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-269">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-270">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2e3c5-270">Is-Single-Valued</span></span>       | <span data-ttu-id="2e3c5-271">True</span><span class="sxs-lookup"><span data-stu-id="2e3c5-271">True</span></span>                                                               |
| <span data-ttu-id="2e3c5-272">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2e3c5-272">Is Indexed</span></span>             | <span data-ttu-id="2e3c5-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-273">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-274">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2e3c5-274">In Global Catalog</span></span>      | <span data-ttu-id="2e3c5-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="2e3c5-275">False</span></span>                                                              |
| <span data-ttu-id="2e3c5-276">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2e3c5-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="2e3c5-277">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2e3c5-277">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="2e3c5-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2e3c5-278">Range-Lower</span></span>            | <span data-ttu-id="2e3c5-279">1</span><span class="sxs-lookup"><span data-stu-id="2e3c5-279">1</span></span>                                                                  |
| <span data-ttu-id="2e3c5-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2e3c5-280">Range-Upper</span></span>            | <span data-ttu-id="2e3c5-281">64</span><span class="sxs-lookup"><span data-stu-id="2e3c5-281">64</span></span>                                                                 |
| <span data-ttu-id="2e3c5-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-282">Search-Flags</span></span>           | <span data-ttu-id="2e3c5-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2e3c5-283">0x00000000</span></span>                                                         |
| <span data-ttu-id="2e3c5-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2e3c5-284">System-Flags</span></span>           | <span data-ttu-id="2e3c5-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e3c5-285">0x00000010</span></span>                                                         |
| <span data-ttu-id="2e3c5-286">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2e3c5-286">Classes used in</span></span>        | [<span data-ttu-id="2e3c5-287">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="2e3c5-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





