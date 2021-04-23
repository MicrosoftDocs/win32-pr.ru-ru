---
title: атрибут MS-TAPI-Protocol-ID
description: Этот атрибут указывает тип конференции TAPI.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-TAPI-ID
- Схема AD атрибута Мстапи-Протоколид
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10538f66b98988fafa69d4fe2f3e70b47348c999
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138875"
---
# <a name="ms-tapi-protocol-id-attribute"></a><span data-ttu-id="9fd30-105">атрибут MS-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="9fd30-105">ms-TAPI-Protocol-Id attribute</span></span>

<span data-ttu-id="9fd30-106">Этот атрибут указывает тип конференции TAPI.</span><span class="sxs-lookup"><span data-stu-id="9fd30-106">This attribute indicates the TAPI conference type.</span></span> <span data-ttu-id="9fd30-107">Этот атрибут используется для определения способа интерпретации двоичного объекта binary в атрибуте [**MS-TAPI-Conference-BLOB**](a-mstapi-conferenceblob.md) .</span><span class="sxs-lookup"><span data-stu-id="9fd30-107">This attribute is used to determine how the binary BLOB in the [**ms-TAPI-Conference-Blob**](a-mstapi-conferenceblob.md) attribute is to be interpreted.</span></span> <span data-ttu-id="9fd30-108">Этот атрибут является произвольной строкой, обычно длина которой меньше 100 символов.</span><span class="sxs-lookup"><span data-stu-id="9fd30-108">This attribute is an arbitrary string, typically less than 100 characters in length.</span></span>



