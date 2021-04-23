---
title: Атрибут DS-UI-Admin-Notification
description: Это список идентификаторов GUID COM-объектов, поддерживающих интерфейс обратного вызова, Дсадмин вызовы при возникновении действия над объектом через пользовательский интерфейс.
ms.assetid: 4845c221-087f-49f5-a95d-71f58a4e8819
ms.tgt_platform: multiple
keywords:
- Active Directory — пользовательский интерфейс-администратор-схема атрибута уведомления AD
- Схема AD атрибута Дсуиадминнотификатион
topic_type:
- apiref
api_name:
- DS-UI-Admin-Notification
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7082d7a8fd751fa001ac796d2a86b60a28463e8b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654860"
---
# <a name="ds-ui-admin-notification-attribute"></a><span data-ttu-id="80d52-105">Атрибут DS-UI-Admin-Notification</span><span class="sxs-lookup"><span data-stu-id="80d52-105">DS-UI-Admin-Notification attribute</span></span>

<span data-ttu-id="80d52-106">Это список идентификаторов GUID COM-объектов, поддерживающих интерфейс обратного вызова, Дсадмин вызовы при возникновении действия над объектом через пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="80d52-106">This is a list of the GUIDs of COM objects that support a callback interface that DSAdmin calls when an action has occurred on an object through the UI.</span></span>



