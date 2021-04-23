---
title: Атрибут Script-Path
description: Этот атрибут указывает путь к сценарию входа пользователя. Строка может иметь значение null.
ms.assetid: 356f2ba0-ceca-4805-a536-286c6a8b54fc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Script-Path
- Схема AD атрибута scriptPath
topic_type:
- apiref
api_name:
- Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0909c35c41ae65f75481910d1377aa2761e99487
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138774"
---
# <a name="script-path-attribute"></a><span data-ttu-id="e9bb0-106">Атрибут Script-Path</span><span class="sxs-lookup"><span data-stu-id="e9bb0-106">Script-Path attribute</span></span>

<span data-ttu-id="e9bb0-107">Этот атрибут указывает путь к сценарию входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="e9bb0-107">This attribute specifies the path for the user's logon script.</span></span> <span data-ttu-id="e9bb0-108">Строка может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="e9bb0-108">The string can be null.</span></span>



| <span data-ttu-id="e9bb0-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9bb0-109">Entry</span></span> | <span data-ttu-id="e9bb0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e9bb0-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="e9bb0-111">CN</span><span class="sxs-lookup"><span data-stu-id="e9bb0-111">CN</span></span>                | <span data-ttu-id="e9bb0-112">Script-Path</span><span class="sxs-lookup"><span data-stu-id="e9bb0-112">Script-Path</span></span>                                                            |
| <span data-ttu-id="e9bb0-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e9bb0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e9bb0-114">scriptPath</span><span class="sxs-lookup"><span data-stu-id="e9bb0-114">scriptPath</span></span>                                                             |
| <span data-ttu-id="e9bb0-115">Размер</span><span class="sxs-lookup"><span data-stu-id="e9bb0-115">Size</span></span>              | \-                                                                     |
| <span data-ttu-id="e9bb0-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e9bb0-116">Update Privilege</span></span>  | <span data-ttu-id="e9bb0-117">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e9bb0-117">Domain administrator or account owner.</span></span>                                 |
| <span data-ttu-id="e9bb0-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e9bb0-118">Update Frequency</span></span>  | <span data-ttu-id="e9bb0-119">При создании записи пользователя, когда необходимо изменить путь.</span><span class="sxs-lookup"><span data-stu-id="e9bb0-119">When the user record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="e9bb0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e9bb0-120">Attribute-Id</span></span>      | <span data-ttu-id="e9bb0-121">1.2.840.113556.1.4.62</span><span class="sxs-lookup"><span data-stu-id="e9bb0-121">1.2.840.113556.1.4.62</span></span>                                                  |
| <span data-ttu-id="e9bb0-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e9bb0-122">System-Id-Guid</span></span>    | <span data-ttu-id="e9bb0-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e9bb0-123">bf9679a8-0de6-11d0-a285-00aa003049e2</span></span>                                   |
| <span data-ttu-id="e9bb0-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9bb0-124">Syntax</span></span>            | [<span data-ttu-id="e9bb0-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-125">**String(Unicode)**</span></span>](s-string-unicode.md)                            |



## <a name="implementations"></a><span data-ttu-id="e9bb0-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e9bb0-126">Implementations</span></span>