| <span data-ttu-id="9fd30-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fd30-109">Entry</span></span> | <span data-ttu-id="9fd30-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9fd30-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="9fd30-111">CN</span><span class="sxs-lookup"><span data-stu-id="9fd30-111">CN</span></span>                | <span data-ttu-id="9fd30-112">MS-TAPI-Protocol-ID</span><span class="sxs-lookup"><span data-stu-id="9fd30-112">ms-TAPI-Protocol-Id</span></span>                                        |
| <span data-ttu-id="9fd30-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9fd30-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9fd30-114">Мстапи — Протоколид</span><span class="sxs-lookup"><span data-stu-id="9fd30-114">msTAPI-ProtocolId</span></span>                                          |
| <span data-ttu-id="9fd30-115">Размер</span><span class="sxs-lookup"><span data-stu-id="9fd30-115">Size</span></span>              | \-                                                         |
| <span data-ttu-id="9fd30-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9fd30-116">Update Privilege</span></span>  | <span data-ttu-id="9fd30-117">Специальные привилегии не требуются.</span><span class="sxs-lookup"><span data-stu-id="9fd30-117">No special privileges required.</span></span>                            |
| <span data-ttu-id="9fd30-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9fd30-118">Update Frequency</span></span>  | <span data-ttu-id="9fd30-119">Задается один раз во время создания объекта Rt-Conference.</span><span class="sxs-lookup"><span data-stu-id="9fd30-119">Set once at the time of creating the Rt-Conference object.</span></span> |
| <span data-ttu-id="9fd30-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9fd30-120">Attribute-Id</span></span>      | <span data-ttu-id="9fd30-121">1.2.840.113556.1.4.1699</span><span class="sxs-lookup"><span data-stu-id="9fd30-121">1.2.840.113556.1.4.1699</span></span>                                    |
| <span data-ttu-id="9fd30-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9fd30-122">System-Id-Guid</span></span>    | <span data-ttu-id="9fd30-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span><span class="sxs-lookup"><span data-stu-id="9fd30-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span></span>                       |
| <span data-ttu-id="9fd30-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fd30-124">Syntax</span></span>            | [<span data-ttu-id="9fd30-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="9fd30-125">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="9fd30-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9fd30-126">Implementations</span></span>

-   [<span data-ttu-id="9fd30-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9fd30-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9fd30-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9fd30-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9fd30-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9fd30-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9fd30-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9fd30-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9fd30-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9fd30-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9fd30-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9fd30-132">Windows Server 2003</span></span>



| <span data-ttu-id="9fd30-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fd30-133">Entry</span></span> | <span data-ttu-id="9fd30-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9fd30-134">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fd30-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fd30-135">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fd30-136">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fd30-137">System-Only</span></span>            | <span data-ttu-id="9fd30-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-138">False</span></span>                                                             |
| <span data-ttu-id="9fd30-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fd30-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9fd30-140">True</span><span class="sxs-lookup"><span data-stu-id="9fd30-140">True</span></span>                                                              |
| <span data-ttu-id="9fd30-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fd30-141">Is Indexed</span></span>             | <span data-ttu-id="9fd30-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-142">False</span></span>                                                             |
| <span data-ttu-id="9fd30-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fd30-143">In Global Catalog</span></span>      | <span data-ttu-id="9fd30-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-144">False</span></span>                                                             |
| <span data-ttu-id="9fd30-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fd30-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fd30-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fd30-146">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fd30-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fd30-147">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fd30-148">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-149">Search-Flags</span></span>           | <span data-ttu-id="9fd30-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fd30-150">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fd30-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-151">System-Flags</span></span>           | <span data-ttu-id="9fd30-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fd30-152">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fd30-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fd30-153">Classes used in</span></span>        | [<span data-ttu-id="9fd30-154">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fd30-154">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9fd30-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9fd30-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9fd30-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fd30-156">Entry</span></span> | <span data-ttu-id="9fd30-157">Значение</span><span class="sxs-lookup"><span data-stu-id="9fd30-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fd30-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fd30-158">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fd30-159">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fd30-160">System-Only</span></span>            | <span data-ttu-id="9fd30-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-161">False</span></span>                                                             |
| <span data-ttu-id="9fd30-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fd30-162">Is-Single-Valued</span></span>       | <span data-ttu-id="9fd30-163">True</span><span class="sxs-lookup"><span data-stu-id="9fd30-163">True</span></span>                                                              |
| <span data-ttu-id="9fd30-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fd30-164">Is Indexed</span></span>             | <span data-ttu-id="9fd30-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-165">False</span></span>                                                             |
| <span data-ttu-id="9fd30-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fd30-166">In Global Catalog</span></span>      | <span data-ttu-id="9fd30-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-167">False</span></span>                                                             |
| <span data-ttu-id="9fd30-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fd30-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fd30-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fd30-169">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fd30-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fd30-170">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fd30-171">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-172">Search-Flags</span></span>           | <span data-ttu-id="9fd30-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fd30-173">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fd30-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-174">System-Flags</span></span>           | <span data-ttu-id="9fd30-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fd30-175">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fd30-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fd30-176">Classes used in</span></span>        | [<span data-ttu-id="9fd30-177">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fd30-177">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9fd30-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fd30-178">Windows Server 2008</span></span>



| <span data-ttu-id="9fd30-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fd30-179">Entry</span></span> | <span data-ttu-id="9fd30-180">Значение</span><span class="sxs-lookup"><span data-stu-id="9fd30-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fd30-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fd30-181">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fd30-182">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fd30-183">System-Only</span></span>            | <span data-ttu-id="9fd30-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-184">False</span></span>                                                             |
| <span data-ttu-id="9fd30-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fd30-185">Is-Single-Valued</span></span>       | <span data-ttu-id="9fd30-186">True</span><span class="sxs-lookup"><span data-stu-id="9fd30-186">True</span></span>                                                              |
| <span data-ttu-id="9fd30-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fd30-187">Is Indexed</span></span>             | <span data-ttu-id="9fd30-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-188">False</span></span>                                                             |
| <span data-ttu-id="9fd30-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fd30-189">In Global Catalog</span></span>      | <span data-ttu-id="9fd30-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-190">False</span></span>                                                             |
| <span data-ttu-id="9fd30-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fd30-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fd30-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fd30-192">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fd30-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fd30-193">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fd30-194">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-195">Search-Flags</span></span>           | <span data-ttu-id="9fd30-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fd30-196">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fd30-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-197">System-Flags</span></span>           | <span data-ttu-id="9fd30-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fd30-198">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fd30-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fd30-199">Classes used in</span></span>        | [<span data-ttu-id="9fd30-200">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fd30-200">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9fd30-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9fd30-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9fd30-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fd30-202">Entry</span></span> | <span data-ttu-id="9fd30-203">Значение</span><span class="sxs-lookup"><span data-stu-id="9fd30-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fd30-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fd30-204">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fd30-205">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fd30-206">System-Only</span></span>            | <span data-ttu-id="9fd30-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-207">False</span></span>                                                             |
| <span data-ttu-id="9fd30-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fd30-208">Is-Single-Valued</span></span>       | <span data-ttu-id="9fd30-209">True</span><span class="sxs-lookup"><span data-stu-id="9fd30-209">True</span></span>                                                              |
| <span data-ttu-id="9fd30-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fd30-210">Is Indexed</span></span>             | <span data-ttu-id="9fd30-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-211">False</span></span>                                                             |
| <span data-ttu-id="9fd30-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fd30-212">In Global Catalog</span></span>      | <span data-ttu-id="9fd30-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-213">False</span></span>                                                             |
| <span data-ttu-id="9fd30-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fd30-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fd30-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fd30-215">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fd30-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fd30-216">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fd30-217">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-218">Search-Flags</span></span>           | <span data-ttu-id="9fd30-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fd30-219">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fd30-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-220">System-Flags</span></span>           | <span data-ttu-id="9fd30-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fd30-221">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fd30-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fd30-222">Classes used in</span></span>        | [<span data-ttu-id="9fd30-223">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fd30-223">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9fd30-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9fd30-224">Windows Server 2012</span></span>



| <span data-ttu-id="9fd30-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fd30-225">Entry</span></span> | <span data-ttu-id="9fd30-226">Значение</span><span class="sxs-lookup"><span data-stu-id="9fd30-226">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fd30-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fd30-227">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fd30-228">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fd30-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fd30-229">System-Only</span></span>            | <span data-ttu-id="9fd30-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-230">False</span></span>                                                             |
| <span data-ttu-id="9fd30-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fd30-231">Is-Single-Valued</span></span>       | <span data-ttu-id="9fd30-232">True</span><span class="sxs-lookup"><span data-stu-id="9fd30-232">True</span></span>                                                              |
| <span data-ttu-id="9fd30-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fd30-233">Is Indexed</span></span>             | <span data-ttu-id="9fd30-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-234">False</span></span>                                                             |
| <span data-ttu-id="9fd30-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fd30-235">In Global Catalog</span></span>      | <span data-ttu-id="9fd30-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fd30-236">False</span></span>                                                             |
| <span data-ttu-id="9fd30-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fd30-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fd30-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fd30-238">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fd30-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fd30-239">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fd30-240">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fd30-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-241">Search-Flags</span></span>           | <span data-ttu-id="9fd30-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fd30-242">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fd30-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fd30-243">System-Flags</span></span>           | <span data-ttu-id="9fd30-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fd30-244">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fd30-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fd30-245">Classes used in</span></span>        | [<span data-ttu-id="9fd30-246">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fd30-246">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