| <span data-ttu-id="80d52-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="80d52-107">Entry</span></span> | <span data-ttu-id="80d52-108">Значение</span><span class="sxs-lookup"><span data-stu-id="80d52-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="80d52-109">CN</span><span class="sxs-lookup"><span data-stu-id="80d52-109">CN</span></span>                | <span data-ttu-id="80d52-110">DS-UI-Admin — уведомление</span><span class="sxs-lookup"><span data-stu-id="80d52-110">DS-UI-Admin-Notification</span></span>                    |
| <span data-ttu-id="80d52-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="80d52-111">Ldap-Display-Name</span></span> | <span data-ttu-id="80d52-112">дсуиадминнотификатион</span><span class="sxs-lookup"><span data-stu-id="80d52-112">dSUIAdminNotification</span></span>                       |
| <span data-ttu-id="80d52-113">Размер</span><span class="sxs-lookup"><span data-stu-id="80d52-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="80d52-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="80d52-114">Update Privilege</span></span>  | <span data-ttu-id="80d52-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="80d52-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="80d52-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="80d52-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="80d52-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="80d52-117">Attribute-Id</span></span>      | <span data-ttu-id="80d52-118">1.2.840.113556.1.4.1343</span><span class="sxs-lookup"><span data-stu-id="80d52-118">1.2.840.113556.1.4.1343</span></span>                     |
| <span data-ttu-id="80d52-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="80d52-119">System-Id-Guid</span></span>    | <span data-ttu-id="80d52-120">f6ea0a94-6f91-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="80d52-120">f6ea0a94-6f91-11d2-9905-0000f87a57d4</span></span>        |
| <span data-ttu-id="80d52-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80d52-121">Syntax</span></span>            | [<span data-ttu-id="80d52-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="80d52-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="80d52-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="80d52-123">Implementations</span></span>

-   [<span data-ttu-id="80d52-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="80d52-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="80d52-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="80d52-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="80d52-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="80d52-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="80d52-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="80d52-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="80d52-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="80d52-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="80d52-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="80d52-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="80d52-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80d52-130">Windows 2000 Server</span></span>



| <span data-ttu-id="80d52-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="80d52-131">Entry</span></span> | <span data-ttu-id="80d52-132">Значение</span><span class="sxs-lookup"><span data-stu-id="80d52-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="80d52-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80d52-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80d52-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="80d52-135">System-Only</span></span>            | <span data-ttu-id="80d52-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-136">False</span></span>                                               |
| <span data-ttu-id="80d52-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80d52-137">Is-Single-Valued</span></span>       | <span data-ttu-id="80d52-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-138">False</span></span>                                               |
| <span data-ttu-id="80d52-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80d52-139">Is Indexed</span></span>             | <span data-ttu-id="80d52-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-140">False</span></span>                                               |
| <span data-ttu-id="80d52-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80d52-141">In Global Catalog</span></span>      | <span data-ttu-id="80d52-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-142">False</span></span>                                               |
| <span data-ttu-id="80d52-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80d52-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="80d52-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80d52-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="80d52-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80d52-145">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80d52-146">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-147">Search-Flags</span></span>           | <span data-ttu-id="80d52-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80d52-148">0x00000000</span></span>                                          |
| <span data-ttu-id="80d52-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-149">System-Flags</span></span>           | <span data-ttu-id="80d52-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80d52-150">0x00000010</span></span>                                          |
| <span data-ttu-id="80d52-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80d52-151">Classes used in</span></span>        | [<span data-ttu-id="80d52-152">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="80d52-152">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="80d52-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80d52-153">Windows Server 2003</span></span>



| <span data-ttu-id="80d52-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="80d52-154">Entry</span></span> | <span data-ttu-id="80d52-155">Значение</span><span class="sxs-lookup"><span data-stu-id="80d52-155">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="80d52-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80d52-156">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80d52-157">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="80d52-158">System-Only</span></span>            | <span data-ttu-id="80d52-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-159">False</span></span>                                               |
| <span data-ttu-id="80d52-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80d52-160">Is-Single-Valued</span></span>       | <span data-ttu-id="80d52-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-161">False</span></span>                                               |
| <span data-ttu-id="80d52-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80d52-162">Is Indexed</span></span>             | <span data-ttu-id="80d52-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-163">False</span></span>                                               |
| <span data-ttu-id="80d52-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80d52-164">In Global Catalog</span></span>      | <span data-ttu-id="80d52-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-165">False</span></span>                                               |
| <span data-ttu-id="80d52-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80d52-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="80d52-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80d52-167">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="80d52-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80d52-168">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80d52-169">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-170">Search-Flags</span></span>           | <span data-ttu-id="80d52-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80d52-171">0x00000000</span></span>                                          |
| <span data-ttu-id="80d52-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-172">System-Flags</span></span>           | <span data-ttu-id="80d52-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80d52-173">0x00000010</span></span>                                          |
| <span data-ttu-id="80d52-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80d52-174">Classes used in</span></span>        | [<span data-ttu-id="80d52-175">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="80d52-175">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="80d52-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="80d52-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="80d52-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="80d52-177">Entry</span></span> | <span data-ttu-id="80d52-178">Значение</span><span class="sxs-lookup"><span data-stu-id="80d52-178">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="80d52-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80d52-179">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80d52-180">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="80d52-181">System-Only</span></span>            | <span data-ttu-id="80d52-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-182">False</span></span>                                               |
| <span data-ttu-id="80d52-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80d52-183">Is-Single-Valued</span></span>       | <span data-ttu-id="80d52-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-184">False</span></span>                                               |
| <span data-ttu-id="80d52-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80d52-185">Is Indexed</span></span>             | <span data-ttu-id="80d52-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-186">False</span></span>                                               |
| <span data-ttu-id="80d52-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80d52-187">In Global Catalog</span></span>      | <span data-ttu-id="80d52-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-188">False</span></span>                                               |
| <span data-ttu-id="80d52-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80d52-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="80d52-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80d52-190">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="80d52-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80d52-191">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80d52-192">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-193">Search-Flags</span></span>           | <span data-ttu-id="80d52-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80d52-194">0x00000000</span></span>                                          |
| <span data-ttu-id="80d52-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-195">System-Flags</span></span>           | <span data-ttu-id="80d52-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80d52-196">0x00000010</span></span>                                          |
| <span data-ttu-id="80d52-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80d52-197">Classes used in</span></span>        | [<span data-ttu-id="80d52-198">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="80d52-198">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="80d52-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80d52-199">Windows Server 2008</span></span>



| <span data-ttu-id="80d52-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="80d52-200">Entry</span></span> | <span data-ttu-id="80d52-201">Значение</span><span class="sxs-lookup"><span data-stu-id="80d52-201">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="80d52-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80d52-202">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80d52-203">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="80d52-204">System-Only</span></span>            | <span data-ttu-id="80d52-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-205">False</span></span>                                               |
| <span data-ttu-id="80d52-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80d52-206">Is-Single-Valued</span></span>       | <span data-ttu-id="80d52-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-207">False</span></span>                                               |
| <span data-ttu-id="80d52-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80d52-208">Is Indexed</span></span>             | <span data-ttu-id="80d52-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-209">False</span></span>                                               |
| <span data-ttu-id="80d52-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80d52-210">In Global Catalog</span></span>      | <span data-ttu-id="80d52-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-211">False</span></span>                                               |
| <span data-ttu-id="80d52-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80d52-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="80d52-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80d52-213">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="80d52-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80d52-214">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80d52-215">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-216">Search-Flags</span></span>           | <span data-ttu-id="80d52-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80d52-217">0x00000000</span></span>                                          |
| <span data-ttu-id="80d52-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-218">System-Flags</span></span>           | <span data-ttu-id="80d52-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80d52-219">0x00000010</span></span>                                          |
| <span data-ttu-id="80d52-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80d52-220">Classes used in</span></span>        | [<span data-ttu-id="80d52-221">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="80d52-221">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="80d52-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80d52-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="80d52-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="80d52-223">Entry</span></span> | <span data-ttu-id="80d52-224">Значение</span><span class="sxs-lookup"><span data-stu-id="80d52-224">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="80d52-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80d52-225">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80d52-226">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="80d52-227">System-Only</span></span>            | <span data-ttu-id="80d52-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-228">False</span></span>                                               |
| <span data-ttu-id="80d52-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80d52-229">Is-Single-Valued</span></span>       | <span data-ttu-id="80d52-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-230">False</span></span>                                               |
| <span data-ttu-id="80d52-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80d52-231">Is Indexed</span></span>             | <span data-ttu-id="80d52-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-232">False</span></span>                                               |
| <span data-ttu-id="80d52-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80d52-233">In Global Catalog</span></span>      | <span data-ttu-id="80d52-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-234">False</span></span>                                               |
| <span data-ttu-id="80d52-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80d52-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="80d52-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80d52-236">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="80d52-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80d52-237">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80d52-238">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-239">Search-Flags</span></span>           | <span data-ttu-id="80d52-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80d52-240">0x00000000</span></span>                                          |
| <span data-ttu-id="80d52-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-241">System-Flags</span></span>           | <span data-ttu-id="80d52-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80d52-242">0x00000010</span></span>                                          |
| <span data-ttu-id="80d52-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80d52-243">Classes used in</span></span>        | [<span data-ttu-id="80d52-244">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="80d52-244">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="80d52-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80d52-245">Windows Server 2012</span></span>



| <span data-ttu-id="80d52-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="80d52-246">Entry</span></span> | <span data-ttu-id="80d52-247">Значение</span><span class="sxs-lookup"><span data-stu-id="80d52-247">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="80d52-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="80d52-248">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="80d52-249">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="80d52-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="80d52-250">System-Only</span></span>            | <span data-ttu-id="80d52-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-251">False</span></span>                                               |
| <span data-ttu-id="80d52-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="80d52-252">Is-Single-Valued</span></span>       | <span data-ttu-id="80d52-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-253">False</span></span>                                               |
| <span data-ttu-id="80d52-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="80d52-254">Is Indexed</span></span>             | <span data-ttu-id="80d52-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-255">False</span></span>                                               |
| <span data-ttu-id="80d52-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="80d52-256">In Global Catalog</span></span>      | <span data-ttu-id="80d52-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d52-257">False</span></span>                                               |
| <span data-ttu-id="80d52-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="80d52-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="80d52-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="80d52-259">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="80d52-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="80d52-260">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="80d52-261">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="80d52-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-262">Search-Flags</span></span>           | <span data-ttu-id="80d52-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="80d52-263">0x00000000</span></span>                                          |
| <span data-ttu-id="80d52-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="80d52-264">System-Flags</span></span>           | <span data-ttu-id="80d52-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="80d52-265">0x00000010</span></span>                                          |
| <span data-ttu-id="80d52-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="80d52-266">Classes used in</span></span>        | [<span data-ttu-id="80d52-267">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="80d52-267">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



 

 