-   [<span data-ttu-id="e9bb0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e9bb0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e9bb0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e9bb0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e9bb0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e9bb0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e9bb0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9bb0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="e9bb0-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9bb0-134">Entry</span></span> | <span data-ttu-id="e9bb0-135">Значение</span><span class="sxs-lookup"><span data-stu-id="e9bb0-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9bb0-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9bb0-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9bb0-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9bb0-138">System-Only</span></span>            | <span data-ttu-id="e9bb0-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-139">False</span></span>                             |
| <span data-ttu-id="e9bb0-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9bb0-140">Is-Single-Valued</span></span>       | <span data-ttu-id="e9bb0-141">True</span><span class="sxs-lookup"><span data-stu-id="e9bb0-141">True</span></span>                              |
| <span data-ttu-id="e9bb0-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9bb0-142">Is Indexed</span></span>             | <span data-ttu-id="e9bb0-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-143">False</span></span>                             |
| <span data-ttu-id="e9bb0-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9bb0-144">In Global Catalog</span></span>      | <span data-ttu-id="e9bb0-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-145">False</span></span>                             |
| <span data-ttu-id="e9bb0-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9bb0-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9bb0-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9bb0-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9bb0-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9bb0-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9bb0-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-150">Search-Flags</span></span>           | <span data-ttu-id="e9bb0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-151">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-152">System-Flags</span></span>           | <span data-ttu-id="e9bb0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-153">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9bb0-154">Classes used in</span></span>        | [<span data-ttu-id="e9bb0-155">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e9bb0-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9bb0-156">Windows Server 2003</span></span>



| <span data-ttu-id="e9bb0-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9bb0-157">Entry</span></span> | <span data-ttu-id="e9bb0-158">Значение</span><span class="sxs-lookup"><span data-stu-id="e9bb0-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9bb0-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9bb0-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9bb0-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9bb0-161">System-Only</span></span>            | <span data-ttu-id="e9bb0-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-162">False</span></span>                             |
| <span data-ttu-id="e9bb0-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9bb0-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e9bb0-164">True</span><span class="sxs-lookup"><span data-stu-id="e9bb0-164">True</span></span>                              |
| <span data-ttu-id="e9bb0-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9bb0-165">Is Indexed</span></span>             | <span data-ttu-id="e9bb0-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-166">False</span></span>                             |
| <span data-ttu-id="e9bb0-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9bb0-167">In Global Catalog</span></span>      | <span data-ttu-id="e9bb0-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-168">False</span></span>                             |
| <span data-ttu-id="e9bb0-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9bb0-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9bb0-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9bb0-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9bb0-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9bb0-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9bb0-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-173">Search-Flags</span></span>           | <span data-ttu-id="e9bb0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-174">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-175">System-Flags</span></span>           | <span data-ttu-id="e9bb0-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-176">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9bb0-177">Classes used in</span></span>        | [<span data-ttu-id="e9bb0-178">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e9bb0-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e9bb0-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e9bb0-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9bb0-180">Entry</span></span> | <span data-ttu-id="e9bb0-181">Значение</span><span class="sxs-lookup"><span data-stu-id="e9bb0-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9bb0-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9bb0-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9bb0-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9bb0-184">System-Only</span></span>            | <span data-ttu-id="e9bb0-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-185">False</span></span>                             |
| <span data-ttu-id="e9bb0-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9bb0-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e9bb0-187">True</span><span class="sxs-lookup"><span data-stu-id="e9bb0-187">True</span></span>                              |
| <span data-ttu-id="e9bb0-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9bb0-188">Is Indexed</span></span>             | <span data-ttu-id="e9bb0-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-189">False</span></span>                             |
| <span data-ttu-id="e9bb0-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9bb0-190">In Global Catalog</span></span>      | <span data-ttu-id="e9bb0-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-191">False</span></span>                             |
| <span data-ttu-id="e9bb0-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9bb0-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9bb0-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9bb0-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9bb0-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9bb0-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9bb0-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-196">Search-Flags</span></span>           | <span data-ttu-id="e9bb0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-197">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-198">System-Flags</span></span>           | <span data-ttu-id="e9bb0-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-199">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9bb0-200">Classes used in</span></span>        | [<span data-ttu-id="e9bb0-201">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e9bb0-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9bb0-202">Windows Server 2008</span></span>



| <span data-ttu-id="e9bb0-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9bb0-203">Entry</span></span> | <span data-ttu-id="e9bb0-204">Значение</span><span class="sxs-lookup"><span data-stu-id="e9bb0-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9bb0-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9bb0-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9bb0-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9bb0-207">System-Only</span></span>            | <span data-ttu-id="e9bb0-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-208">False</span></span>                             |
| <span data-ttu-id="e9bb0-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9bb0-209">Is-Single-Valued</span></span>       | <span data-ttu-id="e9bb0-210">True</span><span class="sxs-lookup"><span data-stu-id="e9bb0-210">True</span></span>                              |
| <span data-ttu-id="e9bb0-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9bb0-211">Is Indexed</span></span>             | <span data-ttu-id="e9bb0-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-212">False</span></span>                             |
| <span data-ttu-id="e9bb0-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9bb0-213">In Global Catalog</span></span>      | <span data-ttu-id="e9bb0-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-214">False</span></span>                             |
| <span data-ttu-id="e9bb0-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9bb0-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9bb0-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9bb0-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9bb0-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9bb0-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9bb0-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-219">Search-Flags</span></span>           | <span data-ttu-id="e9bb0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-220">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-221">System-Flags</span></span>           | <span data-ttu-id="e9bb0-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-222">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9bb0-223">Classes used in</span></span>        | [<span data-ttu-id="e9bb0-224">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e9bb0-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9bb0-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e9bb0-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9bb0-226">Entry</span></span> | <span data-ttu-id="e9bb0-227">Значение</span><span class="sxs-lookup"><span data-stu-id="e9bb0-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9bb0-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9bb0-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9bb0-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9bb0-230">System-Only</span></span>            | <span data-ttu-id="e9bb0-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-231">False</span></span>                             |
| <span data-ttu-id="e9bb0-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9bb0-232">Is-Single-Valued</span></span>       | <span data-ttu-id="e9bb0-233">True</span><span class="sxs-lookup"><span data-stu-id="e9bb0-233">True</span></span>                              |
| <span data-ttu-id="e9bb0-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9bb0-234">Is Indexed</span></span>             | <span data-ttu-id="e9bb0-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-235">False</span></span>                             |
| <span data-ttu-id="e9bb0-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9bb0-236">In Global Catalog</span></span>      | <span data-ttu-id="e9bb0-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-237">False</span></span>                             |
| <span data-ttu-id="e9bb0-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9bb0-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9bb0-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9bb0-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9bb0-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9bb0-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9bb0-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-242">Search-Flags</span></span>           | <span data-ttu-id="e9bb0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-243">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-244">System-Flags</span></span>           | <span data-ttu-id="e9bb0-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-245">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9bb0-246">Classes used in</span></span>        | [<span data-ttu-id="e9bb0-247">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e9bb0-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9bb0-248">Windows Server 2012</span></span>



| <span data-ttu-id="e9bb0-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9bb0-249">Entry</span></span> | <span data-ttu-id="e9bb0-250">Значение</span><span class="sxs-lookup"><span data-stu-id="e9bb0-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="e9bb0-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9bb0-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9bb0-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="e9bb0-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9bb0-253">System-Only</span></span>            | <span data-ttu-id="e9bb0-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-254">False</span></span>                             |
| <span data-ttu-id="e9bb0-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9bb0-255">Is-Single-Valued</span></span>       | <span data-ttu-id="e9bb0-256">True</span><span class="sxs-lookup"><span data-stu-id="e9bb0-256">True</span></span>                              |
| <span data-ttu-id="e9bb0-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9bb0-257">Is Indexed</span></span>             | <span data-ttu-id="e9bb0-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-258">False</span></span>                             |
| <span data-ttu-id="e9bb0-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9bb0-259">In Global Catalog</span></span>      | <span data-ttu-id="e9bb0-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9bb0-260">False</span></span>                             |
| <span data-ttu-id="e9bb0-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9bb0-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9bb0-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9bb0-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="e9bb0-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9bb0-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9bb0-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="e9bb0-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-265">Search-Flags</span></span>           | <span data-ttu-id="e9bb0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-266">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9bb0-267">System-Flags</span></span>           | <span data-ttu-id="e9bb0-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9bb0-268">0x00000010</span></span>                        |
| <span data-ttu-id="e9bb0-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9bb0-269">Classes used in</span></span>        | [<span data-ttu-id="e9bb0-270">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="e9bb0-270">**User**</span></span>](c-user.md)<br/> |



 

 





