---
title: атрибут MS-TAPI-unique-identifier
description: Предоставляет имя многоадресной конференции TAPI. Это атрибут именования класса Rt-Conference.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-TAPI-unique-identifier
- Мстапи — схема AD атрибута UID
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416257"
---
# <a name="ms-tapi-unique-identifier-attribute"></a><span data-ttu-id="17516-106">атрибут MS-TAPI-unique-identifier</span><span class="sxs-lookup"><span data-stu-id="17516-106">ms-TAPI-Unique-Identifier attribute</span></span>

<span data-ttu-id="17516-107">Предоставляет имя многоадресной конференции TAPI.</span><span class="sxs-lookup"><span data-stu-id="17516-107">Provides the name of a TAPI multicast conference.</span></span> <span data-ttu-id="17516-108">Это атрибут именования класса Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="17516-108">It is the naming attribute of the Rt-Conference class.</span></span>



| <span data-ttu-id="17516-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="17516-109">Entry</span></span> | <span data-ttu-id="17516-110">Значение</span><span class="sxs-lookup"><span data-stu-id="17516-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="17516-111">CN</span><span class="sxs-lookup"><span data-stu-id="17516-111">CN</span></span>                | <span data-ttu-id="17516-112">MS-TAPI-unique-identifier</span><span class="sxs-lookup"><span data-stu-id="17516-112">ms-TAPI-Unique-Identifier</span></span>                                             |
| <span data-ttu-id="17516-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="17516-113">Ldap-Display-Name</span></span> | <span data-ttu-id="17516-114">Мстапи — UID</span><span class="sxs-lookup"><span data-stu-id="17516-114">msTAPI-uid</span></span>                                                            |
| <span data-ttu-id="17516-115">Размер</span><span class="sxs-lookup"><span data-stu-id="17516-115">Size</span></span>              | <span data-ttu-id="17516-116">Может быть произвольной строкой, обычно длина которой не превышает 100 символов.</span><span class="sxs-lookup"><span data-stu-id="17516-116">Can be an arbitrary string, typically under 100 characters in length.</span></span> |
| <span data-ttu-id="17516-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="17516-117">Update Privilege</span></span>  | <span data-ttu-id="17516-118">Специальные привилегии не требуются.</span><span class="sxs-lookup"><span data-stu-id="17516-118">No special privileges required.</span></span>                                       |
| <span data-ttu-id="17516-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="17516-119">Update Frequency</span></span>  | <span data-ttu-id="17516-120">Задается один раз во время создания объекта Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="17516-120">Set once at the time of creating the Rt-Conference object.</span></span>            |
| <span data-ttu-id="17516-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="17516-121">Attribute-Id</span></span>      | <span data-ttu-id="17516-122">1.2.840.113556.1.4.1698</span><span class="sxs-lookup"><span data-stu-id="17516-122">1.2.840.113556.1.4.1698</span></span>                                               |
| <span data-ttu-id="17516-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="17516-123">System-Id-Guid</span></span>    | <span data-ttu-id="17516-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span><span class="sxs-lookup"><span data-stu-id="17516-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span></span>                                  |
| <span data-ttu-id="17516-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17516-125">Syntax</span></span>            | [<span data-ttu-id="17516-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="17516-126">**String(Unicode)**</span></span>](s-string-unicode.md)                           |



## <a name="implementations"></a><span data-ttu-id="17516-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="17516-127">Implementations</span></span>

-   [<span data-ttu-id="17516-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="17516-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="17516-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="17516-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="17516-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="17516-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="17516-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="17516-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="17516-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="17516-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="17516-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17516-133">Windows Server 2003</span></span>



| <span data-ttu-id="17516-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="17516-134">Entry</span></span> | <span data-ttu-id="17516-135">Значение</span><span class="sxs-lookup"><span data-stu-id="17516-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17516-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17516-136">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17516-137">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="17516-138">System-Only</span></span>            | <span data-ttu-id="17516-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-139">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17516-140">Is-Single-Valued</span></span>       | <span data-ttu-id="17516-141">True</span><span class="sxs-lookup"><span data-stu-id="17516-141">True</span></span>                                                                                                                        |
| <span data-ttu-id="17516-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17516-142">Is Indexed</span></span>             | <span data-ttu-id="17516-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-143">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17516-144">In Global Catalog</span></span>      | <span data-ttu-id="17516-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-145">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17516-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="17516-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17516-147">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="17516-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17516-148">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17516-149">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-150">Search-Flags</span></span>           | <span data-ttu-id="17516-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17516-151">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="17516-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-152">System-Flags</span></span>           | <span data-ttu-id="17516-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17516-153">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="17516-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17516-154">Classes used in</span></span>        | [<span data-ttu-id="17516-155">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="17516-155">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="17516-156">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="17516-156">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="17516-157">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="17516-157">Windows Server 2003 R2</span></span>



| <span data-ttu-id="17516-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="17516-158">Entry</span></span> | <span data-ttu-id="17516-159">Значение</span><span class="sxs-lookup"><span data-stu-id="17516-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17516-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17516-160">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17516-161">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="17516-162">System-Only</span></span>            | <span data-ttu-id="17516-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-163">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17516-164">Is-Single-Valued</span></span>       | <span data-ttu-id="17516-165">True</span><span class="sxs-lookup"><span data-stu-id="17516-165">True</span></span>                                                                                                                        |
| <span data-ttu-id="17516-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17516-166">Is Indexed</span></span>             | <span data-ttu-id="17516-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-167">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17516-168">In Global Catalog</span></span>      | <span data-ttu-id="17516-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-169">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17516-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="17516-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17516-171">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="17516-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17516-172">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17516-173">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-174">Search-Flags</span></span>           | <span data-ttu-id="17516-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17516-175">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="17516-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-176">System-Flags</span></span>           | <span data-ttu-id="17516-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17516-177">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="17516-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17516-178">Classes used in</span></span>        | [<span data-ttu-id="17516-179">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="17516-179">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="17516-180">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="17516-180">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="17516-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17516-181">Windows Server 2008</span></span>



| <span data-ttu-id="17516-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="17516-182">Entry</span></span> | <span data-ttu-id="17516-183">Значение</span><span class="sxs-lookup"><span data-stu-id="17516-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17516-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17516-184">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17516-185">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="17516-186">System-Only</span></span>            | <span data-ttu-id="17516-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-187">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17516-188">Is-Single-Valued</span></span>       | <span data-ttu-id="17516-189">True</span><span class="sxs-lookup"><span data-stu-id="17516-189">True</span></span>                                                                                                                        |
| <span data-ttu-id="17516-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17516-190">Is Indexed</span></span>             | <span data-ttu-id="17516-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-191">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17516-192">In Global Catalog</span></span>      | <span data-ttu-id="17516-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-193">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17516-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="17516-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17516-195">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="17516-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17516-196">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17516-197">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-198">Search-Flags</span></span>           | <span data-ttu-id="17516-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17516-199">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="17516-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-200">System-Flags</span></span>           | <span data-ttu-id="17516-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17516-201">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="17516-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17516-202">Classes used in</span></span>        | [<span data-ttu-id="17516-203">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="17516-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="17516-204">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="17516-204">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="17516-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17516-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="17516-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="17516-206">Entry</span></span> | <span data-ttu-id="17516-207">Значение</span><span class="sxs-lookup"><span data-stu-id="17516-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17516-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17516-208">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17516-209">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="17516-210">System-Only</span></span>            | <span data-ttu-id="17516-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-211">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17516-212">Is-Single-Valued</span></span>       | <span data-ttu-id="17516-213">True</span><span class="sxs-lookup"><span data-stu-id="17516-213">True</span></span>                                                                                                                        |
| <span data-ttu-id="17516-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17516-214">Is Indexed</span></span>             | <span data-ttu-id="17516-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-215">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17516-216">In Global Catalog</span></span>      | <span data-ttu-id="17516-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-217">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17516-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="17516-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17516-219">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="17516-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17516-220">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17516-221">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-222">Search-Flags</span></span>           | <span data-ttu-id="17516-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17516-223">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="17516-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-224">System-Flags</span></span>           | <span data-ttu-id="17516-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17516-225">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="17516-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17516-226">Classes used in</span></span>        | [<span data-ttu-id="17516-227">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="17516-227">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="17516-228">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="17516-228">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="17516-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17516-229">Windows Server 2012</span></span>



| <span data-ttu-id="17516-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="17516-230">Entry</span></span> | <span data-ttu-id="17516-231">Значение</span><span class="sxs-lookup"><span data-stu-id="17516-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17516-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="17516-232">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="17516-233">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="17516-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="17516-234">System-Only</span></span>            | <span data-ttu-id="17516-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-235">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="17516-236">Is-Single-Valued</span></span>       | <span data-ttu-id="17516-237">True</span><span class="sxs-lookup"><span data-stu-id="17516-237">True</span></span>                                                                                                                        |
| <span data-ttu-id="17516-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="17516-238">Is Indexed</span></span>             | <span data-ttu-id="17516-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-239">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="17516-240">In Global Catalog</span></span>      | <span data-ttu-id="17516-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="17516-241">False</span></span>                                                                                                                       |
| <span data-ttu-id="17516-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="17516-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="17516-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="17516-243">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="17516-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="17516-244">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="17516-245">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="17516-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-246">Search-Flags</span></span>           | <span data-ttu-id="17516-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="17516-247">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="17516-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="17516-248">System-Flags</span></span>           | <span data-ttu-id="17516-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="17516-249">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="17516-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="17516-250">Classes used in</span></span>        | [<span data-ttu-id="17516-251">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="17516-251">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="17516-252">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="17516-252">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





