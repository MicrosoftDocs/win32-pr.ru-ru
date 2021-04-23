---
title: Атрибут журнала NT-PWD-History
description: Журнал паролей пользователя в одностороннего формата Windows NT (OWF). Windows 2000 использует Windows NT OWF.
ms.assetid: 7c6a0fe2-561e-43a2-af46-7505e7e13288
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута NT-PWD-History
- Схема AD атрибута Нтпвдхистори
topic_type:
- apiref
api_name:
- Nt-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41ed3196109d13d4fb6cfae7e23be7ffdfb8c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536197"
---
# <a name="nt-pwd-history-attribute"></a><span data-ttu-id="710bb-106">Атрибут журнала NT-PWD-History</span><span class="sxs-lookup"><span data-stu-id="710bb-106">Nt-Pwd-History attribute</span></span>

<span data-ttu-id="710bb-107">Журнал паролей пользователя в одностороннего формата Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="710bb-107">The password history of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="710bb-108">Windows 2000 использует Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="710bb-108">Windows 2000 uses the Windows NT OWF.</span></span>



| <span data-ttu-id="710bb-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="710bb-109">Entry</span></span> | <span data-ttu-id="710bb-110">Значение</span><span class="sxs-lookup"><span data-stu-id="710bb-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="710bb-111">CN</span><span class="sxs-lookup"><span data-stu-id="710bb-111">CN</span></span>                | <span data-ttu-id="710bb-112">NT-PWD-History</span><span class="sxs-lookup"><span data-stu-id="710bb-112">Nt-Pwd-History</span></span>                                        |
| <span data-ttu-id="710bb-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="710bb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="710bb-114">нтпвдхистори</span><span class="sxs-lookup"><span data-stu-id="710bb-114">ntPwdHistory</span></span>                                          |
| <span data-ttu-id="710bb-115">Размер</span><span class="sxs-lookup"><span data-stu-id="710bb-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="710bb-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="710bb-116">Update Privilege</span></span>  | <span data-ttu-id="710bb-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="710bb-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="710bb-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="710bb-118">Update Frequency</span></span>  | <span data-ttu-id="710bb-119">Каждый раз, когда пользователь изменяет пароли.</span><span class="sxs-lookup"><span data-stu-id="710bb-119">Each time the user changes passwords.</span></span>                 |
| <span data-ttu-id="710bb-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="710bb-120">Attribute-Id</span></span>      | <span data-ttu-id="710bb-121">1.2.840.113556.1.4.94</span><span class="sxs-lookup"><span data-stu-id="710bb-121">1.2.840.113556.1.4.94</span></span>                                 |
| <span data-ttu-id="710bb-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="710bb-122">System-Id-Guid</span></span>    | <span data-ttu-id="710bb-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="710bb-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="710bb-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="710bb-124">Syntax</span></span>            | [<span data-ttu-id="710bb-125">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="710bb-125">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="710bb-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="710bb-126">Implementations</span></span>

-   [<span data-ttu-id="710bb-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="710bb-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="710bb-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="710bb-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="710bb-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="710bb-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="710bb-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="710bb-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="710bb-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="710bb-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="710bb-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="710bb-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="710bb-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="710bb-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="710bb-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="710bb-134">Windows 2000 Server</span></span>



| <span data-ttu-id="710bb-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="710bb-135">Entry</span></span> | <span data-ttu-id="710bb-136">Значение</span><span class="sxs-lookup"><span data-stu-id="710bb-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="710bb-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="710bb-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710bb-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="710bb-139">System-Only</span></span>            | <span data-ttu-id="710bb-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-140">False</span></span>                             |
| <span data-ttu-id="710bb-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="710bb-141">Is-Single-Valued</span></span>       | <span data-ttu-id="710bb-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-142">False</span></span>                             |
| <span data-ttu-id="710bb-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="710bb-143">Is Indexed</span></span>             | <span data-ttu-id="710bb-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-144">False</span></span>                             |
| <span data-ttu-id="710bb-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="710bb-145">In Global Catalog</span></span>      | <span data-ttu-id="710bb-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-146">False</span></span>                             |
| <span data-ttu-id="710bb-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="710bb-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="710bb-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="710bb-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="710bb-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710bb-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="710bb-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710bb-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="710bb-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-151">Search-Flags</span></span>           | <span data-ttu-id="710bb-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710bb-152">0x00000000</span></span>                        |
| <span data-ttu-id="710bb-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-153">System-Flags</span></span>           | <span data-ttu-id="710bb-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710bb-154">0x00000010</span></span>                        |
| <span data-ttu-id="710bb-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="710bb-155">Classes used in</span></span>        | [<span data-ttu-id="710bb-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="710bb-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="710bb-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="710bb-157">Windows Server 2003</span></span>



| <span data-ttu-id="710bb-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="710bb-158">Entry</span></span> | <span data-ttu-id="710bb-159">Значение</span><span class="sxs-lookup"><span data-stu-id="710bb-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="710bb-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="710bb-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710bb-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="710bb-162">System-Only</span></span>            | <span data-ttu-id="710bb-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-163">False</span></span>                             |
| <span data-ttu-id="710bb-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="710bb-164">Is-Single-Valued</span></span>       | <span data-ttu-id="710bb-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-165">False</span></span>                             |
| <span data-ttu-id="710bb-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="710bb-166">Is Indexed</span></span>             | <span data-ttu-id="710bb-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-167">False</span></span>                             |
| <span data-ttu-id="710bb-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="710bb-168">In Global Catalog</span></span>      | <span data-ttu-id="710bb-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-169">False</span></span>                             |
| <span data-ttu-id="710bb-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="710bb-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="710bb-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="710bb-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="710bb-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710bb-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="710bb-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710bb-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="710bb-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-174">Search-Flags</span></span>           | <span data-ttu-id="710bb-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710bb-175">0x00000000</span></span>                        |
| <span data-ttu-id="710bb-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-176">System-Flags</span></span>           | <span data-ttu-id="710bb-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710bb-177">0x00000010</span></span>                        |
| <span data-ttu-id="710bb-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="710bb-178">Classes used in</span></span>        | [<span data-ttu-id="710bb-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="710bb-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="710bb-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="710bb-180">ADAM</span></span>



| <span data-ttu-id="710bb-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="710bb-181">Entry</span></span> | <span data-ttu-id="710bb-182">Значение</span><span class="sxs-lookup"><span data-stu-id="710bb-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="710bb-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="710bb-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="710bb-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710bb-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="710bb-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="710bb-185">System-Only</span></span>            | <span data-ttu-id="710bb-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-186">False</span></span>                                                             |
| <span data-ttu-id="710bb-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="710bb-187">Is-Single-Valued</span></span>       | <span data-ttu-id="710bb-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-188">False</span></span>                                                             |
| <span data-ttu-id="710bb-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="710bb-189">Is Indexed</span></span>             | <span data-ttu-id="710bb-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-190">False</span></span>                                                             |
| <span data-ttu-id="710bb-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="710bb-191">In Global Catalog</span></span>      | <span data-ttu-id="710bb-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-192">False</span></span>                                                             |
| <span data-ttu-id="710bb-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="710bb-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="710bb-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="710bb-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="710bb-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710bb-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="710bb-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710bb-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="710bb-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-197">Search-Flags</span></span>           | <span data-ttu-id="710bb-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710bb-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="710bb-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-199">System-Flags</span></span>           | <span data-ttu-id="710bb-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710bb-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="710bb-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="710bb-201">Classes used in</span></span>        | [<span data-ttu-id="710bb-202">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="710bb-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="710bb-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="710bb-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="710bb-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="710bb-204">Entry</span></span> | <span data-ttu-id="710bb-205">Значение</span><span class="sxs-lookup"><span data-stu-id="710bb-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="710bb-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="710bb-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710bb-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="710bb-208">System-Only</span></span>            | <span data-ttu-id="710bb-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-209">False</span></span>                             |
| <span data-ttu-id="710bb-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="710bb-210">Is-Single-Valued</span></span>       | <span data-ttu-id="710bb-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-211">False</span></span>                             |
| <span data-ttu-id="710bb-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="710bb-212">Is Indexed</span></span>             | <span data-ttu-id="710bb-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-213">False</span></span>                             |
| <span data-ttu-id="710bb-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="710bb-214">In Global Catalog</span></span>      | <span data-ttu-id="710bb-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-215">False</span></span>                             |
| <span data-ttu-id="710bb-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="710bb-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="710bb-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="710bb-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="710bb-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710bb-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="710bb-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710bb-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="710bb-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-220">Search-Flags</span></span>           | <span data-ttu-id="710bb-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710bb-221">0x00000000</span></span>                        |
| <span data-ttu-id="710bb-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-222">System-Flags</span></span>           | <span data-ttu-id="710bb-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710bb-223">0x00000010</span></span>                        |
| <span data-ttu-id="710bb-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="710bb-224">Classes used in</span></span>        | [<span data-ttu-id="710bb-225">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="710bb-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="710bb-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="710bb-226">Windows Server 2008</span></span>



| <span data-ttu-id="710bb-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="710bb-227">Entry</span></span> | <span data-ttu-id="710bb-228">Значение</span><span class="sxs-lookup"><span data-stu-id="710bb-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="710bb-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="710bb-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710bb-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="710bb-231">System-Only</span></span>            | <span data-ttu-id="710bb-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-232">False</span></span>                             |
| <span data-ttu-id="710bb-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="710bb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="710bb-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-234">False</span></span>                             |
| <span data-ttu-id="710bb-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="710bb-235">Is Indexed</span></span>             | <span data-ttu-id="710bb-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-236">False</span></span>                             |
| <span data-ttu-id="710bb-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="710bb-237">In Global Catalog</span></span>      | <span data-ttu-id="710bb-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-238">False</span></span>                             |
| <span data-ttu-id="710bb-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="710bb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="710bb-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="710bb-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="710bb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710bb-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="710bb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710bb-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="710bb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-243">Search-Flags</span></span>           | <span data-ttu-id="710bb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710bb-244">0x00000000</span></span>                        |
| <span data-ttu-id="710bb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-245">System-Flags</span></span>           | <span data-ttu-id="710bb-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710bb-246">0x00000010</span></span>                        |
| <span data-ttu-id="710bb-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="710bb-247">Classes used in</span></span>        | [<span data-ttu-id="710bb-248">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="710bb-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="710bb-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="710bb-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="710bb-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="710bb-250">Entry</span></span> | <span data-ttu-id="710bb-251">Значение</span><span class="sxs-lookup"><span data-stu-id="710bb-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="710bb-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="710bb-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710bb-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="710bb-254">System-Only</span></span>            | <span data-ttu-id="710bb-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-255">False</span></span>                             |
| <span data-ttu-id="710bb-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="710bb-256">Is-Single-Valued</span></span>       | <span data-ttu-id="710bb-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-257">False</span></span>                             |
| <span data-ttu-id="710bb-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="710bb-258">Is Indexed</span></span>             | <span data-ttu-id="710bb-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-259">False</span></span>                             |
| <span data-ttu-id="710bb-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="710bb-260">In Global Catalog</span></span>      | <span data-ttu-id="710bb-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-261">False</span></span>                             |
| <span data-ttu-id="710bb-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="710bb-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="710bb-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="710bb-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="710bb-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710bb-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="710bb-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710bb-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="710bb-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-266">Search-Flags</span></span>           | <span data-ttu-id="710bb-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710bb-267">0x00000000</span></span>                        |
| <span data-ttu-id="710bb-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-268">System-Flags</span></span>           | <span data-ttu-id="710bb-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710bb-269">0x00000010</span></span>                        |
| <span data-ttu-id="710bb-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="710bb-270">Classes used in</span></span>        | [<span data-ttu-id="710bb-271">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="710bb-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="710bb-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="710bb-272">Windows Server 2012</span></span>



| <span data-ttu-id="710bb-273">Ввод</span><span class="sxs-lookup"><span data-stu-id="710bb-273">Entry</span></span> | <span data-ttu-id="710bb-274">Значение</span><span class="sxs-lookup"><span data-stu-id="710bb-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="710bb-275">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="710bb-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710bb-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="710bb-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="710bb-277">System-Only</span></span>            | <span data-ttu-id="710bb-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-278">False</span></span>                             |
| <span data-ttu-id="710bb-279">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="710bb-279">Is-Single-Valued</span></span>       | <span data-ttu-id="710bb-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-280">False</span></span>                             |
| <span data-ttu-id="710bb-281">Индексируется</span><span class="sxs-lookup"><span data-stu-id="710bb-281">Is Indexed</span></span>             | <span data-ttu-id="710bb-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-282">False</span></span>                             |
| <span data-ttu-id="710bb-283">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="710bb-283">In Global Catalog</span></span>      | <span data-ttu-id="710bb-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="710bb-284">False</span></span>                             |
| <span data-ttu-id="710bb-285">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="710bb-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="710bb-286">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="710bb-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="710bb-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710bb-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="710bb-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710bb-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="710bb-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-289">Search-Flags</span></span>           | <span data-ttu-id="710bb-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710bb-290">0x00000000</span></span>                        |
| <span data-ttu-id="710bb-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710bb-291">System-Flags</span></span>           | <span data-ttu-id="710bb-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710bb-292">0x00000010</span></span>                        |
| <span data-ttu-id="710bb-293">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="710bb-293">Classes used in</span></span>        | [<span data-ttu-id="710bb-294">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="710bb-294">**User**</span></span>](c-user.md)<br/> |



 

 





